# Divide et Impera e Ricorsione

[← Torna agli esercizi tematici](../README.md) · [Torna alla raccolta principale](../../README.md)

Esercizi vari su ricorsione usando tecnica *divide-et-impera*. 

---

## Stato delle soluzioni

| Esercizio | Stato |
|---|---|
| Esercizio 1 — Gap in un array | Da completare |
| Esercizio 2 — Primo elemento strettamente maggiore di `x` | [Completato](over.md) |
| Esercizio 3 — Massimo con divide et impera | [Completato](massimo.md) |
| Esercizio 4 — Indice fisso in array ordinato | [Completato](fix.md) |
| Domanda 19 — Sottosequenza ricorsiva | [Completato](subseq.md) |
| Esercizio 5 — Array alternante | [Completato](alt.md) |
| Esercizio - Indice stabile in array ordinato | [Completato](stab.md) |
| Esercizio 1 — Split con divide et impera | [Completato](split.md) | 
| Esercizio 1 - Missing Divide-et-Impera | [Completato](missing.md) |
| Esercizio - Centro di array semi-ordinato | [Completato](esercizio_centre.md) |
| Esercizio - Conteggio delle Inversioni | [Completato](esercizio_inversioni.md) |

---

## Testi degli Esercizi


### **Esercizio 1**

Dato un array di interi `A[1..n]`, chiamiamo *gap* un indice $i \in [1, n)$ tale che $A[i + 1] - A[i] > 1$.

- **i.** Mostrare per induzione su $n$ che un array `A[1..n]` tale che $A[n] - A[1] \ge n$ (quindi $n \ge 2$) contiene almeno un *gap*.
- **ii.** Fornire lo pseudocodice di una procedura ricorsiva *divide et impera* `gap` che dato un array `A[1..n]` tale che $A[n] - A[1] \ge n$ restituisce un *gap* in `A`.
- **iii.** Valutare la complessità della funzione, utilizzando il master theorem.

---

### **Esercizio 2**

Scrivere una procedura di tipo *divide et impera* `over` che dato un array di interi distinti `A[1..n]`, ordinato in modo crescente, e un intero $x$ restituisce l'indice del più piccolo elemento in `A` strettamente maggiore di $x$. Se nessun elemento di `A` soddisfa la condizione, si restituisca $n + 1$. Valutare la complessità dell'algoritmo.

---

### **Esercizio 3**

Realizzare una procedure di tipo *divide et impera* `Max(A, p, r)` per trovare il massimo nell'array `A[p..r]`. Si assuma che l'array non sia vuoto ($p \le r$). Scrivere lo pseudocodice e valutare la complessità con il master theorem.

---

### **Esercizio 4**

Sia `A[1..n]` un array di interi distinti ordinato in senso crescente. Dimostrare che dato un qualunque indice $i$, se $A[i] > i$ allora $A[j] > j$ per ogni $j > i$ e analogamente se $A[i] < i$ allora $A[j] < j$ per ogni $j < i$.
Utilizzare l'osservazione per realizzare una funzione `Fix(A)` che dato l'array di interi `A[1..n]` ordinato senza ripetizioni restituisce un indice $i$ tale che $A[i] = i$, se esiste, e 0 altrimenti. Valutarne la complessità.

---

### **Domanda 19**

Scrivere una funzione ricorsiva `subseq(X, Y, m, n)` che date due sequenze `X[1..m]` e `Y[1..n]`, di lunghezza $m$ e $n$ rispettivamente, verifica se `X` è una sottosequenza di `Y` e restituisce un valore booleano conseguente. Valutarne la complessità.

---

### **Esercizio 5**

Un array `A[1..n]` di numeri si dice *alternante* se non ha elementi contigui identici (ovvero per ogni $i \le n-1$ vale $A[i] \ne A[i+1]$) e inoltre per ogni $i \le n-2$, vale che $a_i < a_{i+1} > a_{i+2}$ oppure $a_i > a_{i+1} < a_{i+2}$. Ad esempio gli array `[1, 2, -1, 3, 2]` e `[5, 1, 2, -1, 3, 2]` sono alternanti, mentre non lo sono `[1, 2, 3]` e `[1, 1, 2]`. Scrivere una funzione ricorsiva `alt(A, n)` che dato un array `A[1..n]` di numeri verifica se è alternante. Valutarne la complessità.

---

### Esercizio 1 — Indice stabile

Dato un array $A[1 \dots n]$ di interi, un indice $i$ si dice stabile se $A[i] = i$.
Realizzare una procedura `stab(A, n)` che, dato in input un array $A[1 \dots n]$ di interi distinti, ordinato in modo crescente, ritorna un indice stabile, se esiste, e ritorna $0$ altrimenti.
Dimostrarne la correttezza e valutarne la complessità.

---

## Esercizio 1 — Split con divide et impera

Sia dato un array $V[1..n]$ i cui valori rappresentano la variazione giornaliera del valore di un titolo azionario.

È noto che il titolo è stato prima in perdita, con valori sempre negativi, poi ha iniziato a oscillare in giorni consecutivi tra valori positivi e negativi, e infine si è stabilizzato su valori positivi. Dunque nella sequenza **non possono esserci due giorni positivi seguiti da un negativo**.

Realizzare un algoritmo divide et impera `Split(V)` che individua il giorno in cui il titolo ha iniziato a essere stabile su valori positivi, ovvero il minimo indice

$$
i \in [1,n]
$$

tale che

$$
\forall j \ge i,\quad V[j] > 0.
$$

Se il titolo non si stabilizza su valori positivi, ritornare `0`.

Esempi:

- per $V=[-1,-2,2,-1,6,3]$ si deve ritornare $5$;
- per $V=[-1,-2,2,-1,6,-3]$ si deve ritornare `0`.

Fornire lo pseudocodice di `Split(V)`, motivarne la correttezza e individuarne la complessità. Si assuma che non ci siano valori nulli.

---

### Esercizio 1 — Missing(A,n)

Sia dato un array $A[1..n]$ ordinato in modo crescente, contenente $n$ interi distinti scelti dall'insieme $\{1, 2, \dots, n+1\}$. 
Esattamente un numero dell'insieme non compare in $A$.

Realizzare un algoritmo divide et impera `Missing(A, n)` che restituisca il numero mancante in tempo $\mathcal{O}(\log n)$.
Fornire pseudocodice, dimostrazione di correttezza e complessità.

---

### Centro di array semi-ordinato

Diciamo che un array senza ripetizioni $A[1 \dots n]$ è semi-ordinato se esiste un indice $k$, con:
$1 \le k < n$
tale che:
$[k+1 \dots n] \quad \text{e} \quad A[1 \dots k]$
siano ordinati, ovvero i sottoarray $A[k+1 \dots n]$ e $A[1 \dots k]$ sono ordinati e:
$A[n] < A[1]$

In questo caso l'indice $k$ viene detto il **centro** dell'array.
Ad esempio l'array che segue è semi-ordinato con centro $k=4$:

```text
 1  2   3   4   5  6  7
[4, 9, 12, 18, -1, 1, 2]
```

Scrivere una funzione `centre(A)` che, dato un array $A$ semi-ordinato, ne restituisce il centro. Giustificare la correttezza dell'algoritmo e valutarne la complessità.

---

### Conteggio delle inversioni

Realizzare con approccio divide et impera una funzione `Inv(A, p, r)` che ritorna il numero di inversioni in $A[p \dots r]$, ovvero il numero di coppie di indici $i,j$ tali che:

$$
i < j \quad \text{e} \quad A[i] > A[j]
$$

*Suggerimento: modificare il MergeSort.*

