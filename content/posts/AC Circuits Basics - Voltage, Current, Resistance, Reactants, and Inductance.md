---
title: AC Circuits Basics - Voltage, Current, Resistance, Reactants, and Inductance
date: 2024-12-08
tags:
  - electronicsengineering
---
# Prerequisites
- The understanding of DC circuits
- Ohm's law
- Kirchhoff's Law
---
# Voltage and Current of AC Circuits
AC means alternating current, which means instead of a steady, constant current in DC, AC will have currents that flow in and out of the source. Since the current changes while the resistance remains constant, by Ohm's law, the voltage will alternate in and out of the source as well. In fact, both $V$ and $I$ will be in the same phase.
$$
\begin{align}
V & = V_{p}\sin(wt+\phi) \\
I & = I_{p}\sin(wt+\phi)
\end{align}
$$
# Inductance
An inductor is a coiled wire. When the coiled wire experiences changing electric flow, it will produce a magnetic field, and that magnetic field produce an opposite electric field, resulting in an opposition towards the current flow. The magnitude of the potential produced by the magnetic field is given by the equation:
```tikz
\usepackage{circuitikz}
\begin{document}
\begin{circuitikz}
\draw
(0, 0) -- (7, 0) to[switch] (10,0)
(10, 0) to[battery] (10, -10)
(10, -10) -- (0, -10)
(0, -10) to[lamp] (0, -5) to[resistor, l=R1] (0, 0)
(0, -5) to[capacitor, l=C1] (2, -5) -- (2, -3) to[resistor, l=R2] (5, -3)
(5, 0) to[resistor, l=R3] (5, -3)
(5, -3) to[capacitor, l=C2] (7, -3) -- (7, -10)
;
\end{circuitikz}
\end{document}
```
$$
\begin{align}
V & = L \frac{dI}{dt}
\end{align}
$$
Where $L$ is the inductance, which is the measure $V$ produced by the rate of flow of current, $I$.

# Capacitance
A capacitor are two parallel conducting plates separated by a dielectric. When the two parallel plates experiences changing electric flow, it will be continuously charged and discharged.
$$
\begin{align}
V & = L \frac{dI}{dt} \\
 \\
 I& = I_{0}\cos(wt) \\
 & = I_{0}(\cos wt+j\sin wt) \\
 & = I_{0}e^{jwt} \\
\frac{dI}{dt} & = I_{0}e^{jwt}jw \\
 & = Ijw \\
 \\
V & = LIjw \\
X_{L} & = j \times Lw \\
 & = Lw, \angle 90\degree
\end{align}
$$
$$
\begin{align}
Q & = CV \\
\frac{dQ}{dt} & = C\frac{dV}{dt} \\
I & = C \frac{dV}{dt} \\
 \\
V & = V_{p}\cos wt \\
 & = V_{p}(\cos wt+j\sin wt) \\
 & = V_{p}e^{jwt} \\
\frac{dV}{dt} & = V_{p}e^{jwt}(jw) \\
 & = Vjw \\
 \\
I & = CVjw \\
\frac{1}{X_{C}} & = Cjw \\
X_{C} & = \frac{1}{Cjw} \\
 & = \frac{1}{Cjw} \times \frac{j}{j} \\
 & = -j \times \frac{1}{Cw} \\
 & = \frac{1}{Cw},\angle -90\degree
\end{align}
$$

## Series Circuit
RL Circuits
$$
\begin{align}
|Z|^2 & = |R|^2+|X_{L}|^2 \\
Z & = R+j|X_{L}|
\end{align}
$$
$$
\begin{align}
Z & = R + j|X_{L}| \\
ZI & = RI + j|X_{L}|I \\
V_{s} & = V_{r}+jV_{L}
\end{align}
$$
RC Circuits
$$
\begin{align}
|Z|^2 & =|R|^2 + |X_{C}|^2 \\
Z & = R-j|X_{C}| \\
ZI & = RI-j|X_{C}|I \\
V_{s} & = V_{r}-jV_{C}
\end{align}
$$
RLC
$$
\begin{align}
Z & = R+j|X_{L}|-j|X_{C}| \\
 & = R+j(|X_{L}|-|X_{C}|) \\
ZI & = RI+jI(|X_{L}|-|X_{C}|) \\
V_{s} & = V_{r}+j(V_{L}-V_{C}) \\

|Z|^2 & = |R|^2+(|X_{L}|-|X_{C}|)^2
\end{align}
$$
## Parallel Circuit
RL Circuits
$$
\begin{align}
\frac{1}{Z} & = \frac{1}{R}+\frac{1}{j|X_{L}|} \\
\frac{V}{Z} & = \frac{V}{R}+\frac{V}{j|X_{L}|} \\
I_{s} & = I_{r}-jI_{L} \\
\frac{1}{|Z|^2} & = \frac{1}{R^2}+\frac{1}{|X_{L}|^2}
\end{align}
$$
RC Circuits
$$
\begin{align}
\frac{1}{Z} & = \frac{1}{R} - \frac{1}{j|X_{C}|}  \\
\frac{V}{Z} & = \frac{V}{R}- \frac{V}{j|X_{C}|} \\
I_{s} & = I_{r}+jI_{c} \\
\frac{1}{|Z|^2} & = \frac{1}{R^2}+ \frac{1}{|X_{C}|^2}
\end{align}
$$
RLC
$$
\begin{align}
\frac{1}{Z} & = \frac{1}{R} + \frac{1}{j|X_{L}|}-\frac{1}{j|X_{C}|} \\
 & = \frac{1}{R}-j \frac{1}{|X_{L}|}+ j \frac{1}{|X_{C}|} \\
 & = \frac{1}{R}+j \left( \frac{1}{|X_{C}|}-\frac{1}{|X_{L}|} \right) \\
 & = \frac{1}{R}- \frac{1}{j|X_{C}|}+ \frac{1}{j|X_{L}|} \\
\frac{V}{Z} & = \frac{V}{R}-\frac{V}{j|X_{C}|}+\frac{V}{j|X_{L}|} \\
I_{s} & = I_{r}+j(I_{C}-I_{L}) \\
\frac{1}{|Z|^2} & = \frac{1}{R^2}+ \left( \frac{1}{|X_{C}|} -\frac{1}{|X_{L}|}\right)^2
\end{align}
$$



