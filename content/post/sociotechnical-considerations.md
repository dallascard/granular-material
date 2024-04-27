---
title: "Sociotechnical Considerations"
date: 2024-04-27T13:42:01-04:00
draft: false
tags: ["artificial-intelligence", "persuasion", "manipulation", "ezra-klein", "dario-amodei",  "anthropic", "natasha-dow-schüll", "addiction-by-design", "books", "podcasts", "sociotechnical-systems", "science"]
---

A whole genre of podcasts seems to have emerged recently, taking the shape of interviews with CEOs of AI companies, or similar. Although I have not listened to many of these, they mostly seem to be pretty abysmal, both because of the amount of hype they involve, and due to the lack of meaningful specifics.

That being said, of the ones I've heard, the recent [interview with Dario Amodei of Anthropic on the Ezra Klein Show](https://www.nytimes.com/2024/04/12/podcasts/transcript-ezra-klein-interviews-dario-amodei.html) seems to me to be vastly better than the average. In part, this is because Klein is a smart, curious, and well informed interviewer, who asks a lot of the right questions, and pushes for details when responses get too mushy. In this case, it also helps that Amodei seems much more straightforwardly honest about limitations than most spokespeople in similar positions.

Klein and Amodei cover a lot of territory, and it is well worth listening to the whole thing, but here I just want to comment on a couple of the points they cover early on. Although there is infinite room for speculation and disagreement, these two points, in my opinion, provide nice examples of the failure of many of those predicting the most dramatic advances in AI to think carefully about the sociotechnical aspects of these questions.

The first point has to do with the idea that more advanced AI[^1] might be able to speed up processes of scientific discovery, such as in drug development.

In response, Klein makes the point that drug discovery is currently very slow, despite being very well funded, in part due to the material processes that currently need to take place for a drug to be approved, specifically things like clinical trials in mice and monkeys and people. How, he asks, will AI be able to speed that up?

Amodei's response is, I think, telling. He basically says "I don't know, I'm not an expert". (Which might cause one to wonder how much confidence we should place in his prognostications). When forced to come up with something specific, he ends up suggesting maybe AI can speed up the process of signing people up for clinical trials. Later on, he expands on this a bit, pointing to things like "doing clinical trials for cheaper, automating the sign-up process, seeing who is eligible for clinical trials, doing a better job discovering things".

Interestingly, he does not say that AI will be able to so perfectly model human biology that we won't need clinical trials, or anything along those lines, although he does mention that other companies are working on this (digital twins and simulating clinical trials). More than anything, he just ends up at "they [the AI systems] will come up with solutions that we don't have yet".

For a bit more context, here's the core of their exchange on this first point:

Klein:
> The drug discovery world, a lot of what makes it slow and cumbersome and difficult, is the need to be — you get a candidate compound. You got to test it in mice and then you need monkeys. And you need humans, and you need a lot of money for that. And there’s a lot that has to happen, and there’s so many disappointments. But so many of the disappointments happen in the real world. And it isn’t clear to me how A.I. gets you a lot more, say, human subjects to inject candidate drugs into. So, what parts of it seem, in the next 5 or 10 years, like they could actually be significantly sped up? When you imagine this world where it’s gone three times as fast, what part of it is actually going three times as fast? And how did we get there?

Amodei:
> I think we’re really going to see progress when the A.I.‘s are also thinking about the problem of how to sign up the humans for the clinical trials. And I think this is a general principle for how will A.I. be used. I think of like, when will we get to the point where the A.I. has the same sensors and actuators and interfaces that a human does, at least the virtual ones, maybe the physical ones. But when the A.I. can think through the whole process, maybe they’ll come up with solutions that we don’t have yet. In many cases, there are companies that work on digital twins or simulating clinical trials or various things. And again, maybe there are clever ideas in there that allow us to do more with less patience. I mean, I’m not an expert in this area, so possible the specific things that I’m saying don’t make any sense. But hopefully, it’s clear what I’m gesturing at.

The second point, which they pivot to right after, is on the topic of persuasion.

