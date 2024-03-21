# Числовые ряды
Пусть дана числовая последовательность $\{a_n\}_{n \in \mathbb N}$. Составленная из членов данной последовательности символ $\sum\limits_{n=1}^{+\infty}a_n$ называется числовым рядом, а $a_i$ - общим членом ряда.

Сумма $n$ первых членов ряда $S_n = a_1 + ... + a_n$ называется $n$-ой частичной суммой ряда
$\lim\limits_{n \to \infty} S_n = S$ называется последовательных частичных сумм $\{S_n\}_{n \in \mathbb N}$ ряда называется суммой этого ряда.

Если предел конечен, то ряд **сходится**, иначе -- **расходится**.

## Теорема (необходимое условие сходимости ряда)
**Фор-ка.** Если ряд сходится, то $\lim\limits_{n\to\infty} = 0$

**Док-во.**
$$
S_n = \sum_{k=1}^{n}a_k,\ S_{n-1} = \sum_{k=1}^{n-1}a_k
$$
По условию $\exists S = \lim\limits_{n\to\infty}S_n = \lim\limits_{n\to\infty}S_{n-1}\Rightarrow\lim\limits_{n\to\infty}a_n = \lim\limits_{n\to\infty}(S_n - S_{n-1}) = S - S = 0.\ \blacksquare$

## Критерий Коши
**Фор-ка.** $\sum\limits_{n=1}^{+\infty}a_n$ сходится $\Leftrightarrow \forall \varepsilon > 0: \exists n_{\varepsilon} \in \mathbb N:$ при $\forall n > n_{\varepsilon}$ и $\forall p \in \mathbb Z, p \ge 0: |a_n + a_{n + 1} + ... + a_{n + p}| < \varepsilon$

**Док-во.**
$\sum\limits_{n=1}^{+\infty}a_n$ - сходится $\Leftrightarrow$

$$
\Leftrightarrow \exists S = \lim_{n\to\infty}S_n \Leftrightarrow \forall \varepsilon > 0: \exists n_{\varepsilon} \in \mathbb N:\forall n, m \in \mathbb N: n, m > n_{\varepsilon} |S_n - S_m| < \varepsilon \Leftrightarrow
$$

$$
\Leftrightarrow \forall n > n_\varepsilon, \forall p \in \mathrm{Z}, p \ge 0 \Rightarrow |S_{n-1} - S_{m + p}| < \varepsilon, \text{ но } |S_{n + p} - S_{n - 1}| =
$$

$$
= |a_a + ... + a_{n+p} - (a_1 + ... + a_{n-1})| = |a_n + ... + a_n + p|.\ \blacksquare
$$

## Теорема (свойства сходящихся числовых рядов)
**Фор-ка.** Если $\sum\limits_{n=1}^{+\infty}a_n$ и $\sum\limits_{n=1}^{+\infty}b_n$ сходятся, то:
- $\sum\limits_{n=1}^{+\infty}a_n + b_n$ сходится, $\sum\limits_{n=1}^{+\infty}(a_n + b_n) = \sum\limits_{n=1}^{+\infty}a_n + \sum\limits_{n=1}^{+\infty}b_n$
- $\sum\limits_{n=1}^{+\infty}\lambda a_n$, где $\lambda \in \mathrm{R}$ сходится, $\sum\limits_{n=1}^{+\infty}\lambda a_n = \lambda \sum\limits_{n=1}^{+\infty}a_n$

**Док-во.** Пусть $A_n = \sum\limits_{k=1}^na_k, B_n = \sum\limits_{k=1}^nb_k \Rightarrow A_n + B_n = \sum\limits_{k=1}^na_k + \sum\limits_{k=1}^nb_k = \sum\limits_{k=1}^n(a_k + b_k)$ - $n$-ая часть суммы ряда $\sum\limits_{n=1}^{+\infty}(a_n + b_n)$, а по теореме о пределе $\exists\lim\limits_{n\to +\infty}(A_n + B_n) = A + B.\ \blacksquare$

