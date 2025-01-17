# Teorema Espectral

> **Teorema.** (em dimensão dois) *Um operador autoadjunto que não é um múltiplo constante da identidade tem dois autovalores reais distintos aos quais estão associados autovetores ortogonais.*

De antemão, precisamos definir o conceito de operador autoadjunto. Desse modo, dizemos que um operador linear $T$ do plano é $\textit{autoadjunto}$ se

```math
\langle T(u)|v \rangle=\langle u|T(v) \rangle,\tag{1}
```

para quaisquer vetores $u$ e $v$ do plano. No entanto, podemos enunciar essa definição de 
forma matricial, tal como abaixo

```math
(Au)^{t}v=u^{t}(Av)
```

de modo que $A$ representa a matriz de um operador autoadjunto $T$ do plano e $u,v$ são 
vetores genéricos. Dado que $(Au)^{t}=u^{t}A^{t}$, teremos a expressão resultante

```math
u^{t}A^{t}v=u^{t}Av
```

No entanto, se isso vale para todas as escolhas de $u,v$, então $A^{t}=A$ e, portanto, se escolhermos

```math
\begin{align}
A=\begin{bmatrix}a_{11} & a_{12}\\a_{21} & a_{22}\end{bmatrix}\quad\text{teremos}\quad   A^{t}=\begin{bmatrix}a_{11} & a_{21}\\a_{12} & a_{22}\end{bmatrix} 
\end{align}
```

Assim, podemos afirmar que $A=A^{t}$, ou seja, $a_{21}=a_{12}$. O cálculo acima mostra que um operador é $\textit{autoadjunto}$ se, e somente se, sua matriz, relativamente à base canônica, é simétrica. Dentre os operadores lineares que estudamos, a [projeção](/Operadores%20Lineares/Projeção.md) e a [reflexão](/Operadores%20Lineares/Reflexão.md) são operadores autoadjuntos.

$\textbf{Demonstração.}$ Suponhamos que $T$ seja um operador autoadjunto, precisamos provar que $T$ tem dois autovalores reais distintos os quais estão associados a autovalores ortogonais.

Suponhamos que a matriz de $T$ seja dada por

```math
\begin{align}
A=\begin{bmatrix}a_{11} & a_{12}\\a_{12} & a_{22}\end{bmatrix}
\end{align}
```

Para calcular os autovalores de $T$ teremos que determinar as raízes do polinômio

```math
\begin{align}
\det(A-tI)=\det \begin{bmatrix}a_{11}-t & a_{12}\\a_{12} & a_{22}-t\end{bmatrix}=t^{2}-(a_{11}+a_{22})t+(a_{11}a_{22}-a_{12}^{2})
\end{align}
```

Cujo discriminante é dado por

```math
\Delta=(a_{11}+a_{22})^{2}-4(a_{11}a_{22}-a_{12}^{2})=(a_{11}-a_{22})^{2}+4a_{12}^{2}
```

Logo, $\Delta$ é um número positivo segundo a soma dos quadrados. Vamos analisar o que aconteceria se as raízes fossem iguais, isto é, $\lambda_{1}=\lambda_{2}$. Para isso, seria necessário que

```math
\Delta=(a_{11}-a_{22})^{2}+4a_{12}^{2}=0
```

O que só é possível se $a_{11}=a_{22}$ e $a_{12}=0$. Substituindo essas condições na matriz $A$ obteremos

```math
A=\begin{bmatrix}a_{11} & 0\\0 & a_{11}\end{bmatrix}=a_{11}I
```

ou seja, os autovalores de $T$ serão iguais apenas quando $A$ for um múltiplo da identidade, isto é, $A=a_{11}I$.

Agora iremos encontrar os autovetores de $T$. Com efeito, considere $\lambda_{1}\neq \lambda_{2}$ os autovalores de $T$ e sejam $u_{1}$ e $u_{2}$ autovetores associados a, respectivamente, $\lambda_{1}$ e $\lambda_{2}$. Substituindo na expressão $(1)$,

```math
\begin{align}
\langle T(u_{1})|u_{2} \rangle&=\langle u_{1}|T(u_{2}) \rangle \\ \\
\langle \lambda_{1} u_{1}|u_{2} \rangle &= \langle u_{1}|\lambda_{2}u_{2} \rangle \\ \\
\lambda_{1}\langle u_{1}|u_{2} \rangle&=\lambda_{2}\langle u_{1}|u_{2} \rangle  \\ \\
(\lambda_{1}-\lambda_{2})\langle u_{1}|u_{2} \rangle &= 0   
\end{align}
```

Como estamos supondo que $\lambda_{1}\neq \lambda_{2}$, a última equação implica que $\langle u_{1}|u_{2} \rangle=0$, ou seja, $u_{1}$ e $u_{2}$ são realmente ortogonais.
