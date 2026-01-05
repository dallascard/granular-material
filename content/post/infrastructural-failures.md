---
title: "Infrastructural Failures"
date: 2026-01-04T19:36:11-05:00
draft: flase
summary: "Susan Leigh Star has noted that infrastructure is often invisible until it breaks. We all know that we are ensconced in a whole network of pipes and wires that provide water, electricity, and other systems upon which we depend, but at least for those of us lucky enough to have reliable service, it is easy to take it for granted that these things just work, until they don't. Given the increasing interdependence of software and infrastructure, the recent Waymo failure in Los Angeles provided a useful reminder of the types of risks inherent in these kinds of distributed-but-centralized technical systems."
tags: ['artificial-intelligence', 'infrastructure', 'technology', 'sociotechnical-systems', 'software', 'instability', 'governance', 'crowdstrike', 'waymo']

---

Susan Leigh Star has noted that infrastructure is often invisible until it breaks.[^1] We all know that we are ensconced in a whole network of pipes and wires that provide water, electricity, and other systems upon which we depend, but at least for those of us lucky enough to have reliable service, it is easy to take it for granted that these things just work, until they don't.

Several months ago, I had the chance to take a Waymo in Los Angeles, and for me, it was one of the most magical technological experiences I've had in quite a long time, comparable perhaps to something like looking out the window of an airplane, or many people's first encounter with ChatGPT. We've all been hearing so much about self driving cars for so long (typically forecast as being being just five years away), and my first experience with Tesla's autopilot was so hilariously disappointing, that it was something of a shock to discover that self-driving taxis were suddenly a reality, at least in California.[^2]

Even though service is still pretty limited, only operating within fairly narrow geographical regions, and---at least while I was there---only operating on city streets (as opposed to highways), the self-driving part works phenomenally well where they do operate. The integration of detailed maps, multimodal input from LiDAR and other sensors, and impressive machine learning made for an experience that felt as good as or better than riding with a human driver. I honestly felt at times like the Waymo was driving more aggressively than I would have been, while still feeling very safe and in control.

Sadly, the tech is far from perfect (naturally), and shortly before Chrstmas, a widespread blackout led to [Waymo's simply stopping](https://www.nytimes.com/2025/12/22/us/waymo-san-francisco-power-earthquake.html)  where they were, creating traffic chaos and frustration. It's apparently unclear whether this was a failure of automation, or if someone made the decision to shut them all down. While this is certainly a better failure mode than high speed crashes, it is a stark reminder of the types of risks inherent in these kinds of distributed-but-centralized technical systems.[^3]

Given that they are still only in a handful of markets, it's perhaps a bit of a stretch to call Waymo "infrastructure", but my experience of them was so impressive that it was easy to begin to think of them that way. Indeed, the whole design of the app is clearly intended to mirror ride hailing services like Lyft and Uber, which I think it's fair to say already do qualify as infrastructure today, at least in some sense of that term. In fact, because there is no individual human driver, Waymos in some ways feel all the more *infrastructural*, and not so different from various other forms of automated transport (e.g., driverless trains). Moreover, it is easy to imagine how self-driving cars might remake a city, something like the ways electric lighting did, and the autonomous nature of them makes the technical layer feel remarkably invisible (as long as it is working).

Hearing about this Waymo failure, I was also reminded of the [CrowdStrike incident](https://en.wikipedia.org/wiki/2024_CrowdStrike-related_IT_outages) from 2024, where a faulty update to security software with access to the Windows kernel led to around 8.5 million computers crashing and failing to boot properly. For me, that incident still remains one of the most salient examples of the risks inherent in widespread computational infrastructure. That case was especially ironic, given that it had an impact similar to a significant cyberattack, including billions of dollars of damage, the exact kind of thing that the CrowdStrike software was nominally intended to prevent!

In the case of Waymo, the initiative incident was apparently a blackout, which is of course a failure of one of the most canonical infrastructural systems---the electricity grid. It's fair to say that we very much take electricity for granted today, and yet, we also take it for granted that failures will inevitably happen.[^4] They are perhaps just frequent enough that we are (hopefully) at least somewhat prepared for them, and have expectations about how long they will typically last. They are also usually concentrated in a geographical area, although there have obviously also been some much more dramatic wide-scale outages throughout history.

Waymos, by contrast, exhibit a combination of newness (therefore unfamiliarity), distributedness (meaning they could be anywhere), and homogenous centralized programming (meaning they might basically all fail simultaneously). The combination of these seems primed to make for an incident that could catch many people off guard, and cause disruptions throughout the city. The fact that some people are not happy about their city being used as a testing ground for self-driving cars obviously adds to the frustration with the stalled cars suddenly creating chaos.

On top of that, there is also the fact that self-driving cars are part of the broader umbrella of AI, which perhaps adds something to the emotional stakes. Even though it is by now a familiar experience, it can still be a shock to remember just how brittle AI systems can be, even if they are capable of such impressive automated decision making. Although it is perhaps most surprising in the case of AI, it's important to remember that similar risks are ultimately inherent in many types of computational systems. 

Sadly it does not feel like we have learned the lessons of the CrowdStrike incident, presumably in part because we have so little choice in the matter. We technically have a choice about which operating systems we use, but the choices are fairly limited, and will be heavily constrained in various types of corporate environments. By their very nature, many infrastructural risks and failures will be governed much more by policy than by indivdual choices. Neverthless, especially with many newly emerging layers of software infrastructure, we would be well served to think more about the risks that are created by these sorts of systems, both commercial and governmental, and how we might mitigate them.


[^1]: See "The Ethnography of Infrastructure", by Susan Leigh Star, in *American Behavioral Scientist* 43(3), 1999.

[^2]: Waymo notes that their cars are supported by a backup "fleet support", which can provide guidance (likely waypointing) in difficult situations, but that the cars otherwise operate fully autonomously.

[^3]: Bruce Schneier has an excellent report I've [linked to before](https://dallascard.github.io/granular-material/post/ai-software-governance/), on the way risks emerge from the combination of speed and scale that is inherent in most computational systems. See [The Coming AI Hackers](https://www.schneier.com/wp-content/uploads/2021/04/The-Coming-AI-Hackers.pdf), by Bruce Schneier, 2021.

[^4]: The power outage reportedly affected 130,000 people who get power from Pacific Gas & Electric.



