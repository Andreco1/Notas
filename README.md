# Teoría de la Medida
Empezando por lo que es un **espacio de probabilidad**, es una triple $(\Omega, \mathcal{F}, P)$ donde $\Omega$ es un conjunto de "salidas", $\mathcal{F}$ es un conjunto de "eventos" y $P$ es una función tal que $P:\mathcal{F}\mapsto[0,1]$ , es decir, $P$ es una función que le asigna una **probabilidad** a los eventos. Asumimos que $\mathcal{F}$ es una  $\sigma-$ álgebra; i,e,. 

>Definición: $\sigma-$ álgebra:
>Una colección no vacía de subconjuntos de $\Omega$ que satisfacen:
I) Si $A \in\mathcal{F}$ entonces $A^{c}\in\mathcal{F}$ 
II) Si $A_{i}\in\mathcal{F}$ es una secuencia contable de conjuntos entonces $\bigcup_{i}A_{i}\in\mathcal{F}$ 

*Contable significa finito o contable infinito, es decir,  a lo más del tamaño de los naturales* $\mathbb{N}$ .
<>
Ya que la $\bigcap_{i}A_{i}=\left( \bigcup_{i}A_{i} \right)^{c}$ , entonces una $\sigma-$ álgebra es cerrada bajo intersecciones contables. 

Sin $P$ , $(\Omega, \mathcal{F})$ es llamado "**espacio de medida**", es decir, un espacio donde s puede poner una medida, eso es lo siguiente que vamos a definir. 

>Definición: Medida
>Es un conjunto de funciones aditivas no negativo y contable,
>
>$$
>\mu:\mathcal{F}\mapsto \mathbb{R}
>$$
>
>con 
>i) $\mu(A)\geq\mu(\emptyset)=0~~\forall A\in\mathcal{F}$
>ii) Si $A_{i}\in\mathcal{F}$ es una secuancia disjunta de conjuntos contable, entonces:
>
>$$
>\mu\left( \bigcup A_{i} \right)=\sum_{i}\mu(A_{i})
>$$


Si $\mu(\Omega)=1$ llamamos a $\mu$ la medida de la probabilidad. Las medidas de probabilidad las vamos a denotar como $P$ .

>Definición: Función aditiva:
>
>Sea $\mu:\mathcal{C}\mapsto\mathbb{\bar{R}}=\mathbb{R}\cup\{ -\infty,\infty \}$ una función definida sobre una colección de conjuntos $\mathcal{C}$ . Decimos que $\mu$ es finitamente aditiva si:
>- $\mu(\emptyset)=0$
>- Para toda colección finita  $(A_{n}) _ {1\leq n\leq m}$  de conjuntos  $\mathcal{C}$  , disjuntos dos a dos, tales que $\bigcup_{i=1}^{m}A_{i\in \mathcal{C}}$ se tiene
>
>$$
>\mu\left( \bigcup_{n=1}^{m}A_{n} \right)=\sum_{n=1}^{n}\mu(A_{n})
>$$


Toda suma tiene que estar bien definida, tal que no pueda pasar que $\mu(A_{i})=-\infty$ y que $\mu(A_{j})=\infty$ para cualesquiera $i,j$ . 

Los siguientes resultados muestran las consecuencias de la **definición de medida**. En todos los casos, consideramos que todos los conjuntos están en $\mathcal{F}$ . 