**Определение.** Ряд $\sum\limits_{k=n + 1}^{+\infty}a_k$ называется $n$-ым остатком $\sum\limits_{n=1}^{+\infty}a_n$.

## Теорема
**Фор-ка.** Если ряд сходится, то сходятся все его остатки и обратно. $\blacksquare$

**Следствие.** Отбрасывание конечного числа членов ряда или добавление в начало не влияет на сходимость ряда.

# Ряды с неотрицательными членами

## Теорема
**Фор-ка.**
Пусть $\sum\limits_{n=1}^{+\infty}a_n,\ a_n \ge 0, \forall n$, ряд сходится $\Leftrightarrow \exists M > 0: \sum\limits_{k=1}^na_k \le M, \forall n$

**Док-во.**
$S_n = \sum\limits_{n=1}^{+\infty}a_n, S_{n+1} = S_n + a_{n+1} \ge S_n \Rightarrow \{S_n\}_{n \in \mathrm{N}}$ - неотрицательно $\Rightarrow \exists\lim\limits_{n\to+\infty}S_n \Leftrightarrow \{S_n\}_{n \in \mathrm{N}}$ - ограничено сверху. $\blacksquare$

## Теорема (признак сравнения)
**Фор-ка.** Пусть $\sum\limits_{n=1}^{+\infty}a_n, \sum\limits_{n=1}^{+\infty}b_n, a_n = O(b_n) \Rightarrow$ если $\sum\limits_{n=1}^{+\infty}b_n$ сходится $\Rightarrow \sum\limits_{n=1}^{+\infty}a_n$ сходится

**Док-во.** $a_n = O(b_n) \Rightarrow \exists n_0 \in \mathrm{N}, \exists c > 0: a_n \le C\cdot b_n, \forall n \ge n_0.$

$\sum\limits_{n=1}^{+\infty}b_n$ сходится $\Rightarrow \sum\limits_{k=n_0+1}^{+\infty}b_k$ - сходится $\Rightarrow \exists M > 0: \sum\limits_{k=n_0+1}^{n_0 + n}b_k \le M, \forall n \Rightarrow \sum\limits_{k=n_0+1}^{n_0 + n}a_k \le \sum\limits_{k=n_0+1}^{n_0 + n}c\cdot b_k \le c \cdot M, \forall n \Rightarrow \sum\limits_{k=n_0+1}^{+\infty}a_k$ сходится $\Rightarrow \sum\limits_{n=1}^{+\infty}a_n$ сходится. $\blacksquare$

## Следствие
**Фор-ка.** Пусть $\sum\limits_{n=1}^{+\infty}a_n, \sum\limits_{n=1}^{+\infty}b_n, \exists \lim\limits_{n\to+\infty}\dfrac{a_n}{b_n} = k$, тогда:

1. при $0 \le k < +\infty$ из сходимости $\sum\limits_{n=1}^{+\infty}b_n$ следует сходимость $\sum\limits_{n=1}^{+\infty}a_n$
2. при $0 < k \le +\infty$ из расходимости $\sum\limits_{n=1}^{+\infty}b_n$ следует сходимость $\sum\limits_{n=1}^{+\infty}a_n$
3. при $0 < k < +\infty$ оба ряда сходятся или расходятся

**Док-во.**

