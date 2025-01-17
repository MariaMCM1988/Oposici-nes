# Resumen Completo de Distribuciones de Probabilidad

A continuación, se describen las distribuciones de probabilidad discretas y continuas, incluyendo funciones de probabilidad o densidad, funciones de distribución acumulada, y características clave.

---

## Distribuciones Discretas

### Más Habituales

#### 1. Distribución de Bernoulli
- **Definición:** Experimento con dos posibles resultados: éxito y fracaso.

$$P(X = x) = p^x (1-p)^{1-x}, \quad x \in \{0, 1\}$$

$$
F_X(x) = 
\begin{cases} 
0, & x < 0 \\ 
1-p, & 0 \leq x < 1 \\ 
1, & x \geq 1 
\end{cases}
$$

- **Media:** $E(X) = p$
- **Varianza:** $\text{Var}(X) = p(1-p)$

#### 2. Distribución Binomial
- **Definición:** Número de éxitos en $n$ repeticiones independientes de un experimento de Bernoulli.

$$P(X = x) = \binom{n}{x} p^x (1-p)^{n-x}, \quad x \in \{0, 1, \dots, n\}$$

$$F_X(x) = \sum_{i=0}^{\lfloor x \rfloor} \binom{n}{i} p^i (1-p)^{n-i}$$

- **Media:** $E(X) = np$
- **Varianza:** $\text{Var}(X) = np(1-p)$

#### 3. Distribución de Poisson
- **Definición:** Modelo para contar eventos raros en un intervalo.

$$P(X = x) = \frac{\lambda^x e^{-\lambda}}{x!}, \quad x \geq 0$$

$$F_X(x) = \sum_{i=0}^{\lfloor x \rfloor} \frac{\lambda^i e^{-\lambda}}{i!}$$

- **Media y Varianza:** $E(X) = \lambda, \, \text{Var}(X) = \lambda$

#### 4. Distribución Geométrica
- **Definición:** Número de fracasos antes del primer éxito.

$$P(X = x) = (1-p)^x p, \quad x \geq 0$$

$$F_X(x) = 1 - (1-p)^{x+1}$$

- **Media:** $E(X) = \frac{1-p}{p}$
- **Varianza:** $\text{Var}(X) = \frac{1-p}{p^2}$

---

### Menos Habituales

#### 5. Distribución Binomial Negativa
- **Definición:** Número de fracasos antes del $r$-ésimo éxito.

$$P(X = x) = \binom{x+r-1}{x} (1-p)^x p^r, \quad x \geq 0$$

- **Media:** $E(X) = \frac{r(1-p)}{p}$
- **Varianza:** $\text{Var}(X) = \frac{r(1-p)}{p^2}$

#### 6. Distribución Hipergeométrica
- **Definición:** Número de éxitos en una muestra sin reemplazo.

$$P(X = x) = \frac{\binom{N_1}{x} \binom{N-N_1}{n-x}}{\binom{N}{n}}, \quad x \in \{0, 1, \dots, n\}$$

- **Media:** $E(X) = n \frac{N_1}{N}$
- **Varianza:** $\text{Var}(X) = n \frac{N_1}{N} \frac{N-N_1}{N} \frac{N-n}{N-1}$

---

## Distribuciones Continuas

### Más Habituales

#### 1. Distribución Uniforme
- **Definición:** Probabilidad constante en $[a, b]$.

$$f(x) = \frac{1}{b-a}, \quad a \leq x \leq b$$

$$
F_X(x) = 
\begin{cases} 
0, & x < a \\ 
\frac{x-a}{b-a}, & a \leq x < b \\ 
1, & x \geq b 
\end{cases}
$$

- **Media:** $E(X) = \frac{a+b}{2}$
- **Varianza:** $\text{Var}(X) = \frac{(b-a)^2}{12}$

#### 2. Distribución Normal
- **Definición:** Modelo para fenómenos naturales.

$$f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}, \quad x \in \mathbb{R}$$

$$F_X(x) = \int_{-\infty}^x f(t) dt$$

- **Media:** $E(X) = \mu$
- **Varianza:** $\text{Var}(X) = \sigma^2$

#### 3. Distribución Exponencial
- **Definición:** Tiempo entre eventos consecutivos.

$$f(x) = \lambda e^{-\lambda x}, \quad x \geq 0$$

$$
F_X(x) = 
\begin{cases} 
0, & x < 0 \\ 
1 - e^{-\lambda x}, & x \geq 0 
\end{cases}
$$

- **Media:** $E(X) = \frac{1}{\lambda}$
- **Varianza:** $\text{Var}(X) = \frac{1}{\lambda^2}$

---

### Menos Habituales

#### 4. Distribución Gamma
- **Función de densidad:**

$$f(x) = \frac{\lambda^k x^{k-1} e^{-\lambda x}}{\Gamma(k)}, \quad x \geq 0$$

- **Función de distribución acumulada:**

$$F_X(x) = \int_0^x f(t) dt$$

- **Media:** $E(X) = \frac{k}{\lambda}$
- **Varianza:** $\text{Var}(X) = \frac{k}{\lambda^2}$

#### 5. Distribución de Pareto
- **Función de densidad:**

$$f(x) = \frac{\alpha x_0^\alpha}{x^{\alpha+1}}, \quad x \geq x_0$$

- **Función de distribución acumulada:**

$$F_X(x) = 1 - \left(\frac{x_0}{x}\right)^\alpha, \quad x \geq x_0$$

- **Media y Varianza:** Dependen de $\alpha > 1$ y $\alpha > 2$, respectivamente.

---

Este resumen incluye todas las distribuciones, con las funciones clave y notación de **MathJax** para plataformas compatibles.
