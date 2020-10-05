# two-pathway-learning

This repository contains code to accompany the following manuscript:

"Remembrance of things practiced with fast and slow learning in cortical and subcortical pathways" \
James M. Murray and G. Sean Escola \
Nature Communications (2020) \
doi:XX

This code may be reused and adapted, in which case please cite the above paper.

The code consists of three Python (v3.7) notebooks, as described below.

`ClassificationError.ipynb` derives the forgetting curve for a single binary neuron classifying random patterns with supervised learning. It also derives the forgetting curve for a neuron with two sets of inputs: one set with fast supervised or reinforcement learning, and another set with slow Hebbian learning. The addition of the second set of inputs enables the neuron to better remember patterns that are presented repeatedly during training.

`InputAlignment.ipynb` shows that, as a pattern to be classified is presented multiple times to a binary neuron with two sets of inputs, where one set of inputs has fast supervised learning and the other has slow Hebbian learning, two things occur. The first is _input alignment_, which means that the inputs along the two pathways become aligned with one another. The second is _control transfer_, which means that the slow-learning pathway becomes increasingly responsible for driving the neuron's activity.

`ReachingTask.ipynb` extends the two-pathway idea to a neural network with one hidden layer trained to perform a task. The task is to smoothly move a cursor to one of four target positions given one of four input cues. The first layer of the network contains both fast-learning (supervised) and slow-learning (Hebbian) weights. The main result is that, if the first target is rehearsed only in the first session of training and then tested after all of the other targets have been trained, the testing performance is much better when the slow Hebbian weights are included, indicating that this pathway functions to prevent previously learned behaviors from being overwritten.