1. $0 \le k < +\infty$, $k = \lim\limits_{n\to+\infty}\dfrac{a_n}{b_n}$, возьмем $\varepsilon = 1 \Rightarrow \exists n_0 \in \mathrm{N}, \forall n > n_0 \Rightarrow |\dfrac{a_n}{b_n} - k| < 1 \Rightarrow \dfrac{a_n}{b_n} < k + 1 \Rightarrow a_n < (k+1)d_n, \forall n > n_0 \Rightarrow a_n = O(b_n) \Rightarrow$ из сходимости $\sum\limits_{n=1}^{+\infty}b_n$ следует сходимость $\sum\limits_{n=1}^{+\infty}a_n$
2. $0 < k \le +\infty$
   1. $k$ - число $\Rightarrow \varepsilon = \dfrac{k}{2} \Rightarrow \exists n_0 \cdot \forall n > n_0 \Rightarrow |\dfrac{a_n}{b_n} - k| < \dfrac{k}{2} \Rightarrow \dfrac{a_n}{b_n} > \dfrac{k}{2} > 0$
   2. $k = +\infty \Rightarrow \varepsilon = 1 \Rightarrow \exists n_0 \cdot \forall n > n_0 \Rightarrow\dfrac{a_n}{b_n} > 1$

    Следовательно $\dfrac{a_n}{b_n} > c > 0 \Rightarrow b_n < \dfrac{1}{c}a_n \Rightarrow b_n = O(a_n)$, следовательно, так как $\sum\limits_{n=1}^{+\infty}b_n$ расходится $\Rightarrow \sum\limits_{n=1}^{+\infty}a_n$ расходится по сравнительному признаку. $\blacksquare$

## Теорема (признак Даламбера)
**Фор-ка.** $\sum\limits_{n=1}^{+\infty}a_n, \forall n \in \N$, если $\dfrac{a_{n+1}}{a_n} \le k \lt 1, \forall n \Rightarrow$ ряд сходится, если $\dfrac{a_{n+1}}{a_n} \ge 1, \forall n \Rightarrow$ ряд сходится

**Док-во.**

1. $\dfrac{a_{n+1}}{a_n} \le k \lt 1 \Rightarrow a_n = \dfrac{a_n}{a_{n-1}} \cdot ... \cdot \dfrac{a_2}{a_1}\cdot a_1 \le k^{n-1}\cdot a_1 = b_n$

   $\sum\limits_{n=1}^{+\infty}b_n = a_1\sum\limits_{n=1}^{+\infty}k^{n-1} = a_1\dfrac{1}{1-k}$
2. $\dfrac{a_{n+1}}{a_n} \ge 1 \Rightarrow a_{n+1}\ge a_n \Rightarrow a_n \ge ... \ge a_1 \lt 0 \Rightarrow a_n \ge a_1, \forall n \Rightarrow \lim\limits_{n\to +\infty}a_n \ne 0.\ \blacksquare$

## Следствие
**Фор-ка.** Дан ряд $\sum\limits_{n=1}^{+\infty}a_n, \exists \lim\limits_{n\to +\infty}\dfrac{a_{n+1}}{a_n}=k$, тогда, если $k \lt 1\Rightarrow$ ряд сходится, $k \gt 1\Rightarrow$ ряд расходится

**Док-во.**
1. $k \lt 1: r \in (k, 1), \varepsilon = r - k > 0 \Rightarrow \exists n_0 \in \N, \forall n \gt n_0: \Big|\dfrac{a_{n+1}}{a_n} - k\Big| \lt r - k\Rightarrow \dfrac{a_{n+1}}{a_n} \lt r \lt 1, \forall n \gt n_0 \Rightarrow$ ряд сходится по Даламберу.
2. $k \gt 1:$
   - $1 \lt k \lt +\infty \Rightarrow r \in (1, k) \Rightarrow \varepsilon = k - r \Rightarrow \exists n_0 \in \N:$

        $\forall n \lt n_0: \Big|\dfrac{a_{n+1}}{a_n} - k\Big| \lt k - r \Rightarrow r - k \lt \dfrac{a_{n+1}}{a_n} - k \Rightarrow 1 \lt r \lt \dfrac{a_{n+1}}{a_n} \Rightarrow$ расходится по Даламберу
    - $k=+\infty\Rightarrow\varepsilon = 1, ...$ - дз. $\blacksquare$

