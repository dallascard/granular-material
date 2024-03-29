---
title: "Confidence in Science"
date: 2022-03-06T09:20:14-05:00
draft: false
tags: ["machine-learning", "reproducibility", "invisible-colleges", "science"]
---

I’ve been thinking recently about the role of confidence in science, and how long beliefs can persist simply because everyone else seems to believe them. Coincidentally, Andrew Gelman [posted](https://statmodeling.stat.columbia.edu/2022/03/04/biology-as-a-cumulative-science-and-the-relevance-of-this-idea-to-replication/) about this two days ago, responding to comments from a biologist about how the replication crisis had not been a major problem in biology. Her argument was that this was because biology is a "cumulative science". By this she meant that when something important gets published, it is often the kind of discovery that people want to use immediately. If the original claims was wrong, people will quickly figure it out.

This is an interesting perspective, but I'm also somewhat skeptical. First, biology is a huge field. In terms of publications, biology arguably represents the majority of current science. I would guess that within that vast space of papers, there are many results which are not important enough that anyone wants to use them immediately. Second, biologists sometimes go so far as to record videos of how they carried out certain experimental processes. This represents an admirable contribution to replicability, but suggests that the details may matter a lot, and this suggests that replication will be challenging.

Third, the idea of a cumulative science applies to all fields, at least to some extent. In part the problem with psychology is that it had so many findings that had a certain pop appeal (Gelman cites the famous "elderly-priming-slow-walking study"), but no direct utility within the field itself. Perhaps biology has avoided this in part because many of the findings are so hard for outsiders to understand?

If there's one field where we might expect this sort of replication-via-use to be discovered, it seems like machine learning would be way up there. There is a huge number of people monitoring for new developments and hoping to use them to get an additional edge in research and business. And yet, this doesn't really seem to happen, at least not in a coordinated way.

My guess is that the problem is that most of the people testing out these findings are not so much a part of the formal scientific community as most authors of papers. As such, they are less incentivized to report any discrepancies they find, at least not in a formal paper. We do find some [papers](https://proceedings.neurips.cc/paper/2019/file/c429429bf1f2af051f2021dc92a8ebea-Paper.pdf) like this, but the field doesn't necessarily place sufficient value on them. I suspect that many people do develop a strong sense about which claims are not reliable, but that most of this knowledge remains as folk wisdom.

Either way, this discussion does illustrate how important it is to have a community of people all actively trying to replicate experiments and share their own findings. This is a key part of David Wootton’s argument in _The Invention of Science_. He writes:

> "There can be no replication if there is not some form of publication, or at least, communication. Two scientists discovered the law governing the acceleration of falling bodies at around the same time -- Harriot and Galileo. Harriot kept his results to himself; Galileo finally published in 1632, some decades after he had made his discovery. ... Soon all sorts of people were dropping objects off tall buildings and getting rather varying results (it is actually much harder than one might think to drop two objects simultaneously, and very difficult to measure how far apart they are when the first one hits the ground)."

He describes a similar process unfolding in the 1640s for experiments with water columns and air pumps, noting that "Torricelli's barometer represents the first piece of experimental apparatus that became widely available", and that "this was the point at which science became a "collaborative and competitive process".

Why did experimental science take off so strongly at this time? It remains something of a mystery, but no doubt there were many causal factors. Wootton points to the impact of printing (though personal correspondence remained a fundamental part of this process), the creation of accessible an experimental apparatus, the existence of claims that seemed to undermine established and accepted knowledge (from Aristotle), and events like the voyage of Columbus leading people to have greater confidence that new knowledge might be possible.

I suspect that for machine learning we are in something of a golden age of raw replication, with huge numbers of people testing things out for themselves. What is lacking, perhaps, is the correspondence and publication network for people to share this work. Or rather, it does exist, but it is as fractured as the early invisible colleges, distributed across emails, blogs, preprints, [workshops](https://ml-retrospectives.github.io/), and various replication sites.

On the other hand, perhaps things move so quickly that it matters less to sort out the validity of every claim, as many of them quickly become more or less irrelevant to practical application. Most likely it is a kind of organic process, in which the widespread adoption of models like transformers reveals their value, more so than the papers replicating particular experiments to validate specific findings.


