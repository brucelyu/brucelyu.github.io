---
title: "Into Rabbit Hole of Quantum Again"
date: 2022-09-04T14:05:34+00:00
categories: [Diary, Science, Study Notes]
slug: into-rabbit-hole-of-quantum-again
comments: true  # Enable Disqus comments for specific page
---

It has been half a year since my last post, and I forgot to post a plan for the year 2022. 
So first some recent updates about my physics study.

Our research group has a weekly [textbook reading session][1], where we choose a textbook each year and study it together. 
In last two years, we have chosen

  - A. Zee's [group theory book][2], which discusses the mathematical language to study symmetry, and
  - X.-G. Wen's [quantum field theory book][3], focusing on the field techniques when dealing with quantum many-body systems.

This year, we have chosen [John Preskill's lecture notes][4] on quantum information and quantum computation. 
It's a journey to ***the strange and crazy quantum world***.

## Strangeness of a quantum world
If I'm only allowed to use a single adjective to describe quantum mechanics, "non-intuitive" will be my choice. 
There are lots of quantum phenomena that happen everyday in experiments and our daily life, which there is no daily language suitable for its explanation. 
We have to invent terminologies to refer to those ideas. 
Here are some examples,
- *Wave-particle duality*: This describes the fact that a thing sometimes behaves like a wave and sometimes behaves like a particle. 
You might have heard it many times.
- *Superposition*: This describes the fact that we have to think of a thing can be 
(1) *both here and there*, or, 
(2) *neither here nor there*, or 
(3) *either here or there*. 
It seems crazy, right?? 
That is the reason why we invent a new word, and it is the idea Schrödinger discussed in his famous cat thought-experiment.
- *Entanglement*: This describes a correlation which seems to exist for two particles, which can be arbitrary far away. 
Einstein called this spooky action at distance and rejected quantum mechanics for this reason.

Quantum information and quantum computation aim to harness this quantum strangeness for our use. 
For example, *superposition* can be used to achieve parallelization if carefully design, which can speed up the computation. 
Also, *Entanglement* can be harnessed to share information between two-part, with a security beyond imagination to current classical approach.

Personally, I believe it is a good playground for us to understand more about the strangenss of the quantum world.

## Quantum Optics: a real experiment playground of quantum strangeness
Light, or photon, is a quantum particle used to realize all the above strangeness. 
During the middle of August, as a complementary material for my study of quantum information, I finished a Coursera course, [Quantum Optics 2 --- two photons and more][5], by Alain Aspect. 
Based on a technique of producing and controlling a single photon state (which was introduced in the first course of the series), it is not possible to implement thought experiments to truly demonstrate the quantum strangeness in real world: violation of Bell's inequality and quantum cryptography. 
Aspect promised a third quantum optics course on light-matter interaction in the future.
            
## Learn quantum mechanics for a second time
My first pass of quantum mechanics is Barton Zwiebach's MITx serious 8.04x to 8.06x, taken about 3 to 4 years ago from 2018 to 2022. 
Studying quantum information remains to me many interesting and subtle topics which I didn't fully grasp back then, like Stern-Gerlach experiments or Bell's inequality. 
I decided to follow a new round of Prof. Freericks's [edX course about quantum mechanics][6] which started in early August. 
This course discusses physics phenomena before diving into mathematical formulations. 
For example, this course covers many fascinating stuffs like ***Stern-Gerlach experiment, Mach-Zehnder interferometer, quantum seeing in the dark, Bell's inequality, hidden variable theory and Wheeler's delay choice experiment***. 
There are all things I have heard of many times but never studied seriously. 
There are many helpful animations to demonstrate those thought experiment, which is a nice feature of this course. 
I feel quite satisfied to relearn quantum mechanics from another quite different perspective.

Another feature of this course is that the Feynman's path integral formulation (see the figure below) is introduced from the very beginning. 
The stationary phase approximation is also secretly introduced.

Now we are at the 4-th week, it feels like a very interesting quantum mechanics course!

{{< figure src="/posts/images/2022/light-quantum.png" width="200" caption="A simulation in Prof. Freericks's quantum mechanics course" >}}

 [1]: https://kawashima.issp.u-tokyo.ac.jp/for-students/group-seminars/
 [2]: https://press.princeton.edu/books/hardcover/9780691162690/group-theory-in-a-nutshell-for-physicists
 [3]: https://academic.oup.com/book/25836
 [4]: http://theory.caltech.edu/~preskill/ph229/
 [5]: https://www.coursera.org/learn/quantum-optics-two-photons
 [6]: https://www.edx.org/professional-certificate/georgetownx-foundations-of-quantum-sensing?index=undefined
