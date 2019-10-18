# QUSIM

Quantum Simulation SDK

# Bloch Sphere


![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Bloch_sphere.svg/384px-Bloch_sphere.svg.png)

> In quantum mechanics, the **Bloch sphere** (also known as the Poincaré sphere in optics) is a geometrical representation of the pure state space of a 2-level quantum system


# Visualisation of Quantum Mechanics


[![](http://img.youtube.com/vi/p7bzE1E5PMY/0.jpg)](http://www.youtube.com/watch?v=p7bzE1E5PMY "")


# Visualisation of an Electron


## Introduction

Yao is an open source framework that aims to empower quantum information research with software tools. It is designed with following in mind:

- quantum algorithm design;
- quantum [software 2.0](https://medium.com/@karpathy/software-2-0-a64152b37c35);
- quantum computation education.

**We are in an early-release beta. Expect some adventures and rough edges.**

## Try your first Yao program

A 3 line [Quantum Fourier Transformation](https://quantumbfs.github.io/Yao.jl/latest/examples/QFT/) with [Quantum Blocks](https://quantumbfs.github.io/Yao.jl/latest/man/blocks/):

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
Operation.qs:
namespace Quantum.DemoRotations2
{
 open Microsoft.Quantum.Primitive;
 open Microsoft.Quantum.Canon;
 open Microsoft.Quantum.Extensions.Diagnostics;
 open Microsoft.Quantum.Extensions.Math;
 operation DemoRotations () : ()
 {
 body
 {
 using(qubits = Qubit[1])
 {
DumpMachine("");
 }
 }
 }
}
```

## Installation

Yao is a [julia](https://julialang.org/) language package. To install Yao, please [open Julia's interactive session (known as REPL)](https://docs.julialang.org/en/v1/manual/getting-started/) and type `]` in the REPL to use the package mode, then type this command:

For stable release

```julia
pkg> add Yao
```

For current master

```julia
pkg> add Yao#master YaoBlocks#master YaoArrayRegister#master
```

If you have problem to install the package, please [file us an issue](https://github.com/QuantumBFS/Yao.jl/issues/new).

For CUDA support, see [CuYao.jl](https://github.com/QuantumBFS/CuYao.jl).

## Documentation

### Getting Started

[Examples: understand Yao's code for quantum algorithms](https://quantumbfs.github.io/Yao.jl/stable/#Getting-Started-1)

### Algoritm Zoo

Some quantum algorithms are implemented with Yao in [QuAlgorithmZoo](https://github.com/QuantumBFS/QuAlgorithmZoo.jl).

### Online Documentation

- [**STABLE**](https://quantumbfs.github.io/Yao.jl/stable) — most recently tagged version of the documentation.
- [**LATEST**](https://quantumbfs.github.io/Yao.jl/latest) — in-development version of the documentation.

## Communication

- Github issues: Please feel free to ask questions and report bugs, feature request in issues
- slack: you can [join julia's slack channel](https://slackinvite.julialang.org/) and ask Yao related questions in `#yao-dev` channel.
- Julia discourse: You can also ask questions on [julia discourse](https://discourse.julialang.org/) or the [Chinese discourse](https://discourse.juliacn.com/)

## Contribution

Please read our [contribution guide](https://github.com/QuantumBFS/Yao.jl/blob/master/CONTRIBUTING.md).

## The Team

This project is an effort of QuantumBFS, an open source organization for quantum science. Yao is currently maintained by [Xiuzhe (Roger) luo](https://github.com/Roger-luo) and [Jin-guo Liu](https://github.com/GiggleLiu) with contributions from open source community. All the contributors are listed in the [contributors](https://github.com/QuantumBFS/Yao.jl/graphs/contributors).

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
