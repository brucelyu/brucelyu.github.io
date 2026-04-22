---
title: "Kepler Problem"
date: 2023-04-23T16:24:15+00:00
categories: [Diary, Science]
slug: kepler-problem
comments: true  # Enable Disqus comments for specific page
---

Today I suddenly realized that Kepler problem is easier than I thought. 
I first met this problem in high school physics class around 2010 and 2011, where we were simply told that the orbit of a planet is an ellipse. 
The statement is clearly very important and it has a name, *Kepler's First Law*. 
However, all later calculations in high school are circular motions. 
I never actually derived this fact myself from Newton's law of motion. 
I believe the reason is that Calculus isn't taught in high school.

During undergraduate years, finally, we learned about Calculus. 
However, those students who are not major in physics never return to the Kepler problem. 
The starting point for Kepler problem in this new Calculus language is of course Newton's second law (mass $\times$ accelerator $=$ force, or $ma = F$),

\begin{align}
m\ddot{\mathbf{r}} = -\frac{GMm}{r^2} \hat{\mathbf{r}},
\end{align}

which looks pretty daunting. 
One can hardly see how this differential equation gives rise to an ellipse orbit, whose equation looks like

\begin{align}
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1.
\end{align}

In fact, one cannot even see why the orbit should be a closed shape from this differential equation 
(do you know why we cannot see this? See Feynman's excellent explanation about this differential equation in [Chapter 9 of his Volume 1 of Lectures on Physics][1]). 

This week, when working with the Kepler problem in General relativity, I encountered the classical problem of calculating the perihelion advance of the Mercury, which is one of [the classic tests][2] of the validity of the theory. 
It is a quite nontrivial calculation, the first step of which is Kepler problem in Newtonian theory. 
I suddenly realize the Kepler problem in Newtonian theory is quite straightforward and can be derived using probably less than 10 lines of equations.


The goal of this post is showing the derivation. 
My intention is that the derivation is accessible to second-year high school students who have already finished learning Newtonian theory: 1) $F= ma$, 2) conservation of energy, and 3) circular motion of planets. 
I assume the basic knowledge of derivatives, which is usually covered in high school first-year mathematics class. 
Hopefully, if I have done a decent job below, the post can demonstrate the power of the conservation laws, including energy conservation.

## Kepler problem in Newtonian gravity as simple as possible
In this short derivation, we will check the well-known facts that 1) the orbit of planets is an ellipse and 2) the sun is on one of the foci of the ellipse. 
The starting points are just two basics conservation laws of Newtonian mechanics.

We put the sun at the center of our coordinate system. 
Since we know that the only nontrivial force is the gravitational pull of the sun on the planet that always point radially towards the sun, the natural choice of the coordinate system is the polar coordinate $(r, \phi)$, which denotes the position of the planet. 
The gravitational potential energy of the planet is $V(r) = -\frac{GMm}{r}$, wherer $M$ is the mass of the sun and $m$ the mass of the planet. 
The kinetic energy of the planet has two parts, radial and tangential one, $K = \frac{1}{2} m \left( \left(\frac{dr}{dt} \right)^2 + \left(r \frac{d\phi}{dt}\right)^2\right)$. 
The conservation of energy means the sum of potential energy and kinetic energy is a *constant* $E$,

\begin{align}
E = \frac{1}{2} m \left(\left(\frac{d{\color{blue} r}}{dt} \right)^2 + \left({\color{blue} r}  \frac{d { \color{blue} \phi}}{dt} \right)^2 \right) -  \frac{GMm}{{ \color{blue} r}}, 
\end{align}

where I emphasize the dynamical variables in this problem with blue color—they are functions of time and it's our goal to find how they evolve with time. 
I cannot see how to write down the solution of the above equation since two unknown variables $r, \phi$ are one equation. 
The second equation is the conservation of angular momentum $L$ of the planets,

\begin{align}
L = m \cdot r \cdot r \frac{d\phi}{dt} = m { \color{blue} r^2} \frac{d{ \color{blue} \phi}}{dt}.
\end{align}

The first equal sign is the definition of angular momentum as mass $\times$ radial coordinate $\times$ tangential velocity. 
To find the curve of the orbit, we can either find $r(t), \phi(t)$ as functions of time and eliminate $t$, or find $r$ as function of $\phi$ directly. 
Let's choose the second approach here. 
The strategy is now clear, we can solve for $dr/dt$ and $d\phi / dt$ and eliminate $t$ by taking their ratio,

\begin{align}
\left(  \frac{dr}{dt} \right)^2 = 2 \frac{E}{m} + 2 \frac{GM}{r} - \frac{L^2}{m^2 r^2},\\\
\left( \frac{d\phi}{dt} \right)^2 = \frac{L^2}{m^2 r^4}, \text{ so}\\\
\left( \frac{dr}{d\phi} \right)^2 = \frac{(dr/dt)^2}{(d\phi / dt)^2}= \frac{2E/m + 2GM \frac{1}{r} - L^2/m^2 \frac{1}{r^2}}{L^2/m^2 \frac{1}{r^4}}.
\end{align}

The right-hand side of Eq. (7) begs us to treat $1/r$ as a variable, not $r$, so we define $u = 1/r$. 
By solving $u$ as a function of $phi$, we get $r$ immediately. 
Equation (7) in terms of $u$ is

\begin{align}
\left( \frac{du}{d\phi} \right)^2 &= \frac{2E/m + 2GM u - L^2/m^2 u^2}{L^2/m^2} =
\frac{2Em}{L^2} + \frac{2GMm^2}{L^2} u - u^2 \nonumber \\\
&=- \left(u - \frac{2GMm^2}{L^2} \right)^2 + \frac{2Em}{L^2} + \left( \frac{GMm^2}{L^2} \right)^2.
\end{align}

We move terms related to dynamic variable $u$ to the left-hand side and leave the constant to the right-hand side to get 

\begin{align}
\left( \frac{d{\color{blue} u}}{d{\color{blue} \phi}} \right)^2 + \left({\color{blue} u} - \frac{2GMm^2}{L^2} \right)^2 
= \frac{2Em}{L^2} + \left( \frac{GMm^2}{L^2} \right)^2.
\end{align}

We use blue to denote the variable. 
Remember that $u$ is a function of $phi$ and the above equation is a sum of two functions of $phi$ becomes a constant. 
What's the solution? 
Sinusoidal functions. 
And we are so lucky that the derivative of $cos$ gives you $sin$ and their sum is a constant! 
We find the equation for the curve of the planet orbit as

\begin{align}
\frac{1}{r(\phi)} = u(\phi) = \frac{2GMm^2}{L^2} + \sqrt{ \frac{2Em}{L^2} + \left( \frac{GMm^2}{L^2} \right)^2 } \cos(\phi). 
\end{align}

It still doesn't look like the standard equation of ellipse. 
Now, we have a good high-school math exercise of showing how the standard ellipse equation in Eq. (2) is related to our solution above in Eq. (10) in polar coordinate. 
Or you can refer to [this Wikipedia page][3].

Do you think it difficult or complicated? 
All we need are two conservation laws and a few lines of algebra! 
Now you see in front of your own eyes *how an ellipse arises from Newtonian mechanics and how the sun is at one of the foci of the ellipse*!

 [1]: https://www.feynmanlectures.caltech.edu/I_09.html
 [2]: https://en.wikipedia.org/wiki/Tests_of_general_relativity#Perihelion_precession_of_Mercury
 [3]: https://en.wikipedia.org/wiki/Ellipse#Polar_form_relative_to_focus
