[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/wM4-KOzy)
# Little-o

Definition of little $o$: $T(n) \in o(f(n)) \iff \forall c > 0, \exists n_0, \forall n \ge n_0 : T(n) < c f(n)$  
Definition of big $O$: $T(n) \in O(f(n)) \iff \exists c > 0, \exists n_0 > 0, \forall n \ge n_0 : T(n) \le c f(n)$

Prove: $T(n) \in o(f(n)) \to T(n) \in O(f(n))$  
If $T(n) \in o(f(n))$, there exists a positive $c$ and $n_0$ such that for all $n \ge n_0$, $T(n) < c f(n)$. Using the same $c$ and $n_0$, $T(n) \le c f(n)$ must be true for all $n \ge n_0$, because if $a < b$, $a \le b$.  
Also note, the definition of little $o$ is stricter in requiring $T(n) < c f(n)$ holds for all $c$, while big $O$ only requires there exist a $c$. If a property is true for all $c$, obviously there exists a $c$ which satisfies the same property.

Concrete example: $T(n) = n, f(n) = n^2$  
$n \in o(n^2)$ because for $c = 1, n_0 = 2$, $n < n^2$  
$n \in O(n^2)$ because for $c = 1, n_0 = 2$, $n \le n^2$