Klein asks Amodei about [Anthropic's recent blog post on persuasion](https://www.anthropic.com/news/measuring-model-persuasiveness). Despite this being a topic where it feels like the answer could have involved a significant amount of hype, Amodei is actually fairly circumspect: "what we found is that the largest version of our model is almost as good as the set of humans we hired at changing people’s minds. This is comparing to a set of humans we hired, not necessarily experts, and for one very kind of constrained laboratory task."

Klein then pushes a bit further, pointing out that they only tested a zero-shot setup, but that in the real world, it will be easy to overcome this limitation. Here's Klein:

> This is not going to be true for A.I. We’re going to — you’re going to — somebody’s going to feed it a bunch of microtargeting data about people, their Google search history, whatever it might be. Then it’s going to set the A.I. loose, and the A.I. is going to go back and forth, over and over again, intuiting what it is that the person finds persuasive, what kinds of characters the A.I. needs to adopt to persuade it, and taking as long as it needs to, and is going to be able to do that at scale for functionally as many people as you might want to do it for.

This is worth commenting on, because it seems to be something of a staple of a lot of discourse on AI safety---the idea that advanced AI systems will be so persuasive, that they will basically be able to convince people to do anything. If this were true, the scaremongers point out, then advanced AI systems won't face any significant physical limitations, as they can simply convince a person to carry out a task in the real world. Klein doesn't quite go that far, but it is an implicit argument you hear in many places.

The reality is, I think, more complicated. Clearly there are many cases where people can be and have been persuaded, either to change their opinion on an issue, or to carry out some action. In the most extreme cases, many people have arguably been manipulated into taking actions that are highly self-destructive in expectation, including things like going to war and betting large sums on gambling systems with transparently bad odds.

Again, interestingly, Amodei helpfully points out that this is not a simple one-sided escalation. First, people inevitably end up adapting to technological developments. Whereas early forms of advertising were once highly persuasive, people learn to ignore them and are less persuaded over time. Second, the dynamic will inevitably be something more like an arms race; technological or infrastructural defenses will be developed, including using AI. Here's Amodei's response, a few paragraphs later:

> So where my mind goes as a defense to this, is, is there some way that we can use A.I. systems to strengthen or fortify people’s skepticism and reasoning faculties, right? Can we help people use A.I. to help people do a better job navigating a world that’s kind of suffused with A.I. persuasion? It reminds me a little bit of, at every technological stage in the internet, right, there’s a new kind of scam or there’s a new kind of clickbait, and there’s a period where people are just incredibly susceptible to it. And then, some people remain susceptible, but others develop an immune system. And so, as A.I. kind of supercharges the scum on the pond, can we somehow also use A.I. to strengthen the defenses?

This is a topic I want to come back to in the future, but for the moment, I'll just end by saying that everytime the issue of the potential persuasiveness of AI comes up, my mind immediately goes back to a fantastic book by Natasha Dow Schüll, called "[Addiction by Design: Machine Gambling in Las Vegas](https://press.princeton.edu/books/paperback/9780691160887/addiction-by-design)". Schüll is an anthropologist, and the book is basically a deep dive ethnography of the gambling industry, written in 2012. In researching the book, she spent considerable time with both the people who gamble (primarily using slot machines) and the designers of those machines, and along the way, providing numerous heart-breaking vignettes of unfortunate people essentially destroying their lives through their addiction to gambling.

There is a lot to be said about this book, but the primary point for me in this context is just how simple these machines are. The designers are obviously somewhat clever, both in terms of creating an unpredictable reward structure, and in using mildly deceptive techniques, like making it appear that the odds are better than they actually are. Obviously the design of these machines could be pushed much farther in terms of addictiveness, but in many cases designers are prohibited from doing so because of how the industry is regulated. In the end, however, it almost doesn't matter. Despite the simplicity of these systems, there will be some small number of people who will simply sit there and pour whatever money they have into them, until it is all gone.

Addiction by Design is obviously an incredibly sad book, but it is an important one, I think, for anyone interested in the topic of persuasion or manipulation. On the one hand, it provides compelling case studies of just how easily some people can be manipulated into self-destructive behaviour, using very simple means. At the same time, the fact that most people are easily able to ignore theses systems (or at least redirect that behaviour into something less harmful, like TV or video games), suggests that a large part of this is some sort of selection effect, rather than an inherent addictiveness property of the machines themselves. Perhaps it is true, as some people suggest, that AI will become so addictive that far more people will be simply unable to resist it. But for the moment, I remain skeptical.


[^1]: Amodei favours the term artificial superintelligence (ASI); the quotations come from the transcript provided by the New York Times, which insists on punctuating AI as "A.I."


