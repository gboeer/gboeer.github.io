## Galactica Playground

### What is Galactica? 

Galactica is a text generation model released by Meta AI in November 2022 [^1]. It has mainly been trained on scientific open access publications and data and therefor can generate text that is similar to those kinds of documents.

* 🌐 [Official website](https://galactica.org)
* 📚 [Official publication](https://arxiv.org/pdf/2211.09085.pdf)
* :octocat: https://github.com/paperswithcode/galai
* 🤗 https://huggingface.co/facebook/galactica-6.7b

### Galactica introducing itself

I wondered how self-aware Galactica could be, so I tried different prompts to see if it could create a description of its own capabilities. By using the same parameters for all tries, the results depend on the input text alone and they can change drastically as a result. See for youself:

| ⤷ _Input_  | ⤶ _Output_  |
| --- | --- |
| "In the paper "Galactica: A Large Language Model for Science.", the authors claim that " | In the paper "Galactica: A Large Language Model for Science.", the authors claim that "we introduce a new approach to language modelling that combines the strengths of neural and classical models", and that it can be used to improve scientific communication. |
| "In summary, Galactica is able to " | In summary, Galactica is able to (i) produce a large variety of galaxy types by varying the model parameters; (ii) produce galaxies with a variety of morphologies; (iii) reproduce the observed galaxy luminosity function (LF); (iv) produce a wide range of color gradients in the galaxies, and (v) reproduce the observed galaxy size distribution.|
| "The new language model Galactica, by Meta AI, is able to " | The new language model Galactica, by Meta AI, is able to "understand" natural language, and to translate it into actions. |



[^1]: Taylor, Ross, et al. "Galactica: A Large Language Model for Science." arXiv preprint arXiv:2211.09085 (2022).
