# QUSIM

Quantum Simulation SDK
QUSIM is a simulation and 3D visualisation SDK to aid in the exploration of quantum computation. 

# Bloch Sphere

One other useful way of interpreting the state of a qubit is by the angles of the vectors, in
this case

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Bloch_sphere.svg/384px-Bloch_sphere.svg.png){width=250px}

> In quantum mechanics, the **Bloch sphere** (also known as the Poincaré sphere in optics) is a geometrical representation of the pure state space of a 2-level quantum system


# Visualisation of Quantum Mechanics

Here we have a represantion of a wavefunction of a free particle, below is a sample presentation of such modelling:
 
[![](http://img.youtube.com/vi/p7bzE1E5PMY/0.jpg)](http://www.youtube.com/watch?v=p7bzE1E5PMY "")


# Visualisation of an Electron


## Introduction

Qusim is an open source visualisation and simulation tool to empower creatives and researchers to develop artistic interpretations of quantum computing. It is designed with following in mind:

- quantum mechanics and simulation;
- quantum visualisation (volumetric);
- quantum computation education.

## Sample

```c-sharp
Driver.cs:
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using System;
namespace Quantum.DemoRotations2
{
 class Driver
 {
 static void Main(string[] args)
 {
 using (var quantumSimulator = new QuantumSimulator())
 {
 var result = DemoRotations.Run(quantumSimulator).Result;
 }
 Console.WriteLine("Done");
 Console.ReadLine();
 }
 }
}
```

## Installation

Yao is a [julia](https://julialang.org/) language package. To install Yao, please [open Julia's interactive session (known as REPL)](https://docs.julialang.org/en/v1/manual/getting-started/) and type `]` in the REPL to use the package mode, then type this command:

For stable release

```javascript
pkg> add Yao
```

For current master

```javascript
pkg> add Yao#master YaoBlocks#master YaoArrayRegister#master
```


## Papers Referenced

> Quantum spacetime on a quantum simulator
> Keren Li, Youning Li, Muxin Han, Sirui Lu, Jie Zhou, Dong Ruan, Guilu Long, Yidun Wan, Dawei Lu, Bei Zeng & Raymond Laflamme 
> https://www.nature.com/articles/s42005-019-0218-5

> Learning and inference on generative adversarial quantum circuits,
> Jinfeng Zeng, Yufeng Wu, Jin-Guo Liu, Lei Wang, and Jiangping Hu,
> Phys. Rev. A 99, 052306 – Published 6 May 2019

> Parameterized quantum circuits as machine learning models,
> Marcello Benedetti, Erika Lloyd, and Stefan Sack
> https://arxiv.org/pdf/1906.07682.pdf

## License

**Yao** is released under the Apache 2 license.
