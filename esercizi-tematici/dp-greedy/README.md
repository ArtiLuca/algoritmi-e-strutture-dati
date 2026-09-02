# Esercizi DP & Greedy da Esame

[← Torna agli esercizi tematici](../README.md) · [Torna alla raccolta principale](../../README.md)

Esercizi vari su:

- Programmazione dinamica con ricorrenza data (Bottom-Up, Memoizzazione)
- Esercizi Greedy su Activity Selection
- Esercizi Greedy su Scheduling
- Esercizi Greedy esecuzione file sequenziali
- Esercizi Greedy Coin Exchange
- Definizione ricorrenza LCS

---

## Stato delle soluzioni

| Esercizio | Stato |
|---|---|
| DP su stringhe con Memoization | [Completato](dp_stringhe_memoizzazione.md) |
| Domanda B - Activity Selection Greedy Sel | [Completato](greedy_sel.md) |
| Esercizio 2 - Selezioni di Attività Compatibili | [Completato](activity_selection.md) |
| Esercizio 2 - Scheduling greedy e somma dei tempi di completamento | [Completato](schedule_opt.md) |
| Domanda B — Longest Common Subsequence (LCS) | [Completato](domanda_LCS.md) |
| Esercizio 2 — Algoritmo greedy per il resto delle monete | [Completato](greedy_monete.md) |
| Esercizio 2 - Programmazione dinamica bottom-up | [Completato](esercizio_dp_bottom_up_esame.md) |
| Esercizio 2 — Programmazione dinamica (DP 2023) | [Completato](esercizio_dp_bottom_up_stringhe.md) |
| Esercizio 2 - Greedy Costo Minimo File Sequenziali | [Completato](esercizio_greedy_file.md) |
| Esercizio - DP Memoizzazione $M(i,j)$ | [Completato](esercizio_esame_memoizzazione.md) |

---

## Testi degli Esercizi


### Esercizio 2 - DP su stringhe con Memoization

Data una stringa $X = x_1, x_2, \dots, x_n$, si consideri la seguente quantità $\ell(i, j)$, definita per $1 \le i \le j \le n$:

$$
\ell(i, j) =
\begin{cases}
1 & \text{se } i = j \\
2 & \text{se } i = j - 1 \\
2 + \ell(i + 1, j - 1) & \text{se } i < j - 1 \text{ e } x_i = x_j \\
\sum_{k=i}^{j-1}(\ell(i,k) + \ell(k+1,j)) & \text{se } i < j - 1 \text{ e } x_i \ne x_j
\end{cases}
$$

- **(1)** Scrivere una coppia di algoritmi `INIT_L(X)` e `REC_L(i, j)` per il calcolo memoizzato di $\ell(1, n)$.
- **(2)** Si determini la complessità al caso migliore $T_{\text{best}}(n)$ supponendo che le uniche operazioni di costo unitario e non nullo siano i confronti tra caratteri.

---

### Domanda B - Activity Selection Greedy Sel

Si consideri il problema di selezione di attività compatibili:

**(a)** Definire il problema.

**(b)** Descrivere brevemente l'algoritmo ottimo `GREEDY-SEL` visto in classe.

**(c)** Fornire un esempio di algoritmo greedy *non* ottimo, motivandone la non
ottimalità.

---

### Esercizio 2 - Selezioni di Attività Compatibili

Si consideri il problema di selezione di attività compatibili, con $n$ attività
$a_1, \dots, a_n$ che ci vengono date attraverso due vettori $\mathbf{s}$ e $\mathbf{f}$ di
tempi di inizio e fine, e ordinate per tempo di *inizio*, cioè:

$$ 0 < s_1 \le s_2 \le \dots \le s_n $$

**(a)** Scrivere un algoritmo greedy iterativo che implementa la scelta greedy
di selezionare l'attività che inizia per ultima.

**(b)** Determinare l'insieme di attività restituito dall'algoritmo al punto
(a) quando eseguito sul seguente insieme di 6 attività, caratterizzate dai
seguenti vettori $\mathbf{s}$ e $\mathbf{f}$ di tempi di inizio e fine:

$$ \mathbf{s} = (1, 2, 3, 5, 7, 10) $$
$$ \mathbf{f} = (3, 9, 10, 7, 11, 12) $$

**(c)** Dimostrare la proprietà di scelta greedy, cioè che esiste soluzione
ottima che contiene l'attività che inizia per ultima.

---

### Esercizio 2 - Scheduling greedy e somma dei tempi di completamento

Abbiamo $n$ programmi da eseguire sul nostro computer. Ogni programma $j$, con:

```math
j \in \{1,2,\ldots,n\},
```

ha lunghezza $\ell_j$, che rappresenta la quantità di tempo richiesta per la sua
esecuzione.

Dato un ordine di esecuzione:

```math
\sigma = j_1,j_2,\ldots,j_n
```

dei programmi, cioè una permutazione di $\{1,2,\ldots,n\}$, il tempo di
completamento $C_{j_i}(\sigma)$ del programma $j_i$ è dato dalla somma delle
lunghezze dei programmi:

```math
j_1,j_2,\ldots,j_i.
```

L'obiettivo è trovare un ordine di esecuzione $\sigma$ che minimizza la somma dei
tempi di completamento di tutti i programmi, cioè:

```math
\sum_{j=1}^{n} C_j(\sigma).
```

### Punto (a)

Dare un semplice algoritmo greedy per questo problema, e valutarne la
complessità.

### Punto (b)

Dimostrare la proprietà di scelta greedy dell'algoritmo del punto (a), cioè che
esiste un ordine di esecuzione ottimo $\sigma^\star$ che contiene la scelta
greedy.

---


### Domanda B — Longest Common Subsequence (LCS)

Scrivere la ricorrenza sulle lunghezze $\ell(i,j)$ per il problema della longest
common subsequence (LCS).

---

### Esercizio 2 — Algoritmo greedy per il resto delle monete

Supponiamo di avere un numero illimitato di monete di ciascuno dei seguenti
valori: $\{50, 20, 1\}$. Dato un numero intero positivo $n$, l'obiettivo è selezionare il
più piccolo numero di monete tale che il loro valore totale sia $n$. Consideriamo
l'algoritmo greedy che consiste nel selezionare ripetutamente la moneta di
valore più grande possibile.

### Punto (a)

Fornire un valore di $n$ per cui l'algoritmo greedy non restituisce una
soluzione ottima.

### Punto (b)

Supponiamo ora che i valori delle monete siano $\{10, 5, 1\}$. In questo caso
l'algoritmo greedy restituisce sempre una soluzione ottima: dimostrare che ogni
insieme ottimo $M^\star$ di monete di valore totale $n$ contiene la scelta greedy.

---

### Esercizio 2 — Programmazione dinamica bottom-up

Date due stringhe $X = \langle x_1, x_2, \dots, x_m \rangle$ e $Y = \langle y_1, y_2, \dots, y_n \rangle$, si consideri la seguente quantità $\ell(i, j)$, definita per ogni coppia di valori $i, j$ con $0 \le i \le m$ e $0 \le j \le n$:

$$
\ell(i, j) =
\begin{cases}
1 & \text{se } i = 0 \text{ oppure } j = 0 \\
3 \cdot \ell(i, j - 1) & \text{se } i, j > 0 \text{ e } x_i = y_j \\
2 \cdot \ell(i - 1, j - 1) - \ell(i - 1, j) & \text{se } i, j > 0 \text{ e } x_i \ne y_j
\end{cases}
$$

Si vuole calcolare la quantità:

$$
q = \max \{ \ell(i, j) : 0 \le i \le m, 0 \le j \le n \}
$$

- **(a)** Scrivere un algoritmo bottom-up per il calcolo di $q$.
- **(b)** Determinare la complessità esatta dell'algoritmo, supponendo che le uniche operazioni di costo unitario e non nullo siano i confronti tra caratteri.

---

### Esercizio 2 — Programmazione dinamica (DP 2023)

Per $n > 0$, siano dati due vettori a componenti intere $a, b \in \mathbb{Z}^n$.
Si consideri la quantità $c(i, j)$ con $0 \le i \le j \le n-1$, definita come segue:

$$
c(i, j) =
\begin{cases}
a_i & \text{se } 0 < i \le n-1 \text{ e } j = n-1 \\
b_j & \text{se } i = 0 \text{ e } 0 \le j \le n-1 \\
c(i-1, j-1) \cdot c(i, j+1) & \text{se } 0 < i \le j < n-1
\end{cases}
$$

Si vuole calcolare la quantità:

$$
m = \max \{ c(i, j) : 0 \le i \le j \le n-1 \}
$$

- **(a)** Fornire un algoritmo iterativo bottom-up per il calcolo di $m$.
- **(b)** Valutare la complessità esatta dell’algoritmo, associando costo unitario alla moltiplicazione tra numeri interi e costo nullo a tutte le altre operazioni.

---

### Esercizio 2 — Greedy con Argomento di Scambio

Si hanno $n$ file memorizzati in sequenza. Il file $i$ ha dimensione $s_i > 0$ e probabilità di accesso $p_i > 0$.

Dato un ordine $\sigma$, il costo atteso di accesso è: 

$\sum_i p_i C_i(\sigma)$,

dove $C_i(\sigma)$ è la somma delle dimensioni dei file che precedono il file $i$ nell'ordine, più la dimensione del file $i$ stesso.

Trovare un ordinamento dei file che minimizzi il costo atteso.
Fornire la regola greedy, una dimostrazione tramite scambio di elementi adiacenti e la complessità.

---

### Ricorrenza memoizzata $M(i,j)$

Sia $n>0$. Si consideri la seguente ricorrenza $M(i,j)$ definita su tutte le coppie $(i,j)$ con $1\leq i\leq j\leq n$:

$$
M(i,j)=
\begin{cases}
1 & \text{se } i=j,\\
2 & \text{se } j=i+1,\\
M(i+1,j-1)\cdot M(i+1,j)\cdot M(i,j-1) & \text{se } j>i+1.
\end{cases}
$$

1. Scrivere una coppia di algoritmi `INIT_M(n)` e `REC_M(i,j)` per il calcolo memoizzato di $M(1,n)$.
2. Calcolare il numero esatto $T(n)$ di moltiplicazioni tra interi eseguite per il calcolo di $M(1,n)$.


