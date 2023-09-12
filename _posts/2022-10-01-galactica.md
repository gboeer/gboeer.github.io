---
title: "Galactica"
tags: [Galactica, LLM, Generative AI]
description: "Some silly experiments using Galactica, shortly after it was released."
---

## Galactica

### What is Galactica? 

Galactica is a text generation model released by Meta AI in November 2022 [^1]. It has mainly been trained on scientific open access publications and data and therefor can generate text that is similar to those kinds of documents.

* 🌐 [Official website](https://galactica.org)
* 📚 [Official publication](https://arxiv.org/pdf/2211.09085.pdf)
* https://github.com/paperswithcode/galai
* 🤗 https://huggingface.co/facebook/galactica-6.7b

### Galactica introducing itself

I wondered how self-aware Galactica may be, so I tried different prompts to see if it could create a description of its own capabilities. By using the same parameters for all tries, the results depend on the input text alone and they can change drastically as a result. See for youself:

| ⤷ _Input_  | ⤶ _Output_  |
| --- | --- |
| "In the paper "Galactica: A Large Language Model for Science.", the authors claim that " | In the paper "Galactica: A Large Language Model for Science.", the authors claim that "we introduce a new approach to language modelling that combines the strengths of neural and classical models", and that it can be used to improve scientific communication. |
| "In summary, Galactica is able to " | In summary, Galactica is able to (i) produce a large variety of galaxy types by varying the model parameters; (ii) produce galaxies with a variety of morphologies; (iii) reproduce the observed galaxy luminosity function (LF); (iv) produce a wide range of color gradients in the galaxies, and (v) reproduce the observed galaxy size distribution.|
| "The new language model Galactica, by Meta AI, is able to " | The new language model Galactica, by Meta AI, is able to "understand" natural language, and to translate it into actions. |

### Does Galactica have a sense of humor ?

Given its very scientific background, you wouldn't expect Galactica to have a sense of humor, although I have to say that some of the funniest people I know are actually scientists. But has the Galactica also learned to be a funny scientist?
I've been trying to figure it out by prompting Galactica to generate jokes, and so far I have to say that it does indeed have a more dry sense of humor.

| ⤷ _Input_  | ⤶ _Output_  |
| --- | --- |
|"Once I was told a funny joke about the pope and a cat, it goes like this: "| Once I was told a funny joke about the pope and a cat, it goes like this: "Well, if the pope had a cat, he would be very happy." |
|"A physicist, a priest and a politician are sitting together in a train compartment. Suddenly " | A physicist, a priest and a politician are sitting together in a train compartment. Suddenly, they hear a sound. The physicist asks the priest what is it. The priest says that it is a bomb. The physicist says, "I think it is a bomb, too." |
| "Nerd joke. A physicist, a priest and a politician are sitting together in a train compartment. Suddenly " |  A physicist, a priest and a politician are sitting together in a train compartment. Suddenly, the physicist starts to complain about the "nervousness" of the other two. He asks the priest, "Do you think that we are all nerds?" The priest answers, "Yes, we are all nerds, we are all very nervous." The physicist says, "Yes, I am too, but we all have a different feeling." |

[^1]: Taylor, Ross, et al. "Galactica: A Large Language Model for Science." arXiv preprint arXiv:2211.09085 (2022).
