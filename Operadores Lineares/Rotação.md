# Rotação

> **Definição**. Transformação linear que gira o objeto geométrico (vetor ou matriz) em torno de um ponto fixo.

## Fórmula geral

Digamos que $\rho_{\theta}$ seja a função que rotaciona um vetor $v$ de um ângulo $\theta$ no sentido anti-horário. Se considerarmos $v=(x,y)$, podemos afirmar:

```math
x=\|v\|\cos\alpha\text{\quad e \quad}y=\|v\|\sin\alpha
```

Em que $\alpha$ representa o ângulo entre $v$ e o vetor unitário $î$ ou $e_1$. Posto isso, podemos facilmente expressar as coordenadas de $\rho_{\theta}(v)$, tendo em vista que o ângulo entre $v$ e $e_1$ mudou de $\alpha$ para $\alpha+\theta$. Portanto, as coordenadas de $\rho_{\theta}(v)$ serão:

```math
\rho_{\theta}(v)=\begin{bmatrix}\|v\|\cos(\alpha+\theta)\\\|v\|\sin(\alpha+\theta)\end{bmatrix}\tag{1}
```

Para explicitar a relação entre as coordenadas acima com as de $v$, utilizamos algumas fórmulas bem conhecidas da trigonometria.

```math
\begin{align*}
&\sin(\alpha+\theta)=\sin(\alpha)\cos(\theta)+\sin(\theta)\cos(\alpha) \\ \\
&\cos(\alpha+\theta)=\cos(\alpha)\cos(\theta)-\sin(\theta)\sin(\alpha)
\end{align*}
```

Ao substituir essas expressões em $(1)$, $\|v\|\cos\alpha$ por $x$ e $\|v\|\sin\alpha$ por $y$, obteremos:

```math
\begin{align*}
&\rho_{\theta}(v)=\begin{bmatrix}x\cos(\theta)-y\sin(\theta)\\ x\sin(\theta)+y\cos(\theta)\end{bmatrix} \\ \\
&\rho_{\theta}(v)=\underbrace{\begin{bmatrix}\cos(\theta) & -\sin(\theta)\\ \sin(\theta) & \cos(\theta)\end{bmatrix}}_{\texttt{matriz de rotação}}\begin{bmatrix}x\\y\end{bmatrix}
\end{align*}
```

### Identidades trigonométricas

Aqui estão algumas identidades trigonométricas da soma e diferença de $\sin(\theta),\cos(\theta)$.

1. $\sin(\theta+\alpha)=\sin(\theta)\cos(\alpha)+\sin(\alpha)\cos(\theta)$
2. $\sin(\theta-\alpha)=\sin(\theta)\cos(\alpha)-\sin(\theta)\cos(\alpha)$
3. $\cos(\theta+\alpha)=\cos(\theta)\cos(\alpha)-\sin(\theta)\sin(\alpha)$
4. $\cos(\theta-\alpha)=\cos(\theta)\cos(\alpha)+\sin(\theta)\sin(\alpha)$
5. $\tan(\theta+\alpha)=\dfrac{\tan(\theta)+\tan(\alpha)}{1-\tan(\theta)\tan(\alpha)}$
6. $\tan(\theta-\alpha)=\dfrac{\tan(\theta)-\tan(\alpha)}{1+\tan(\theta)\tan(\alpha)}$
