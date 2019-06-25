Java Neural Decompilation

Introduction

Decompilation is reconstruction of a program in a high-level language to a low-level programming language. It has motivated to decompile many low-level programs due to many reasons such as fix bugs, changing requirements, analyzing software and etc,. Traditional decompilers rely on pattern matching to identify the high-level control-flow structure in a program. These decompilers try to match segments of a program’s control-flow graph (CFG) to some patterns known to originate from certain control-flow structures. Neural Machine Translation Recent years have seen tremendous progress in Neural Machine Translation (NMT). NMT systems use neural networks to translate a text from one language to another. This projeect presents a simple automatic neural decompilation technique for JVM bytecode to Java program.


This work consists of three steps:
 
1. Preparing Data 

The most important part in this project is the dataset. Most neural machine translation(NTM) use dictionary dataset to train their networks. This project as simple task just uses a dataset with 50 JVM bytecodes and their corresponding java programs. A Java compiler in the code is used to generate the bytecodes and saved them as a txt.file in a certain format. The comments in both programs (high-level and low-level) are eliminated to avoid mislearning the network. The final file is generated with 100 lines that each two lines represent the low-level program and its high-level program in respect. 

2. Neural Network 

There are many networks to translate the languages and also evaluate the translations. But, few of them worked on the compilation and decompilation. The seq2seq with attention network is chosen as the network with slightly modification. This network trains a sequence to sequence (seq2seq) model for Spanish to English translation. For more information please refer to: https://www.tensorflow.org/beta/tutorials/text/nmt_with_attention 

3. Translation and Evaluation
 
The base NMT network works well for Spanish to English translation. There is some conflict between the data between that project and this neural decompilation. Thus, the result is not significant. 

Implementation

This work is implemented on Tensorflow, Keras. python version 3.7. You need to install java-jdk in your environment.





