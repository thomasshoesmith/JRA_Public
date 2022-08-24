# JRA_Public
Undergraduate Research for the Junior Research Associate Scheme at the University of Sussex

## JRA abstract

Modern Artificial Neural Networks (ANN) still require a lot of processing power. For instance, AlphaGo used approximately 1MW of power to run, whilst a human brain only uses 20W.

Unlike units in ANNs which continuously exchange real-valued activations, neurons in spiking neural networks communicate infrequently using binary events called spikes like neurons in biological 
brains. This reduced communication means that, theoretically, SNNs could offer a much more energy efficient alternative to ANNs. 

Training SNNs from scratch remains tricky but there are several promising approaches for converting 
already trained ANNs to SNNs. The current limitation with SNNs is that they require a lot of signal spikes in order to achieve the same task performance as ANNs; the aim for this project will be to 
investigate more efficient means of spike based encoding of activations in SNNs in order to improve on both, the number of signals required as well as the accuracy of the SNN in image classification.

## What is the JRA?

"The eight-week programme is offered to all of our high performing undergraduate students over the summer. If you're accepted on to the scheme, you get a bursary to work on your research full time, work closely with supervisors, and network with other researchers.

You'll also attend training workshops and have access to University resources.

At the end of the scheme, you'll put together a research poster which is displayed at our Undergraduate Research Poster Exhibition. The top two posters are chosen to represent Sussex at the British Conference of Undergraduate Research (BCUR) annual Posters in Parliament exhibition. 

Since 2008, more than 450 students have participated in the programme - including students from Brighton and Sussex Medical School (BSMS) and there are special provisions for Sussex Neuroscience students."

https://www.sussex.ac.uk/study/undergraduate/undergraduate-research/junior-research-associates

## The Project 

Despite yielding impressive results from image classification to playing against humans in games such as AlphaGo [Silver et al., 2016], Artificial Neural Networks (ANNS) require a vast amount of energy when compared to the brain. AlphaGo as an example required approximately 1MW of power to run [Mattheij, 2016], meanwhile the energy consumed by an average human brain is equivalent to approximately 20W [Ling, 2001] giving AlphaGo 50,000 times more energy in this competition. This brings us onto the latest challenge in modern machine learning which is the focus on the efficiency of algorithms so that they can be run on more portable devices or scaled up without the requirement of large energy resources.

Spiked Neural Networks (SNN) based have shown the potential to be more energy efficient than comparable ANNs mainly due to their lower computational requirements and the sparser spike-based communications between neurons [Khacef et al., 2018]. However, training large SNNs from scratch remains challenging and converting a high performing ANN into a similarly performing SNN has typically involved encoding ANN activations in the firing rate of the spiking neurons [Sengupta et al., 2019]. However, the resulting SNN required a relatively large number of spikes to generate similar performance and these larger numbers of spikes outweighed the energy savings of the SNN.In a recent paper [Stöckl and Maass, 2021], the authors introduce a new method for converting ANNs to SNNs using the so-called “Few Spikes (FS) conversion”. FS treats each neuron’s output spikes as a binary code representing the activation of the ANN neuron and, by using the timing of the spikes to 
hold additional information in this way, fewer spikes are needed and each input can be presented for fewer timesteps.

This project will build on the research from this paper to explore further optimisations to these binary codes allowing the number of spikes and timesteps to be further reduced and efficiency improved. The SNN performance will be evaluated by its accuracy of image classification on a selection of benchmark data sets including CIFAR-10 and ImageNet. CIFAR-10 is a database consisting of 60,000 32x32 colour images that can be classified into 10 classes with 6000 images per class. ImageNet is a much more challenging dataset consisting of around 14 million larger images in 20000 classes.

## Feb 2022 update

Although functional, the current models need to be modified into event driven timesteps, rather than a single compute step. When this is completed (as part of my FYP) the updated method will be added to the notebook.
