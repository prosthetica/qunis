# QUSIM

> Quantum Simulation SDK

QUSIM is a simulation and 3D visualisation SDK to aid in the exploration of quantum computation. 

# Bloch Sphere

> In quantum mechanics, the **Bloch sphere** (also known as the Poincaré sphere in optics) is a geometrical representation of the pure state space of a 2-level quantum system. A useful way of interpreting the state of a qubit is by the angles of the vectors, 

![](https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Bloch_sphere.svg/384px-Bloch_sphere.svg.png)



# Visualisation of Quantum Mechanics

Here we have a represantion of a wavefunction of a free particle, below is a sample presentation of such modelling:
 
[![](http://img.youtube.com/vi/p7bzE1E5PMY/0.jpg)](http://www.youtube.com/watch?v=p7bzE1E5PMY "")


# Visualisation of an Electron


## Introduction

Qusim is an open source visualisation and simulation tool to empower creatives and researchers to develop artistic interpretations of quantum computing. It is designed with following in mind:

- quantum mechanics and simulation;
- quantum visualisation (volumetric);
- quantum computation education.
- quantum circuitry data structure visualiser

## Simulation 

#### Toffoli 

Toffoli simulator, which is a special-purpose simulator that can simulate quantum algorithms , for example this is exposed with the method `ToffoliSimulator`: 

```c-sharp
    var sim = new ToffoliSimulator();
    var res = myOperation.Run(sim).Result;
    var sim = new ToffoliSimulator(qubitCount: 1000000);
    var res = myLargeOperation.Run(sim).Result;
```    

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


## Papers Referenced

> Quantum spacetime on a quantum simulator
> Keren Li, Youning Li, Muxin Han, Sirui Lu, Jie Zhou, Dong Ruan, Guilu Long, Yidun Wan, Dawei Lu, Bei Zeng & Raymond Laflamme 
> https://www.nature.com/articles/s42005-019-0218-5

> Visualizing a silicon quantum computer
> Barry C Sanders, Lloyd C L Hollenberg, Darran Edmundson, and Andrew Edmundson
> https://iopscience.iop.org/article/10.1088/1367-2630/10/12/125005

> Architectural design for a topological cluster state quantum computer,
> Simon J. Devitt, Austin G. Fowler, Ashley M. Stephens, Andrew D. Greentree, Lloyd C.L. Hollenberg, William J. Munro, Kae Nemoto
> https://arxiv.org/abs/0808.1782

## License

**Qusim** is released under the Apache 2 license.
