# Identification-of-dynamical-system-using-ML
Building AI course project

## Summary

The goal of this project is to test a possibility to replace dynamic system simulations by a simplified model based on NN. The gain from this would be much shorter time to generate output given initial state and control inputs as functions of time, which can be used in real-time simulators or in other applications which require multiple simulations. If succesefully built, the generator can be used to study phase space of the system to detect stable/unstable equilibrium and bifurcations. 

## Implementation

To implement this idea, GAN model is suggested. If we are given an intial state of the system, control input signals and we know the "ground true" measured from some tests. The Generator will then generate an output and Discriminator should detect faulty vs true output.

## Verification

As a simplest case we can implement the GAN for a linear differential equation of first order,  
![alt text](https://latex.codecogs.com/gif.latex?%5Cdot%7Bx%7D%20&plus;%20Au%28t%29x%28t%29%20%3D%20f%28t%29)  
where u(t) is known control input, x(t0) = x0 - known initial state, and we can analytically derive general solution and generate large amount of "test measurments" for training.

## Possible risks and bottlenecks

The GAN model will require large amounts of training data. Training time increases rapidly with increased complexity and non-linearity of the model. If input data is very sparce, phase space of the Generator will differ much from the phase space of the original dynamic system. Some kind of augmented input will be reqiured.

