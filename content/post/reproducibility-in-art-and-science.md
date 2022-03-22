---
title: "Reproducibility in Art and Science"
date: 2017-06-05T20:43:20-05:00
draft: false
tags: ['reproducibility', 'art', 'science', 'digital', 'preservation', 'open-science']
medium: https://dallascard.medium.com/reproducibility-in-art-and-science-fd5b7b10fd01
---

Marking the beginning of a new [partnership](http://rhizome.org/editorial/2017/may/30/rhizome-google-partnership/) between Rhizome and the Google Cultural Institute, the Rhizome blog recently published a [conversation](http://rhizome.org/editorial/2017/may/30/preservation-by-accident-is-not-a-plan/) between Dragan Espenschied, Rhizome’s preservation director, and Vint Cerf, Google’s Chief Internet Evangelist. In addition to bringing together two people with among the coolest job titles ever, it got me thinking about some similarities between art and science when it comes to the issue of reproduction.

The main thrust of the conversation is about the difficulty of preserving internet art. In particular, works such as [The Web Stalker](https://anthology.rhizome.org/the-web-stalker) were often made in a particular context, intended to be performances of a sort, and which depended on the existence of a certain technical infrastructure, including a particular operating system, a particular input device, an internet connection, and accompanying protocols. Part of the conversation relates to the fact that it’s actually very difficult to maintain or recreate every single thing that is required in order for a modern viewer to have the exact same experience as when it was first created. Nevertheless, Dragan argues, there is still value in preserving part of the experience.

In terms of actual mechanisms, we now have several options for preserving internet art. First, there is emulation, such that we can effectively run programs on hardware which no longer exists. Second, when the original source code is available it may be possible to port it to a modern language. On the other hand, it is not hard to find cases where the source code by itself is insufficient (such as where a bug was exploited as a feature). Third, (though Dragan demurs at this), we can try to give people the tools to make things in a way that makes them easy to preserve in a stable form.

In my mind, these ideas are mirrored nicely in current efforts to promote and enable reproducible science. As has been widely popularized recently, there is something of a [crisis](https://www.nature.com/news/1-500-scientists-lift-the-lid-on-reproducibility-1.19970) [of](https://osf.io/ezcuj/) [reproducibility](http://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.0020124) happening in certain fields of science at the moment, particularly psychology. (See Andrew Gelman on [why psychology](http://andrewgelman.com/2016/09/22/why-is-the-scientific-replication-crisis-centered-on-psychology/)). More broadly, there is a push to make things as reproducible as possible as a best practice, especially in computer science.

Of course, like trying to recreate the viewing experience of a piece of internet art from the 1990s, trying to make science completely reproducible can be surprisingly difficult. The least promising situation is trying to rely on the methodological description given in a scientific paper; while intended to be comprehensive, such descriptions are often notoriously silent on some critical detail. Practically speaking, it is just very difficult to succinctly but completely describe everything of relevance that was done.

At a higher level of sophistication, it is becoming increasingly common to release source code to accompany papers, which (at least in theory), allows for reproducing the published results. This a huge step forward, but unfortunately doesn’t solve all problems. The biggest remaining hurdle is often data, which might not be publicly available, or even sharable without raising privacy concerns. And even when data is available, challenges remain, from algorithms which inherently involve a certain amount of randomness, to hacky research code which cannot be easily installed on your particular operating system.

The final step is perhaps to actually package everything in a way that is easy for anyone to work with and which will run anywhere. This can be challenging, but there is lots of good [advice](https://ropensci.github.io/reproducibility-guide/sections/introduction/) out there, and tools such as [Jupyter notebook](https://jakevdp.github.io/blog/2017/03/03/reproducible-data-analysis-in-jupyter/) make this easier than ever before.

Problems of reproducibility and preservation will always remain of course, but striving to avoid them is an excellent goal. If having people run their own study and use your fully-automated analysis pipeline is an ideal in research, it is perhaps akin to recreating the experience of a work of digital art through preservation and emulation. The context will inevitably be somewhat different, but this sort of replication has the potential to lead to fruitful follow-on developments, in both art and science. As Dragan suggests, it is better to preserve something rather than nothing, and there are thankfully now plenty of tools out there to make this as easy as possible, and communities such as Rhizome and the Google Cultural Institute that help inspire, organize, and direct these efforts.
