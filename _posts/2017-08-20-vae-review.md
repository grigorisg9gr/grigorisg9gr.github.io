---
title:  "Review on online VAE tutorials"
categories:
  - Machine Learning
  - Neural Networks
tags:
  - machine learning
  - variational autoencoders
  - neural networks
  - review
---

Instead of creating another tutorial about Variational Autoencoders (VAE), I will share my experience on the parts that introduced me to the topic. 

VAE are a type of neural network (function approximators) that assume the existence of an undelying low-dimensional space of the data. They try to approximate this latent distribution. You can then sample from this distribution to generate synthetic data. VAE are emerging as a great way to model the latent properties of objects, while one of their interpretations lies in variational Bayesian methods. They remain a hot research topic, so our understanding is not complete.

This review is organised in two parts: in the first part each tutorial is summarised. Then, a table with the attributes of each tutorial are provided. The attributes are organised in three categories: i) background information, ii) main VAE part, iii) applications.

- [fastforward labs](http://blog.fastforwardlabs.com/2016/08/12/introducing-variational-autoencoders-in-prose-and.html): This is a two-part tutorial for VAE; in part 1 VAE are explained as a generalisation of the autoencoder and explain the differences from it. Sequentially, they explain how VAE can be approached from the Bayesian perspective (the author provides a high level intuition). 
In the [second part](http://blog.fastforwardlabs.com/2016/08/22/under-the-hood-of-the-variational-autoencoder-in.html), they dive more into the practical implementation (python 3, tensorflow). They additionally explain the re-parametrization trick and the final cost function. 

- [jmetzen](https://jmetzen.github.io/2015-11-27/vae.html): The author implements VAE step by step in tensorflow and experiments with MNIST. He provides a notebook with the code, very practical for understanding a fundamental implementation.

- [int8.io](http://int8.io/variational-autoencoder-in-tensorflow/): The author starts by explaining the benefits of GAN and how it can create artificial samples. However, through the shortcomings of GAN, he introduces VAE as a combination of the Autoencoders and the variational inference. He presents a nice application (face swapping). The focus guides the reader through a practical introduction/understanding to the network's structure.

- [kvfans](http://kvfrans.com/variational-autoencoders-explained/): Nice introductory post on explaining VAE. The author provides details on encoding/decoding an image through an example. He introduces VAE as a solution to the shortcomings of GAN. 

- [jaan.io](https://jaan.io/what-is-variational-autoencoder-vae-tutorial/): The first part is devoted in an engineering approach of the original paper. The introduction is a bit rough, however the second part is devoted in the theoretical aspect. He derives the lower bound minimisation. As a 'footnote', the author provides a splendid explanation of the re-parametrization trick, while the glossary in the end of the article is very handy (it summarises the differences of the neural network vs probabilistic approach). Overall the first part is engineering-based tips, while the second part is more mathematical and demands some math understanding. 

- [wiseodd](https://wiseodd.github.io/techblog/2016/12/10/variational-autoencoder/): The author starts with a comparison of GAN vs VAE. Then he retracts and uses a very simple example (imagination process) to provide the intuition of the latent variables. He derives the variational bound (math heavy part); he implements VAE in Keras (python) and explains the re-parametrization trick. Even though the deep learning side is not developed much, personally I find this tutorial quite thorough (from the math side). 

- [nutty netter](https://www.youtube.com/watch?v=h0UE8FzdE8U): Short visual introduction in VAE. It starts by explaining why the log likelihood allows the efficient stohastic optimisation, derives the variational bound and then explains VAE as a neural network. The video creator offers some experimental results and some improvements in the original paper. However, he does not explain the reparametrisation trick or the motivation to use VAE instead of the alternatives (mean field, etc).

Following the summation of the articles, the table below describes the core components that are included in each article. The following abbreviations are used:

- ML: machine learning
- AE: autoencoders' explanation
- LL: log likelihood explanation
- NN: neural network

| Article | Background info | Main part | Applications | Difficulty/Audience |
|---------|:---------------:|:---------:|:------------:|:----------:|
|[fastforward labs](http://blog.fastforwardlabs.com/2016/08/12/introducing-variational-autoencoders-in-prose-and.html)| `AE`<br/>`Bayesian learning` |`VAE as NN`|     -         | `ML beginners` |
|[fastforward labs (part2)](http://blog.fastforwardlabs.com/2016/08/22/under-the-hood-of-the-variational-autoencoder-in.html)| - | `cost function explanation` |     -         | `requires math understanding` |
|[jmetzen](https://jmetzen.github.io/2015-11-27/vae.html)|  -  | -  |    `code`<br/>`results`  | `engineers` |
|[int8.io](http://int8.io/variational-autoencoder-in-tensorflow/)|`AE` | `VAE as NN` | `code`<br/>`results` | `engineers`<br/>`ML beginners` |
|[kvfans](http://kvfrans.com/variational-autoencoders-explained/)| - | `VAE as NN` | `code`<br/>`results`<br/>`limitations` | `engineers` |
|[jaan.io](https://jaan.io/what-is-variational-autoencoder-vae-tutorial/)| `probabilistic/bayesian approach`<br/>`approximate posterior` |`variational bound derivation`<br/>`re-parametrization trick`| `code` | `requires math understanding` |
|[wiseodd](https://wiseodd.github.io/techblog/2016/12/10/variational-autoencoder/)| `bayesian approach`<br/>`approximate posterior`<br/>`intuition`|`variational bound derivation`<br/>`re-parametrization trick`| `code`| `requires math understanding` |
|[nutty netter](https://www.youtube.com/watch?v=h0UE8FzdE8U)| `LL` | `variational bound derivation`<br/>`VAE as NN`| `limitations` | `requires math understanding` |


The tutorials above cover the introduction to VAE from different aspects, however they all have limited explanation on the shortcomings of VAE (e.g. how the Gaussian prior leads to blurry results) or how to adapt VAE to more complex modelling than MNIST.
Obviously, these tutorials are introductory in the topic and the actual paper(s) about VAE provide more information on the motivation and derivation of this type of neural network. 
