# Algoritmi e Strutture Dati — Appello del 1 settembre 2026

Questa cartella contiene i testi dell'appello del  
**1 settembre 2026** del corso di Algoritmi e Strutture Dati.

## Fonte

Questo appello non risulta disponibile nella pagina ufficiale degli appelli passati.
Non sono presenti le mie soluzioni per questo appello.

## Stato delle soluzioni

| Problema | Argomento principale | Stato |
|---|---|---|
| Domanda A | Definizione classe Ω e ricorrenza | [Da Completare] |
| Domanda B | Doppio Hashing | [Da Completare] |
| Esercizio 1 | ABR Equilibrato | [Da Completare] |
| Esercizio 2 | Esercizio Greedy | [Da Completare] |

---

## Domanda A (6 punti)

Definire formalmente la classe $\Omega(f(n))$. Dimostrare che la seguente ricorrenza ha soluzione $T(n)=\Omega(n)$

$$
T(n)=\frac{1}{3}T(n-1)+2n+1
$$

---

## Domanda B (6 punti)

Si consideri una tabella hash di dimensione $m=8$, e indirizzamento aperto con doppio hash basato sulle funzioni

$$
h_1(k)=k \bmod m
$$

e

$$
h_2(k)=1+2*(k \bmod (m-1)).
$$

Si descriva in dettaglio come avviene l’inserimento della sequenza di chiavi:

$$
26,\ 20,\ 42,\ 31,\ 71.
$$

Potremmo anche usare un doppio hash basato su $h_1$ e

$$
h'_2(k)=2+2*(k \bmod (m-1))?
$$

---

## Esercizio 1 (9 punti)

Un albero binario $T$ con chiavi numeriche non-negative si dice *equilibrato* se ogni nodo $x$ con chiave $k$ ha discendenti con chiavi non superiori a $2 \cdot k$.

Ad esempio, l’albero di sinistra è equilibrato, mentre quello di destra non lo è, ad esempio perché il nodo 2 ha come discendente 5.

**Albero di sinistra:**

```text
        4
       / \
      3   5
     / \   \
    6   1   2
```

**Albero di destra:**

```text
        2
       / \
      3   3
     / \   \
    6   1   5
```

Realizzare una funzione booleana `eq1(T)` che dato un albero binario $T$, con chiavi non negative, verifica se $T$ è o meno equilibrato. Dare lo pseudocodice, motivare la correttezza e valutarne la complessità. Si assuma che $T$ abbia radice `T.root` e nodi $x$ con campi `x.l` e `x.r` per figlio sinistro e destro, rispettivamente, e `x.k` per la chiave.

---

## Esercizio 2 (10 punti)

Dato un insieme di $n$ numeri reali positivi e distinti

$$
S=\{a_1,a_2,\ldots,a_n\},
$$

con

$$
0<a_i<a_j<1 \text{ per } 1\leq i<j\leq n,
$$

un $(2,1)$-*boxing* di $S$ è una partizione

$$
P=\{S_1,S_2,\ldots,S_k\}
$$

di $S$ in $k$ sottoinsiemi (cioè,

$$
\bigcup_{j=1}^{k}S_j=S
$$

e

$$
S_r\cap S_t=\emptyset,\quad 1\leq r\neq t\leq k
$$

) che soddisfa i seguenti vincoli:

$$
|S_j|\leq 2
\qquad\text{e}\qquad
\sum_{a\in S_j}a\leq 1,\quad 1\leq j\leq k.
$$

In altre parole, ogni sottoinsieme contiene al più due valori la cui somma è al più uno. Dato $S$, si vuole determinare un $(2,1)$-boxing che minimizza il numero di sottoinsiemi della partizione.

**(a)** Progettare un algoritmo greedy che restituisce un $(2,1)$-boxing ottimo in tempo lineare.
(Suggerimento: si creino i sottoinsiemi in modo opportuno basandosi sulla sequenza ordinata.)

**(b)** Enunciare e dimostrare la proprietà di scelta greedy su cui l’algoritmo si basa.
