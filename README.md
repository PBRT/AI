# AI
General knowledge and definitions of AI 

## Perceptrons

### Structure

The basic entity to reflect neurons initially was called **perceptrons** since 1950. Take a bunch of inputs, and produce only **one binary output**.

Each inputs have a weight, and the overall perceptron have a threshold. Weights reflects the importance of an input (weather, company...).

```
const sum = x1*w1 + x2*w2 + x3*w3 ....;
const output = sum > threshold ? 1 : 0;
```

or in another way with scalar products

```
const bias = -threshold;
const output = [x1, x2, x3] * [w1, w2, w3] + bias > 0 ? 1 : 0
```

### Network of perceptrons

Normally, the first layer take care of the *simple* decisions, and then give the output to a second layer and so on util the final output. The network is hence able to make decision from previous decisions, and tune the most accurate answer.

The output of all the perceptrons is connected to all the input of the second layer.

The input layer is a layer of perceptrons with a value and no input.

Overall, network of perceptrons is great, but any small modifications lead to a big change in the output (either 0 or 1). So it's hard to *tune* the way we want, or at least it's hard to see how to improve gradually


## Sigmoid Neuron

### Definition

Exactly the same as a percetron, but this time input is **between 0 and 1**. So basically a small input/weight modification create a small output modification, enable the learning process.

The output value is computed with the formula σ(w⋅x+b) with σ(z)≡1/1+e−z.

Looks complicated to calculate, but what's important to remember is:
- If w⋅x+b is big, output will be around 1
- If w⋅x+b is small, output will be around 0

It's only when w⋅x+b is close to the middle that we'll have variations.

### Multiple Layer Perceptrons (MLP)

Confusing name since most of the time implemented with sigmoid. Basically refers to a network with an input layer, an output layer, and some *hidden* layer which simply means some layer in between.

Most of the networks are **feed-forwards** networks, which means output of an neuron is fed to the the input of the next one, with no loops.
