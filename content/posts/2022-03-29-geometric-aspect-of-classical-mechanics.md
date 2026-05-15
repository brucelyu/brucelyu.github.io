---
title: "Geometric aspect of classical mechanics"
date: 2022-03-28T15:09:07+00:00
categories: [Science, Study Notes]
slug: geometric-aspect-of-classical-mechanics
comments: true  # Enable Disqus comments for specific page
---

There are many approaches to classical mechanics. 
The first introduction in high school is intuitive and fit into our everyday experience: motion of a single particle is some trajectory in ordinary space and we are interested in finding its time evolution. 
This formulation relies heavily on notions like **particles**, **force**, **velocity** and **acceleration**. 

However, even in high school physics class, the discussion doesn't limit itself to intuitive notions. 
We are seeing very abstract concepts like **energy** and **momentum**. 
These conserved quantities are very powerful tools to make our analysis simple and elegant.
Moreover, it provides a deeper understanding of a physical problem. 

During the undergraduate physics course (see, for example, the [classical mechanics course][1] in MIT/OCW), non-physics majors usually learn mechanics using the same formulation developed during high school. 
More interesting topics related to rigid body are discussed, where the notion of **angular momentum** is naturally introduced. 
When we first meet **Lagrange**'s formulation of mechanics, we will probably start to be amazed by the **power of abstraction** and **mathematics**. 
It is probably the first shift of framework for learning physics. 
The final step to this journey of abstraction is perhaps the **differential geometric perspective of classical mechanics**. 
The classical book on this is Arnold's [Mathematical Methods of Classical Mechanics][2]. 
Recently, I finished a [concise online course][3] provided by the Perimeter institute of theoretical physics, which does an excellent job in explaining the geometric aspects of classical mechanics.

## Lagrangian and Hamiltonian formulation of classical mechanics
The beauty of Lagrangian's formulation of classical mechanics is that it frees us from the maze of vector analysis (drawing diagrams of an object subjecting to various forces...). 
It certainly satisfies the intuitive picture, but the payoff is the simplicity and generality of the formulation. 
Now the key concepts become *generalized coordinates*, *kinetic and potential energy*. 
This powerful formulation allows us
1. Change the description of our system easily by using different set of generalized coordinates. 
We can choose the most convenient ones (for a simple pendulum, we prefer a single angle to two Cartesian coordinates). 
1. Identify conserved quantities easily from symmetry of the problem according to the beautiful Noether's theorem.
1. This one single formalism encapsulates most of the classical physics, including mechanics, electromagnetism, optics and general relativity.
1. Through Feynman's path integral formulations, it provides a smooth and a very intuitive transition to the quantum world!

A Legendre transformation brings Lagrangian to Hamilton's formulation. 
The dynamics degrees of freedom double, but the equation of motion (EOM) becomes more symmetric; as an autonomous differential equation system, the order of the EOM goes down from 2 to 1, which has well-studied and understood in mathematics (see [this differential equation course][4] in MIT/OCW). 
Now the dynamics becomes a flow in the so-called phase space, an abstract flow in a geometric space.

## The underlying geometric picture
There are lots of subtle points in Lagrange and Hamilton's formulation. 
For example, is the Lagrangian function of generalized coordinates or function of time? 
How can we treat the coordinate $q$ and its velocity $dot{q}$ independently. 
This will be clarified using mathematics notions like manifold and tangent bundle. 
The very symmetric form of the Hamilton's equation will be described as symplectic structure in the differential geometry language.

 [1]: https://ocw.mit.edu/courses/physics/8-01sc-classical-mechanics-fall-2016
 [2]: https://link.springer.com/book/10.1007/978-1-4757-1693-1
 [3]: https://psi-online.perimeterinstitute.ca/courses/theoretical-mechanics
 [4]: https://ocw.mit.edu/courses/mathematics/18-03sc-differential-equations-fall-2011/
