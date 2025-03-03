# catenary-activation-function

This library proposes the use of a "catenary" curve as an activation function. Allowing more dimensions of change.


During extant work with mathematics and other machine learning, I seem to find a lot of the mathematics or the best formulae derive from nature. It seems to conclude that if artificial intelligence frameworks mimic that of the natural brain, then finding an activation function of which is more intrinsic to natural properties should result in a better outcome.

That's the theory.

---

> Aiming to align artificial neural networks more closely with natural principles. The catenary curve shape could provide a more balanced or smoother transition compared to traditional functions.


The catenary curve in itself is the "perfect curve". It's the most optimal curve under load and rest. In turn should work when resolving natural curves in our activation. All activations are either curvy or very straight, but this means we must pick one. What if it were possible to have the perfect curve all the way through the entire function, e.g. linear to sigmoid.

Using the catenary curve could offer a more flexible activation function.

The catenary has three additional inputs along with the standard inputs used for an activation. I call them dimensions. They are the start and end points and length of the curve itself.

Extending the length would change the depth of the curve. In some activations, you can go under this cutoff. In backward propagation, you would have a reverse curve.

An activation function built with plottable points could have independent neurons managing the start and end positions, and the third neuron managing the length. These could be trained to produce the optimal activation function for that data set.

The activation function could mimic other activation functions by dialing the right settings. You could go from sigmoid to ReLU without changing the activation function itself.

---

I think that's the real benefit of a catenary. Two different variations of the same curve could elicit different results from the same dataset. A general appliance is fitting and could serve for more organic nature.

My concept is - if this is a better curve, it should be easier to train and more manage organic activations. If the catenary curve proves more naturally aligned with neural functions, it could improve both training efficiency and performance.


Additional components to the activation function include the "start" and "end" _points_.

If they reside within the k-space of the activation layer, i.e. if the start and end points reside within an area of which can elicit results - rather than starting outside of a 0 and 1 property - The tips of the curve need to be _smoothed_. We need to smooth-off the tips, thereby ensuring that there isn't a fall-off.

I think these two points would be 2D, so you could move them in 2D space, changing the curve, just like you would a normal chain.

Another avenue can be _caching of positions_. A simple equation based upon the width of the fixed floating point numerical decimal.
For example, a floating point 4 only needs 1,000 points. A floating point 16 may need a million points. That would be silly. So you would obviously use a derivative.

---

At the moment Backward propagation isn't completely solved. I'm not sure what type of curve to backpropagate. My first theory is to take the smooth points of A and B and produce a single hill curve, bump curve if you will, for the reverse. Other theories would a true reverse catenary, where you would have an activation function dedicated to backwards propagation, which would be the inverse or the mirror version of the same catenary. Potentially we could _train_ a backprogration curve.

Likely we can derive a backward hump curve given the dimensions of the curve.