# SASDetector: High Efficiency Code Clone Detector Based on Syntax and Semantic Features


## Introduction

SASDetector is an interpretable clone detection tool with high performance, it consists of three main phases:

* Firstly, we propose a novel code representation CPT, extracted from the property graphs of the functions based on static analysis.
* Secondly, we extract features from CPT based on five features of non-keyword nodes, including Node, Parent, Sibling, Usage and Data Flow features.
* Finally, a specific matching algorithm is designed to detect code clones and deduce similar code snippets between them, where asymmetric Dice similarity coefficient is used for similarity measure

## Dataset

We conduct our evaluations on two datasets: BigCloneBench and Open-Source projects


* [BigCloneBench](https://github.com/clonebench/BigCloneBench) is code clone benchmark dataset which composes of over 6,000,000 tagged clone pairs. According to the clone type, it is divided six categories: Type-1, Type-2, VSType-3, SType-3, MType-3, and WType-3/Type-4. In our experiment, we filter out the clone pairs with less than 5 lines.

* Four Open-Source Projects: [Ant 1.10.12](https://ant.apache.org/srcdownload.cgi), [Opennlp 1.8.1](https://opennlp.apache.org/download.html), [Maven 3.8.6](https://maven.apache.org/download.cgi), [SpringBoot 2.7.1](https://github.com/spring-projects/spring-boot). We extract all functions from each java file in these projects, details are as follows.


| System | Files | Functions | LOC |
| ---- | ----: | ----: | ----: |
| Ant 1.10.12 | 1,322 | 13,844 | 120,866 |
| Maven 3.8.6 | 989 | 5,928 | 66,196 |
| Opennlp 1.8.1 | 903 | 3,826 | 49,902 |
| Springboot 2.7.1 | 6,209 | 36,036 | 235,302 |