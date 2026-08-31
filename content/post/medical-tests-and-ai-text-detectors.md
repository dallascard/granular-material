---
title: "Medical Tests and AI Text Detectors"
date: 2026-08-23T23:09:57-04:00
draft: false
tags: ["large-langauge-models", "artificial-intelligence", "sociotechnical-systems", "statistics", "measurement", "evaluation", "fiction", "medicine", "communication"]
summary: "I recently listened to a podcast episode where the host and a guest tried to explain the problem with medical tests that produce a lot of false positives, such as various screenings that are used for certain types of cancer. Despite both being smart and capable people, they did an impressively bad job at this, and I suspect they left much of the audience either confused or misinformed.

Part of the problem was that they jumped immediately to using terms like sensitivity and specificity, as well as Type-I / Type-II errors, without properly defining what these mean. They also chose to frame this using a Bayesian explanation, using terms like prior and posterior, even though it's arguably simpler to explain things in frequentist terms. But part of the problem is that this is a legitimately complicated issue to explain to a general audience, especially in audio. ↳"
---


I recently listened to a podcast episode where the host and a guest tried to explain the problem with medical tests that produce a lot of false positives, such as various screenings that are used for certain types of cancer. Despite both being smart and capable people, they did an impressively bad job at this, and I suspect they left much of the audience either confused or misinformed.

Part of the problem was that they jumped immediately to using terms like sensitivity and specificity, as well as Type-I / Type-II errors, without properly defining what these mean. They also chose to frame this using a Bayesian explanation, using terms like prior and posterior, even though it's arguably simpler to explain things in frequentist terms. But part of the problem is that this is a legitimately complicated issue to explain to a general audience, especially in audio.

It's always hard to know what will work best for different people, but at least where a visual aid is possible, I feel like a confusion matrix goes a long way to explaining the basic problem. That is, imagine that there is some test we want to characterize in terms of its reliability. Imagine getting a group of people, and giving them all this test, and getting each of their test results. Now, imagine that we can somehow also get each person's true status (i.e., truly positive or truly negative for the disease we are testing for).[^1] If we have all of this, we can simply count up how many times the test is right or wrong for those who are positive and for those who are negative, and put the counts of these into a confusion matrix:

| | Predicted Positive | Predicted Negative |
| --- | :---: | :---: |
| **Actually Positive** | True positives (TP) | False negatives (FN) |
| **Actually Negative** | False positives (FP)| True negatives (TN) 

Even keeping things abstract, the idea that there are some number of true positives, true negatives, false negatives, and so forth, helps to make the point that these tests are not perfect, and that these specific error rates might matter. Depending on what these values are for a given situation, the raw numbers themselves can make the point quite clearly. Moreover, it can easily show how the rate of false positives (FP) may actually be quite high, especially relative to true positives (TP), even if it is small relative to true negatives (TN).

For example, hypothetical results in some population for a given test might follow a pattern like this:

| | Predicted Positive | Predicted Negative |
| --- | :---: | :---: |
| **Actually Positive** | 100 (TP) | 10 (FN) |
| **Actually Negative** | 1,000 (FP) | 100,000 (TN) |

In some ways this looks good: For those who actually have the disease (the "Actually Positive" row), the test only provides 10 false negatives for every 100 accurate reads (1:10). Similarly, for those who are actually negative (the bottom row), the test only produces 1,000 false positives for every 100,000 correct reads (1:100). Unfortunately, applying this test in practice might still cause problems: If we look only at those cases where the test is positive (the "Predicted positive" column), for every 100 predicted positives that are correct (TP), there are 1,000 that are wrong (FP), meaning that a positive result is much more likely to be wrong than right, by a factor of 10. The problem of course is that there is a low incidence of actually positive people in this sample (only around 110 actually positive cases per ~100,000 people), meaning that the false positives swamp the true positives. 

Even with a visual aid, part of the difficulty in explaining this paradox is a result of how these tests are normally characterized. There are many statistics we can compute from the table (e.g., accuracy, sensitivity, specificity, etc.), but all discard some information, and may individually be misleading. For example, the *accuracy* of the test in the confusion matrix above (how often the test is correct) is over 99%, but this is almost entirely due to the large number of actual negatives that are easy to detect.

As in the episode I heard, tests may frequently be described in terms of sensitivity (TP / (TP + FN)) and specificity (TN / (FP + TN)). That is, how likely is the test to be correct, given someone is in fact either truly positive (e.g., has cancer) or truly negative? Unfortunately, those numbers aren't really what we want to know. Because we don't know whether the person being tested is actually positive or negative, (that is the point of the test after all!),  we can't easily make use of those statistics.

Rather, what we probably most want to know is the False Discovery Rate (FDR = FP / (TP + FP)).  That is, if a test comes back positive, how likely is it to be wrong? The situation mentioned above, where false positives (FP) are small relative to true negatives (TN), but large relative to true positives (TP), would imply a high FDR (which means a prediction of positive is not reliable), even though specificity is also high. This is sadly a common combination when a condition is rare.

Unfortunately, there's a reason that the FDR statistic is typically not available, which is that the FDR will depend greatly on the population that is being tested. If you give the test to a group of people with a high incidence of the disease (or whatever it is that the test is for), then that changes the expected balance of truly positives and negative people.[^2] As such, tests that come back positive may be more likely to be correct than in some other population. To put it differently, using the test on different populations would result in different values of the confusion matrix, which would translate into different rates of false discovery (FDR).

