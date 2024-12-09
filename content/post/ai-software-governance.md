---
title: "AI, software, and governance"
date: 2022-12-12T18:48:06-05:00
draft: false
tags: [artificial-intelligence,machine-learning,algorithmic-decision-making,governance,software,large-language-models,sociotechnical-systems,power]
summary: In a recent article covering the FTX collapse, the New York Times described large language models (LLMs) as "an increasingly powerful breed of A.I. that can write tweets, emails and blog posts and even generate computer programs." There is a lot that we could pick apart in this definition (e.g., what makes LLMs part of a "breed", what distinguishes the ability to write an email as opposed to a blog post, etc.), but for the moment I'd like to focus on the term "A.I." (henceforth "AI"). Referring to LLMs as an example of AI is certainly not atypical. Indeed, it increasingly seems like LLMs have become one of the modern canonical examples of this concept. But why is it that we think of these systems as members of this category? And how much rhetorical work is being done by referring to LLMs as a type of "AI", as opposed to "models", "programs", "systems", or other similar categories?
---



{{< figure src="/img/ai-software-governance/image2.jpg" >}}



In a recent [article](https://www.nytimes.com/2022/12/01/technology/sam-bankman-fried-crypto-artificial-intelligence.html) covering the FTX collapse, the New York Times described large language models (LLMs) as "an increasingly powerful breed of A.I. that can write tweets, emails and blog posts and even generate computer programs." There is a lot that we could pick apart in this definition (e.g., what makes LLMs part of a "breed", what distinguishes the ability to write an email as opposed to a blog post, etc.), but for the moment I'd like to focus on the term "A.I." (henceforth "AI").


Referring to LLMs as an example of AI is certainly not atypical. Indeed, it increasingly seems like LLMs have become one of the modern canonical examples of this concept. But why is it that we think of these systems as members of this category? And how much rhetorical work is being done by referring to LLMs as a type of "AI", as opposed to "models", "programs", "systems", or other similar categories?



Although it has never been precise, the term "AI" has traditionally been used to refer to systems which could do things that once only humans could do.[^1] Classic domains include board games, robotics, email filtering, face recognition, and more recently, systems which can generate images or text, like DALL-E and GPT-3. Nevertheless, many far less sophisticated systems are also commonly grouped under the same umbrella term, including, for example, relatively simple statistical models used for risk prediction in legal and financial settings.[^2] 

Although there is some logic in grouping all of these types of things together as part of the same concept, many examples that would fit the theme are often excluded. Simple calculators likely don't count as AI for most people, even though they can carry out complicated mathematical operations. Many types of robots are considered AI, but others, such as dishwashers, typically aren't. Modern image generation systems, such as DALL-E, are almost always referred to as AI, but older ways of algorithmically creating media, such as procedural music generation, usually aren't. Most people probably *don't* 	think of internet search engines as AI, and yet these depend critically on core techniques in natural language processing.

Given this conceptual morass, the term "AI" has arguably become less and less useful, to the point that we would now be better served, in many contexts, by thinking much more broadly in terms of "software" (with software that is tied to specific hardware, as in robotics, being a special case). That is not to say that certain types of AI systems do not deserve special consideration, but rather that most of the concerns that arise from what gets called "AI" also apply to a much broader set of computational systems. Moreover, the most important risks which arise from AI systems arguably have more to do with their nature as software than anything to do with their "intelligence".

A key reason that all of this matters is that automated decision making, AI, and software more generally, are becoming increasingly inseparable from [governance](https://www.theregreview.org/2022/07/07/jacobs-mulligan-the-hidden-governance-in-ai/). This includes not just questions about how to regulate technology, but the fact that the rules and structures which govern our lives are being increasingly interwoven with automation. In some cases, decision-making authority is being given completely over to software. In others, algorithms exert influence on human decision makers, who retain the ultimate authority and responsibility. In all cases, there are important questions to be asked about how such systems were created, and what kinds of effects that they are having.

Some important early examples of this were discussed by Danielle Citron in her classic article "[Technological Due Process](https://openscholarship.wustl.edu/law_lawreview/vol85/iss6/2/)". Detailing efforts to automate the administration of benefits in Colorado, Texas, and elsewhere, Citron described how programmers were tasked with translating existing administrative policy into concrete programmatic rules. Not only did they end up making outright errors, they were also effectively given the implicit authority to resolve ambiguity, in a way that sidestepped standard democratic processes. Although Citron did not refer to AI in that article, similar dynamics are at work today in machine learning-based systems that are being deployed across [many branches of government](https://ssrn.com/abstract=3551505).

Using the more general term "software" admittedly carries its own risks, as people's mental model of software may also fail to match reality in important ways. The point, however, is that there is a very strong continuity between what gets called "AI", and the kinds of calculations carried out by algorithms that are becoming increasingly ubiquitous in social systems. Recognizing this continuity helps to illuminate where risks come from, and also provides additional mental models that may be useful for thinking about their potential impacts on society.

Importantly, although "lifelong learning" is an important area of research in machine learning, the vast majority of extant AI systems are essentially just unchanging mathematical functions which carry out a specific calculation when called upon to do so.[^3] That is, they are composed of specific computational components, each of which takes in an input, performs a well-defined calculation, and returns an output.

Large language models, such as GPT-3, provide an excellent example here. When considered as a complete product, they have the ability to generate impressively coherent paragraphs of text. The way they are presented, however, tends to mask how these systems actually operate when generating text, which is by making repeated calls to a single function. That function takes an arbitrary sequence of letters, numbers and punctuation (i.e., one or more sentences, up to a certain maximum length), and returns a probability distribution over a vocabulary of possible tokens (words or word pieces) to output. One of those tokens is then randomly sampled from that distribution, and this process is repeated over and over again, each time including the newly generated token as part of the input for the next function call.

GPT-3 is clearly a case where the total effect adds up to more of the sum of its parts, but understanding how it works helps to eliminate some of the mystery. It also reminds us that, in most cases, all the decisions about what an AI system will do have already been made at the time of their deployment. For GPT-3, the probability distribution that will be produced for any possible input sequence has already been determined in advance (as learned during training), and has been encoded into the function that carries out the computation. That is, we can't easily know what probability distribution the model will produce for any given input without calling the function, but whatever that output is, it has already been determined, and can always be discovered by simply running the code. (Though of course the actual output of the model in operation will vary based on which tokens are randomly sampled from the resulting distributions).

Importantly, the same holds for classification systems used for tasks like loan repayment prediction. For the set of inputs that the system uses (e.g., age, income, etc.), a given system has predetermined all the decisions that it will make for all possible combinations of inputs, even if these are periodically updated. This is far different from legal systems, in which many potential cases remain ambiguous at the time of a rule's creation, and will remain so until decided through additional layers of governance.

The core element in what gets called AI these days is not something fundamentally new in terms of software architecture, but the way in which these functions are created---being trained on data, rather than manually written by programmers. This is an important development, as it means that it is now possible to create systems that are able to do (or seem to do) things better or more cheaply than would have been possible via manually writing code. However, in many cases, the details of how a function was created matter less than the fact that it exists and has been deployed, and that it effectively operationalizes a complicated set of rules which determine outcomes, rules that were probably not decided upon through normal democratic processes.[^4]

Thinking of AI as part of the general class of software provides a few advantages. First, it reminds us that we should expect AI to be fallible in the ways that most software is. It is true that many types of AI systems introduce additional and surprising failure modes---such as adversarial examples---but this is on top of the many ways in which all software can fail unexpectedly. Unlike, for example, the design of bridges, software engineering has relatively few mechanisms in place (either technical or social) to ensure that applications are produced to a high standard of reliability. In fact, the norm today is to assume that software will be flawed when it is released, with problems to be fixed as they are discovered, by a series of ongoing patches and updates.

The view of AI as software also helps to surface key reasons why we should be cautious about the widespread deployment of automation in society. As outlined by Bruce Schneier, in an excellent [report](https://www.schneier.com/academic/archives/2021/04/the-coming-ai-hackers.html) about risks from AI, many threats arise from the properties of speed, scale, and reach. In particular, the speed at which computers operate means that decisions can be carried out nearly instantaneously. Scale is even more consequential: once developed, software can be deployed extremely widely at very little cost, meaning that it can quickly and easily produce systemic effects.

Speed and scale combine to create the power of reach. That is, a piece of software can easily have a vast impact. Those who make the decisions about how software will operate (whether explicitly by writing code, or implicitly via training machine models) potentially exercise enormous power via such systems, in some cases effectively modifying the rules of the social world. Because the deployment of automated decision making systems involves redistributing decision making authority, even relatively simple software systems can change the landscape of power, potentially having a massive influence on people's lives, both now and in the future. The term "AI" arguably serves a powerful rhetorical purpose here, producing different associations and exaggerated expectations on the part of consumers and policy makers, compared to more stodgy terms like "software".

As software systems are deployed in areas like policing, the judiciary, and financial regulation, they can quickly become part of the fabric of governance, such that they cannot be easily disentangled from other parts of the broader system. The claims and promises made on behalf of AI have arguably been an important driver behind the proliferation of such systems, but the term itself can serve to obscure their nature as software.

While some machine learning systems do raise unique concerns with respect to factors like labor, bias, and maintenance, we should not lose sight of a more comprehensive shift that is taking place, in which decision making power and influence is being given over to computational systems, often with few mechanisms for accountability, transparency, participation, or redress. Mentally replacing the term "AI" with "software" provides, in many cases, a more legible model for understanding the kinds of claims and proposals that are currently being made, and can help us think through the opportunities and risks that they entail.


[^1]: Consider, for example, this [statement](http://jmc.stanford.edu/articles/dartmouth/dartmouth.pdf) from the proposal for the 1956 Dartmouth conference on AI: "An attempt will be made to find how to make machines use language, form abstractions and concepts, solve kinds of problems now reserved for humans, and improve themselves."

[^2]: Indeed, if we look at [recent coverage](https://www.nytimes.com/topic/subject/artificial-intelligence) of the topic in the Times, many articles focus on models for text and image generation (e.g., for [recipes](https://www.nytimes.com/2022/11/04/dining/ai-thanksgiving-menu.html)), others focus on predictive or diagnostic tasks, (like trying to [identify people](https://www.nytimes.com/2022/09/30/health/suicide-predict-smartphone.html) who are likely to commit suicide or [swimming pools](https://www.nytimes.com/2022/08/30/world/europe/france-taxes-pools-artificial-intelligence.html) on which people are failing to pay taxes), and a few focus on more traditional optimization tasks, such as [warehouse management and logistics](https://www.nytimes.com/2022/07/12/business/warehouse-technology-robotics.html).

[^3]: Naturally some systems will be periodically updated, which has also become the norm for software generally. To the extent that systems actually are learning on the fly, this too will be embedded within a broader software ecosystem, including how feedback is collected, etc.

[^4]: Much is made of the fact machine learning models resist the kind of simple explanations that people often want (because these functions involve higher-order interactions among many variables), but in general, people tend to underestimate how interpretable AI functions are (given that they are fully open to inspection, unless proprietary), and overestimate the reliability of traditional software (which may be practically impossible to properly verify). In all cases, the critical factor is how AI/software is connected to the social world, and the kinds of effects that it is capable of producing.