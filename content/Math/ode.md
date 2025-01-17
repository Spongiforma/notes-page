+++
title = "ODEs"
author = ["root"]
draft = false
+++

## Theorems {#theorems}


### Rectification {#rectification}

A rectification of a direction field is a diffeomorphism mapping it into a field of parallel directions.

**Theorem**

Every smooth direction field is rectifiable in a neighbourhood of each point. If the field is of class \\(C^r\\), then the rectifying diffeomorphism can be taken from the class \\(C^r\\).

Equivalently,

-   All smooth direction fields in domains of the same dimension are locally diffeomorphic.
-   The differential equation \\(\dot{x} = v(t,x)\\) with smooth RHS is locally equivalent to \\(\dv{y}{\tau} = 0\\).

Existence and uniquness theorems follow from the rectification theorem.


### Initial conditions {#initial-conditions}

The solution of an equation with smooth RHS depends smoothly on the initial conditions. This allows us to investigate the effect of perturbations on solutions.


### Transformation over the time interval {#transformation-over-the-time-interval}

**Definition**

Transformation over the time interval from \\(t\_0\\) to \\(t\\) is the mapping of a domain of the phase space into the phase space that assigns to the initial condition at the instant to the value of the solution with this initial condition at the instant t.

**Theorem**

The transformations over the time interval from \\(t\_0\\) to \\(t\\) for an equation with smooth RHS

1.  are defined in a neighbourhood of each phase point \\(x\_0\\) for t sufficiently close to \\(t\_0\\);
2.  are local diffeomorphisms and depend smoothly on \\(t\_0\\) and \\(t\\)
3.  satisfy the identity \\(g^t\_t\_0 x = g^t\_s g^s\_{t\_0} x\\) for x and t sufficiently close to \\(t\_0\\).
4.  are such that for fixed \\(\xi\\) the function \\(\phi(t) = g^t\_{t\_0} \xi\\) is a solution of the DE, satisfying the intiial condition, \\(\phi(t\_0) = \xi\\).


### Extension theorems {#extension-theorems}

Consider \\(\dot{x} = v(t,x)\\) defined by a smooth direction field in a domain \\(U\\) of the extended phase space. Let \\(\Gamma\\) be a subset of the domain U.

**Definition**

A solution with the initial condition \\(\phi(t\_0) = x\_0\\) can be extended forward to \\(\Gamma\\) if there exists a solution with the same initial condition whose graph intersects \\(\Gamma\\) in a point where \\(t \geq t\_0\\).

**Corollary**

A solution with initial condition in a compact set in the extended phase space can be extended forward and backward to the boundary of the compact set.