By contrast, the argument is often made that sensitivity and specificity are stable, meaning they will not vary across populations. But crucially, note that this isn't actually true! Except for very simple situations, the nature of both an actually positive and an actually negative sample could vary quite dramatically with the population. For actual negatives especially, there might be many ways to be negative, with higher or lower likelihood of looking positive, according to some test. Similarly, some positives may be easier or harder for a test to recognize.[^3]

Taking this to the extreme, what we really care about is whether we can trust the test on one particular person, regardless of if they are positive or negative. Since we can't usefully get that information (or else we wouldn't need the test), we typically fall back to look at how the test performs across a group of people, and using those sample statistics as a proxy measure of test reliability. Critically, however, this assumes that the sample population used is a good proxy for the person in question.

Essentially, it's the same problem no matter how we describe things. In order to meaningfully characterize a test, we need to know who the reference population is. Even though we would like to know how well it will work for our own individual case, the best we can typically do is put ourselves into some sort of generic reference population, perhaps something like people of similar age or other demographic characteristics, and hope they are a reasonable proxy for our own situation. More commonly of course, such specific numbers are not available at all, and we just need to hope we are similar enough to a population for which information is available.

If you read the title of this post, it may not surprise you to learn that the same logic governing medical tests also applies to so-called AI text detectors, like [Pangram](https://www.pangram.com/). In recent months, it feels like this subject has been constantly in the news, including within the context of [peer review](https://gregdurrett.github.io/colm2026-blog/ai-papers.html) for conferences, journalists and  [novelists accused of using AI-generated text](https://www.theguardian.com/books/2026/jul/31/crime-novel-deal-collapses-questions-ai-jerry-falade-call-me-ill-hide-the-body), claims about  [members of Congress](https://nicholasdecker.substack.com/p/who-uses-ai-in-congress), and many other cases.

In principle, the setup is fairly simple. If you build a tool to guess whether a piece of text was written by a a large language model (LLM) or not, and give it a bunch of writing samples that you sourced from people and chatbots, respectively, you can easily compute a confusion matrix, and thereby estimate the sensitivity, specificity, and so forth. Some systems for this, such as Pangram, have claimed extremely impressive performance on this task, on the order of [99.9% accuracy](https://arxiv.org/abs/2402.14873).

If the part about medical tests above was not clear, hopefully in case of AI text detection it's all the more obvious that these numbers are not particularly meaningful outside of a particular context.[^4] As above, what we really want is something like false discovery rate, to be able to know how much we can trust a test that comes back with a prediction of positive (i.e., that the text was written by an LLM). Also as above, however, the reliability of the AI-text detector will vary dramatically depending on exactly what the set of documents being tested is.

If you're unconvinced, simply imagine sampling text from different places, and/or writing your own text. Most likely, you have some sense of what Claude and ChatGPT "sound like", and could do a passable job mimicking their style. Compare that to text where you just randomly write down words as they pop into your mind. These are potentially harder and easier cases of actual negatives, and most likely will produce different error rates. 

Similarly, if any LLM output counts as an actually positive sample, it seems likely that how you prompt the model could have an effect on whether or not an AI text detector thinks it was written by LLMs. Contrary to what is often implicitly assumed, there is no "natural" distribution of model outputs, since what prompts people use can vary widely.

Moreover, this case also hopefully makes it clear that, whereas one's status of having a disease or not may be a simple binary outcome, whether text was "written by AI" is not so simple. The most obviously tricky cases are those where you take text generated by a model, but then proceed to edit it. Does that count, and if so, how much editing is allowed? Similarly, what about the fact that we're now all being influenced in our style by the output of models. What about when someone tries to intentionally mimic the style of their favourite LLM, or gives a model text they wrote and ask it to simplify the writing?

For many cases, of course, this may be relatively moot. If you are looking for evidence that writing with the help of AI has entered some domain in any way at all, such as [fiction](https://www.nytimes.com/2023/02/23/technology/clarkesworld-submissions-ai-sci-fi.html), AI text detectors will almost certainly provide compelling evidence, as long as you don't care too much about getting precise estimates. But when it comes to evaluating student work, for example, the number you are probably looking for---how likely is a positive result to be correct or incorrect---is unfortunately not something that can be computed and then simply ported across domains.

According to a friend of mine who is a doctor, there's a rule in medicine that you should never order a test unless you know how you would make use of that information (i.e., what action you would take as a result). In many cases, the subsequent actions available (such as ordering a more invasive test) will carry additional risks, and so you want to avoid producing information that either wouldn't change how you would act, or is more likely to lead to incidental harm. In many cases, the same principle could apply to the notion of trying to check if text was written by an LLM, especially in light of the fact that their reliability varies with context, and cannot easily be known, except without additional evaluation.

In other words, if you're considering using an AI-text detector, it's worth thinking about exactly what question you're trying to answer, what level of reliability you would consider adequate, how you will evaluate that, and what actions you would take as a result of the test.



[^1]: In some cases, for example, there might be a more reliable test that is also more invasive or harmful, such that there is some greater cost to using it.

[^2]: This is where the Bayesian formulation would describe things in terms of a prior probability, and updating our degree of belief following the test, but note that this isn't actually needed to make sense of the basic problem.

[^3]: To be fair, it is plausible that sensitivity and specificity might vary less with the population being tested than other statistics like false discovery rate, at least for some tests or conditions, but it seems highly misleading to say that they generically do not vary. 

[^4]: In the case of the original [Pangram report](https://arxiv.org/abs/2402.14873), the performance numbers are based on publicly-available test set of 928 positive examples (generated by various LLMs) and 1048 negative examples (written by humans), including "hand-picked examples from the internet". There is no particular reason to doubt the claims about performance on this test set, but it's also hard to know whether the evaluation was done with sufficient rigor, or whether these examples are representative of typical use cases.


