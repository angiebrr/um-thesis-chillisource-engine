# ChilliSource particle system study (thesis fork)

> [!WARNING]
> Archived and no longer maintained; kept for reference. This is my 2016 fork of ChilliSource v1.6 for my master's thesis, not the official engine. The upstream project is [ChilliWorks/ChilliSource](https://github.com/ChilliWorks/ChilliSource), and its original README is below.

## Overview

I forked ChilliSource, an open-source C++ game engine, to study its particle system for my master's thesis at the University of Montana. This fork adds the instrumentation behind that study:

- **Shiny integration** (`Source/CSProfiling/Shiny/`) for instrumented profiling on all platforms. It isn't thread safe, which is part of why I wrote my own metrics system.
- **A metrics system** (`Source/CSProfiling/Metrics/`) that records render and timing metrics to CSV, with its own `put_time` and `to_string` so it builds on Android
- **Particle system hooks** in `Source/ChilliSource/Rendering/Particle/` so the metrics can time each stage of the particle lifecycle and how long the update thread waits on locks

My commits are the ones from March–June 2016 by angelahnicole; everything else is upstream. The lock-free and multiple-mutex variants I compared are excerpted in the thesis repo.

**Tech:** C++, ChilliSource, Shiny, Windows/iOS/Android builds

Related repos:

- [um-thesis-particle-optimization](https://github.com/angiebrr/um-thesis-particle-optimization): the thesis itself, with results and the dataset
- [um-thesis-cspong-benchmarking](https://github.com/angiebrr/um-thesis-cspong-benchmarking): the Pong game that ran the automated benchmarks against this fork

---

## Original ChilliSource README

![alt link](Documents/Images/ChilliSourceLogo.png)

ChilliSource v1.6.0
====================

ChilliSource is an open source, cross-platform game engine designed by game developers for game developers. It is completely free to use, released under the MIT License.

Links
-----
* [Chilli Works Website](http://chilli-works.com/)
* [ChilliSource Documentation](http://www.chilli-works.com/learn/)
* [ChilliSource Samples Repository](https://github.com/ChilliWorks/CSSamples)
* [ChilliSource Testing Repository](https://github.com/ChilliWorks/CSTest)
* [ChilliSource Forum](http://forums.chilli-works.com/)

Getting Started
---------------
The [Getting Started: What You'll Need](http://www.chilli-works.com/learn/tutorials-2/getting-started-what-youll-need/) tutorial provides a good starting point for working with ChilliSource. It demonstrates how to create and build a new project. Also check out the other tutorials for more information.

If you have any development questions or suggestions for the engine please post them on the [ChilliSource Forum](http://forums.chilli-works.com/). Any bugs encountered should be reported using [Github Issues](https://github.com/chilliworks/chillisource/issues).

Contribution
------------
Information on how to contribute can be found on the [Website](http://chilli-works.com/).

---

![alt link](Documents/Images/CricketLogo.png)

Built with Cricket Audio
<br>[www.crickettechnology.com](www.crickettechnology.com)

Usage of the Cricket Audio System is covered by the Cricket Audio free license (described at [http://www.crickettechnology.com/free_license](http://www.crickettechnology.com/free_license)). 
<br>For other licensing options, please visit [http://www.crickettechnology.com/source_license](http://www.crickettechnology.com/source_license).