> This file is a AI rewrite of my original dication.

# Catenary Activation Function

The catenary activation function proposes an approach to an activation - leveraging the natural properties of the catenary curve. Inspired by the inherent elegance of nature's mathematical principles, this method introduces additional dimensions of control and flexibility, hoping to produce a more organic alignment with neural behavior.

## Overview

The catenary activation function is designed to integrate natural curves for a smoother and more balanced transition in activation values.

## The Catenary Curve: Nature's Perfect Arc

The catenary curve ("perfect curve"), describes the shape assumed by a freely hanging chain or cable under gravity. This curve is known for its optimality in balancing forces and distributing tension evenly.

## Design and Dimensions of the Function

A distinguishing feature of the catenary activation function is its incorporation of three additional inputs beyond the standard activation parameters.

These inputs, referred to as dimensions, include:

- **Start Point:** Determines where the activation begins.
- **End Point:** Sets the termination of the activation.
- **Length:** Controls the overall depth and extent of the curve.

By tuning these parameters, the function can mimic various traditional activations. Adjusting the settings could allow the function to transition through behaviors. E.g. a sigmoid to ReLU without the need to switch functions entirely.

## Benefits and Potential Impact

The advantage of utilizing a catenary-based activation function lies in its adaptability:

+ **Flexibility:** With the ability to morph into different activation behaviors, the network can adapt more fluidly to diverse data sets.
+ **Training Dynamics:** By aligning more closely with natural principles, there is potential for more efficient training and better performance.
+ **Neuronal Control:** By delegating the control of the start and end points to independent neurons, along with an additional neuron managing the curve's length, the network can learn to optimize these parameters for the best overall performance - for training, and potentially during activation time.


## Implementation Considerations

### Smooth Transition and Boundary Management

The start and end points may reside within a defined activation space (e.g., between 0 and 1). This requires smoothing the tips of the curve to prevent abrupt fall-offs and ensure continuity.

Conceptually, this is akin to manipulating a physical chain in two-dimensional space, where each endpoint is _continued_ from their 2D position, applying smooth transtions from those tips to the _edge_ of the activation space.


### Caching and Computational Efficiency

Another consideration is the caching of curve layout.

Given that the precision of floating point representations can vary dramatically (for example, floating point 4 might only need 1,000 points while floating point 16 could be millions), an efficient derivative-based approach to reading the function should be considered.

We split the spline and apply more points around the curve, when activated we derive the gradient given the two closest points from the cached curve.


### Backward Propagation Challenges

One of the more complex aspects of introducing a novel activation function is defining its behavior during backward propagation.

Primary Ideas:

+ **Smooth Reverse Curve:** Utilize the smooth points of the forward pass to generate a single, smooth “bump” curve during backpropagation. Derived from the smoothness created at the tips.
+ **Mirrored Catenary:** (probably poor) Implement a true reverse catenary, essentially creating an inverse or mirror version of the activation function tailored specifically for the backward pass.
+ **Calculated:** The shape of the _bump curve_ can be derived from the shape of the catenary.

