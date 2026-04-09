---
title: "Terminology in IEC 62443"
date: 2026-04-09T18:10:43+02:00
tags: 
  - security
  - standardisation
description: "I have wrestled with some terminology in IEC 62443."
image: ""
aliases: []
draft: false
---
In general, IEC 62443 is quite well-written, especially if you compare it to (older) safety standards. But I've been wrestling with some of the terminology for months now.

Most of these questions might have been answered quickly if I had access to a TC 65X member telling me about the committee's intentions and current plans, but I don't, so I'm doing textual exegesis.

Let me sketch out my questions about four different terms in the published version from 2019, and how the current drafts for the next version of IEC 62443 mostly resolve those.

# Compensating countermeasures

This was my main hang-up. Compensating countermeasures basically bridge the gap between the target security level SL-T of a zone and the capability security level SL-C of a component.

If you don't satisfy a requirement in the component itself, but offer an external compensating countermeasure for it you potentially lose an SL-C level. But the component can still be used in a zone that calls for a higher SL-T, because the compensating countermeasure absorbs the risk differential between the lower SL-C and the higher SL-T.

Throughout several parts it is made clear that SL-C measures risk reduction without compensating countermeasures. -2-2 6.7.2 says “can meet without compensating security measures”. -3-2 Annex A says “capable of meeting the SL-Ts natively without additional compensating countermeasures”, -3-3 A.2 says “capable of meeting the target SLs natively without additional compensating countermeasures”.

But that was all parts 2 and 3. And in part 4 the situation changes somewhat:

-4-2 3.1.9 says “in addition to inherent security capabilities to satisfy one or more security requirements” and -4-2 4.3 says “requirements specified in this document cannot be met without the assistance of a compensating countermeasure that is external to the component”.

Here the intention seems to be that your component requirement can actually be met with the help of compensating countermeasures, and your higher SL-C is saved.

And then -6-2 hits the core of my confusion: 3.1.15 defines “met by system integration” and speaks of REs and CRs delegated to a higher-level system the component integrates into. It specifically says “are met by the system” and “with the assistance of compensating countermeasure”. Also, 5.7.2.4 says “component requirements are met by component or met by system integration”. So compensating countermeasures really count, at least insofar as they are about delegation to/integration into a system.

I've long considered that a contradiction and tried to find a way around it that isn't simply that part 4 terminology is totally independent of parts 2 and 3 terminology. There isn't one. The gap between “natively with additional compensating countermeasures” and “met […] with the assistance of compensating countermeasures” cannot be bridged linguistically.

The current draft of -4-2 (and only this part) thankfully renames “compensating countermeasures” to “supporting measures”, breaking the direct correspondence and making it clear that the concepts are similar in spirit, but different in their practical implications.

# Met by system integration

This term already came up in the compensating countermeasures part, but the weird thing about this phrase itself is how it is only introduced in -6-2, the evaluators' part. There is not a single mention in -4-2, although -4-2 obviously talks in various wordings about “integrate into a system” and “rely on a system”. I would have expected -4-2 and -6-2 to be more congruent in terminology.

I haven't seen a draft for -6-2, but I'd expect it to switch from “met by system integration” to the new “supporting measures” wording, as well.

# Trust boundary

Trust boundary is a term that has been in use by the threat modeling community for years as an element in a data flow diagram (alongside processes, external entities, data stores and flows). Flows crossing a trust boundary especially need to be scrutinized for security implications. This is also what prEN 50742 C.7.1 understands as trust boundaries.

But IEC 62443 also uses both this term and another closely related term, in two senses: it mentions trust boundaries in -4-1 in the threat modeling chapter (-4-1 6.3), but also talks in -1-1 about boundaries of zones (-1-1 5.9.1) and their crossing by trusted conduits (-1-1 5.10). Trust and boundary equals trust boundary… in practice this often seems to be called “trust zone” by security consultants indeed. This is also given some license by -1-1 5.9.1: “Zones may be considered to be trusted or untrusted.”

It's not quite a usurpation of the term, because it is still two different terms, and you obviously can threat model on a system's high-level architectural view. But the danger of conflating the boundary of a (security) zone derived from the zone and conduit requirements in -3-2 with a trust boundary within a component's firmware, for example, is real, and I have seen it happen too often. It simply invites people to claim that the whole electric cabinet is a “trust zone” and therefore we can simply trust every component in there and don't need any controls (false!). And so threat modeling only needs to concern itself with that high-level view of -3-2 zones (also false!).

By the way, “trust zone” is a security mechanism in ARM processors. Why is everyone around me using that term as kind of dual to trust boundaries (everything surrounded by trust boundaries is a trust zone)? Is that really common or just my environment?

The draft of -1-1 renames trust boundary to security zone boundary. Trust boundary remains in the -4-1 for the threat modeling use. Thus, both concepts are linguistically clearly separated.

# Essential function

This is the one I'm struggling most with today. And it doesn't help that discussions invariably confuse essential function with “the basic function of our product” (what the customer is buying the product for). In my experience it is difficult to get the point across that “essential function” is jargon, a normative term of art with a definition and several requirements around it, not just a colloquial phrase to be filled what's coming to mind first.

My big question: are all or most components expected to have essential functions? Or are essential functions a rare species? Since I'm mostly developing safety-related products, that question is moot (-4-2 3.1.20), but for automation products without safety functions or special needs of high availability?

If we put safety and environmental protection aside, the remaining application of essential function is “availability for the equipment under control” (-4-2 3.1.20). We want our product to be available, of course. But is the product's basic function in need of high availability?

The draft of -1-1 calls out essential functions as “high value equipment” (giving steam turbines as an example) and products with a special need for integrity (e.g. pharmaceuticals). Although we now get an entire chapter about essential functions (8.7), it does not clear up much.

On the other hand, designing for essential functions needn't be burdensome for many components. The requirements around essential functions are basically that those unctions may not be impeded by security: the emergency stop really must work without the panicked human having to type in a password (-4-2 5.4.2, 11.2) and a few other things (-4-2 11.3.1, 11.3.2, 13.5.2). So it may not matter much in practice.

My current thinking is that essential funktions are rarer than many people believe, and many components won't have any. But I'm very uncertain about that.