>Teorema 1.1.1 :
>Sea $\mu$ una medida en $(\Omega, \mathcal{F})$ 
>- Monotonía : Si $A\subset B$ entonces $\mu(A)\leq\mu(B)$ 
>- Subaditividad: Si $A\subset \bigcup_{m\in\mathbb{N}}A_{m}$ entonces $\mu(A)\leq\sum_{m\in\mathbb{N}}A_{m}$ entonces $\mu(A)\leq\sum _ {m\in\mathbb{N}}\mu(A _ {m})$
>- Continuo desde abajo: Si $A_{1}\subset A_{2}\subset\dots$ y $\bigcup_{i}A_{i=A}$ , es decir, $A_{i}\uparrow A$ y $\bigcup_i A_{i}=A\implies \mu(A_{i})\uparrow\mu(A)$ 
>- Continuo desde arriba: Si $A_{i}\downarrow A$ , es decir, $A_{1}\supset A_{2}\supset\dots$ y $\bigcap_{i}A_{i}=A$ , con $\mu(A) _ {i}<\infty\implies \mu(A_{i})\downarrow\mu(A)$




Las pruebas de este teorema se obtienen del libro "Probability: Theory and Examples - Rick Durrett (2019)".

**Prueba del Teorema 1.1.1:**
- **Monotonía**:

Sea $B-A=B\cap A^{c}$ la diferencia entre dos conjuntos. Usando $+$ para denotar la union disjunta, $B=A+(B-A)$ entonces:

$$
\mu(B)=\mu(A)+\mu (B-A)\leq\mu(A)
$$

$\therefore \mu(B)\leq\mu(A)~~~~~~~~ \blacksquare$  

- **Subaditividad**:

Si tomamos trozos del conjunto $A$ tal que $A'_{n}=A_{n}\bigcap A$ , aseguramos que los conjuntos sean disjuntos, tomamos entonces $B_{1}=A_{1}'$ y para cualquier $n>1$ tomamos a $B_{n}=A_{n}'-\bigcup_{m=1}^{n-1}A'_{m}$ , esto vuelve a los conjuntos disjuntos y fuerza que $\bigcup _ {n\in\mathbb{N}}B_{n}=A$ , ya que $B_{m}\subset A_{m}$ y por la condición de monotonía $\mu(B_{m})\leq\mu(A_{m})$ , entonces:

$$
\mu(A)=\sum_{m=1}^{\infty}\mu(B_{m})\leq\sum_{m=1}^{\infty}\mu(A_{m})
$$

$$
\therefore \mu(A)\leq\sum_{m=1}^{\infty}\mu(A_{m}) ~~~~~~\blacksquare
$$

- **Continuo por abajo**:

Si $A_{1}\subset A_{2}\subset A_{3}\subset\dots$ y $\bigcup_{i}A_{i}=A$, es decir $A_{i}\uparrow A$ y $\bigcup_{i}A_{i} = A \implies$

$$
\mu(A_{i})\uparrow \mu(A)
$$

se refiere a la sucesión creciente de las medidas de los elementos (subconjuntos) de $A$ , la demostración requiere tomar a $B_{n}=A_{n}-A_{n-1}$. Entonces las $B_{n}$ son disjuntas y tienen a $\bigcup_{m=1}^{\infty}B_{m}=A$ , entonces $\bigcup_{m=1}^{n}B_{m}=A_{n}$ , lo que implica:

$$
\mu(A)=\sum_{m=1}^{\infty}\mu(B_{m})=\lim_{ n \to \infty } \sum_{m=1}^{n}\mu(B_{m})=\lim_{ n \to \infty } \mu(A_{m})
$$

- **Continuo por arriba:**

sea $A_{1}-A_{n}\uparrow A_{1}$ así que $\mu(A_{1}-A_{n})=\mu(A_{1})-\mu_{A}$ y se sigue que

$$
\mu(A_{n})\downarrow \mu(A)~~~~\blacksquare
$$

>Ejemplo 1.1.2. Espacios de probabilidad discretos:
>Sea $\Omega=a$ un conjunto contable, i.e., finito o contable finito (a lo más del tamaño de los $\mathbb{N}$). sea $\mathcal{F}=$ el conjunto de todos los subconjuntos de $\Omega$.
>Sea $P(A)=\sum_{\omega \in A} P(\omega)$ donde $P\geq 0$ y $\sum_{\omega \in \Omega}=1$  

