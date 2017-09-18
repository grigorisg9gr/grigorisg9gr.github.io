---
title:  "Simple classifier is-face or not"
categories:
  - Machine Learning
  - Computer Vision
tags:
  - computer vision
  - classification
  - python
---


This post is devoted to constructing a simple binary classifier from scratch. A classifier is a tool that enables the algorithm to categorise different objects in their respective 'class'. A binary classifier is a classifier with two categories, e.g. is this animal cat or dog? 

In this example, the classifier is trained in the 'face' class, i.e. it returns a binary decision whether there is a face in the pixels or not.
This post is prepared as part of a seminar of the EESTech Challenge 2016-17 ([official site](http://eestechchallenge.eestec.net/#/), [EESTEC news](https://eestec.net/news/tech-your-future-with-eestech-challenge/)).

A simple version of this classifier with ~25 lines of code can be built as indicated below, using python and 2 well-tested libraries. In the end of this post, there are some proposals for improving the accuracy of the trained model, extending it for more difficult cases. Aside of the snippets below, the notebook with the complete code can be found [here](https://gist.github.com/grigorisg9gr/b344260171538bc8711834c8de82e3a7).

If you want to run the code yourself, you should:

- install the [menpo](http://www.menpo.org/) library. The recommended way is by installing [Anaconda](https://www.continuum.io/downloads). Among the reasons to install it through anaconda is that a lot of additional package, e.g. [scikit learn](http://scikit-learn.org/stable/) will be installed along with menpo/menpofit (and you won't need to spend time with compatible versions, conda will sort it out).
- download the [300W](http://ibug.doc.ic.ac.uk/resources/300-W/) dataset along with the [Pascal](http://host.robots.ox.ac.uk/pascal/VOC/) dataset.

