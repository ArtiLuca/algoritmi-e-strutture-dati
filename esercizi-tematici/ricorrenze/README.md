# Limiti Asintotici e Ricorrenze

[← Torna agli esercizi tematici](../README.md) · [Torna alla raccolta principale](../../README.md)

Esercizi vari su:

- Soluzione ricorrenze con metodo di sostituzione
- Soluzione ricorrenze con master theorem
- Soluzione ricorrenze con ipotesi di soluzione mediante albero delle ricorrenze
- Dimostrazioni formali su proprieta notazioni asintotica

---

## Stato delle soluzioni

| Esercizio | Stato |
|---|---|
| Domanda 1 — `T(n) = 4T(n/2) + n log n` | Da completare |
| Domanda 2 — `T(n) = T(n/2) + T(n/4) + n` | Da completare |
| Domanda 3 — `T(n) = 4T(n/2) + n√n` | Da completare |
| Domanda 4 — `T(n) = T(n - 2) + 2n` | Da completare |
| Domanda 5 — Ricorrenza esatta con `T(n - 1) + 2` | Da completare |
| Domanda 6 — `3T(n/5) + T(n/6) + n` | [Completato](domanda_6.md) |
| Domanda 7 — `5T(⌊n/3⌋) + 2n²` | [Completato](domanda_7.md) |
| Domanda 8 — `T(n) = T(n - 1) + log n` | [Completato](esercizio_8.md) |
| Domanda 9 — `T(n/2) + T(√n/2) + 2n` | [Completato](domanda_9.md) |
| Domanda 10 — `T(4n/5) + n/2 + log n` | [Completato](domanda_10.md) |
| Domanda 11 — `1/2 T(n - 1) + n` | [Completato](domanda_11.md) |
| Domanda 12 — Definizione di Ω e ricorrenza con sommatoria | [Completato](domanda_12.md) |
| Domanda 13 — Definizione di O e ricorrenza `2/3 T(n - 1) + 2n` | [Completato](esercizio_13.md) |
| Domanda 14 — `3T(n/2) + n(n + 1)` | [Completato](domanda_14.md) |
| Domanda 15 — `T(n/2) + T(n/3) + √n + 2` | [Completato](domanda_15.md) |
| Domanda 16 — `5T(n/3) + (n - 2)²` | [Completato](domanda_16.md) |
| Domanda 17 — Transitività di Ω | [Completato](domanda_17.md) |
| Domanda 18 — Relazione tra Θ, O e Ω | Da completare |
| Domanda A — Ricorrenza `T(n)=4T(n/2)+n^3+1` | [Completato](ricorrenza_master_theorem_domanda_A.md) |
| Domanda A — Ricorrenza `T(n)=T(n-1)+2n-1` | Da completare |
| Domanda A — Proprietà di `Θ(g(n))` | [Completato](domanda_classe_theta.md) |
| Domanda A — Proprietà di `Θ(g(n))` | [Completato](domanda_classe_theta.md) |
| Domanda A - Proprietà di classi $\mathcal{O}$ e $\Omega$ | [Completato](notazione_asintotica_dimostrazione_domanda_A.md) |
| Esercizio Ricorrenze (Sostituzione & Master Theorem) | [Completato](esercizio_ricorrenze_sostituzione_master.md) |
| Domanda A - Domanda Classe Omega | [Completato](domanda_classe_omega.md) |
| Domanda A — Classe $\Omega$ | [Completato](notazione_asintotica_dimostrazione_domanda_B.md) | 
| Domanda A — Ricorrenza con metodo di sostituzione | [Completato](domanda_ricorrenza_sostituzione.md) |
| Domanda A — Ricorrenze e classe Ω esponenziale | [Completato](domanda_ricorrenza_esponenziale.md) |
| Domanda A - Ricorrenza con Master Theorem | [Completato](domanda_master_theorem.md) |
| Domande - Proprieta Notazione Asintotica | [Completato](domanda_proprieta_notazione_asintotica.md) |
| Esercizi - Albero delle Ricorrenze | [Completato](esercizio_albero_ricorrenze.md) |
| Esercizi - Ricorrenze Metodo di Sostituzione | [Completato](esercizio_ricorrenze_metodo_sostituzione.md) |
| Esercizi - Ricorrenze Master Theorem | [Completato](esercizio_ricorrenze_master_theorem) |

---

## Testi degli Esercizi

### **Domanda 1**

Risolvere la ricorrenza $T(n) = 4 T(n/2) + n \log n$ utilizzando il master theorem.

---

### **Domanda 2**

Mostrare che la ricorrenza $T(n) = T(n/2) + T(n/4) + n$ ammette soluzione $T(n) = \Theta(n)$ utilizzando il metodo di sostituzione.

---

### **Domanda 3**

Risolvere la ricorrenza $T(n) = 4T(n/2) + n\sqrt{n}$ utilizzando il master theorem.

---

### **Domanda 4**

Risolvere la ricorrenza $T(n) = T(n - 2) + 2n$ utilizzando il metodo di sostituzione per dimostrare un limite asintotico stretto.

---

### **Domanda 5**

Risolvere la ricorrenza

$$
T(n) = \begin{cases} 3 & \text{se } n = 0 \\ T(n - 1) + 2 & \text{se } n > 0 \end{cases}
$$

utilizzando il metodo di sostituzione per determinare una soluzione esatta (non asintotica).

---

### **Domanda 6**

Sia data la seguente equazione di ricorrenza:

$$
T(n) = \begin{cases} 1 & \text{se } n = 1 \\ 3T(n/5) + T(n/6) + n & \text{se } n > 1 \end{cases}
$$

Si fornisca un limite asintotico stretto per la soluzione.

---

### **Domanda 7**

Sia data la seguente equazione di ricorrenza:

$$
T(n) = 5T(\lfloor n/3 \rfloor) + 2n^2
$$

Si fornisca un limite asintotico stretto per la soluzione.

---

### **Domanda 8**

Sia data la seguente equazione di ricorrenza:

$$
T(n) = T(n - 1) + \log n
$$

Si dimostri che $T(n) = \mathcal{O}(n \log n)$.

---

### **Domanda 9**

Sia data la seguente equazione di ricorrenza:

$$
T(n) = T(n/2) + T(\sqrt{n}/2) + 2n
$$

Si dimostri che $T(n) = \Theta(n)$.

---

### **Domanda 10**

Si consideri la ricorrenza

$$
T(n) = T\left(\frac{4n}{5}\right) + \frac{n}{2} + \log n
$$

Fornire limite asintotico stretto per la soluzione.

---

### **Domanda 11**

Si dimostri che la ricorrenza che segue ha soluzione $T(n) = \Theta(n)$

$$
T(n) = \frac{1}{2}T(n - 1) + n
$$

---

### **Domanda 12**

Dare la definizione di $\Omega(f(n))$. Dimostrare che la ricorrenza che segue ha soluzione $T(n) = \Omega(2^n)$

$$
T(n) = \sum_{k=1}^{n-1} T(k) T(n - k)
$$

---

### **Domanda 13**

Dare la definizione di $\mathcal{O}(f(n))$. Dimostrare che la ricorrenza che segue ha soluzione $T(n) = \mathcal{O}(n)$

$$
T(n) = \frac{2}{3}T(n - 1) + 2n
$$

---

### **Domanda 14**

Dare una soluzione asintotica per la ricorrenza $T(n) = 3T(n/2) + n(n + 1)$.

---

### **Domanda 15**

Data la ricorrenza $T(n) = T(n/2) + T(n/3) + \sqrt{n} + 2$ dimostrare che ha soluzione $T(n) = \mathcal{O}(n)$. Il limite è stretto, ovvero vale anche $T(n) = \Omega(n)$?

---

### **Domanda 16**

Data la ricorrenza $T(n) = 5T(n/3) + (n - 2)^2$, trovare la soluzione asintotica.

---

### **Domanda 17**

Dare la definizione di $\Omega(f(n))$. Mostrare che se $f(n) = \Omega(g(n))$ e $g(n) = \Omega(h(n))$ allora $f(n) = \Omega(h(n))$.

---

### **Domanda 18**

Dare la definizione di $\Theta(f(n))$. Mostrare che $\Theta(f(n)) = \mathcal{O}(f(n)) \cap \Omega(f(n))$.

---

### Domanda A — 6 punti

Dare una soluzione asintotica per la ricorrenza

$$
T(n)=4T(n/2)+n^3+1.
$$

---

### Domanda A — 7 punti

Risolvere la seguente ricorrenza

$$
T(n)=T(n-1)+2n-1
$$

fornendo un limite asintotico stretto per la soluzione.

Individuare una ipotesi di soluzione e quindi utilizzare il metodo di sostituzione per dimostrarne la correttezza.

---

### Domanda A — 8 punti

Definire formalmente la classe $\Theta(g(n))$.

Dimostrare le seguenti affermazioni o fornire un controesempio:

1. se $f(n),f'(n)\in\Theta(g(n))$ allora

$$
f(n)+f'(n)\in\Theta(g(n));
$$

2. $f(n),f'(n)\in\Theta(g(n))$ allora

$$
f(n)\cdot f'(n)\in\Theta(g(n)).
$$

---

### Domanda A — Classi $\mathcal{O}$ e $\Omega$

Dare la definizione formale delle classi $\mathcal{O}(f(n))$ e $\Omega(f(n))$ per una funzione $f(n)$.
Mostrare che se $f(n) = \mathcal{O}(n)$ e $g(n) = n^2 - f(n),$ allora $g(n) = \Omega(n^2)$.

---

### Esercizio Ricorrenze (Sostituzione & Master Theorem)

1. Dimostrare che la ricorrenza $T(n) = T(n/2) + T(n/4) + n$ ammette soluzione $\Theta(n)$
2. Trovare un'ipotesi per $T(n) = T(n-2) + 2n$ e dimostrare con sostituzione
3. Master Theorem per $T(n) = 4T(n/2) + n\log n$
4. Master Theorem per $T(n) = 4T(n/2) + n^2\sqrt{n}$

---

### Domanda A — Dimostrazione Formale con Notazione Asintotica

Definire formalmente la classe $\mathcal{O}(g(n))$.
Dimostrare oppure confutare le seguenti affermazioni.

- **(i)** Se $f(n) = \mathcal{O}(g(n))$ e $h(n) = \mathcal{O}(g(n))$, allora $f(n) + h(n) = \mathcal{O}(g(n))$.
- **(ii)** Se $f(n) = \mathcal{O}(g(n))$, allora $2^{f(n)} = \mathcal{O}(2^{g(n)})$.

Per ciascuna affermazione, fornire una dimostrazione usando la definizione formale oppure un controesempio.

---

### Domanda A — Classe $\Omega$

Assumendo che $f(n) = \Omega(n^2)$, si dimostri se la seguente affermazione è vera:
$$f(n) + g(n) = \Omega(n^2 + g(n))$$
Vale anche la seguente?
$$f(n) - g(n) = \Omega(n^2 - g(n))$$
Dimostrarlo oppure fornire un controesempio.

---

### Domanda A — Ricorrenza con metodo di sostituzione

Si dimostri che la ricorrenza che segue ha soluzione $T(n)=\Theta(n)$:

```math
T(n)=\frac{2}{3}T(n-1)+2n.
```

---

### Domanda A — Ricorrenze e classe Ω esponenziale

Data la ricorrenza:

$$ 
T(n) = \frac{3}{2}T(n-1) + 2 
$$

mostrare che la soluzione è $O(2^n)$.

Vale anche $T(n) = \Omega(2^n)$? Motivare la risposta.

---

### Domanda A - Ricorrenza con Master Theorem

Si determini la soluzione asintotica della seguente equazione di ricorrenza:

```math
T(n)=3T(n/3)+n^2+1.
```

---

### Proprietà Notazione Asintotica

**Dimostrare le seguenti uguaglianze:**

1. $f(n) = \mathcal{O}(g(n))$ sse $g(n) = \Omega(f(n))$
2. $\Theta(g(n)) = \mathcal{O}(g(n)) \cap \Omega(g(n))$
3. $f(n) = \Theta(f(n))$
4. $f(n) = \Theta(g(n))$ sse $\Theta(f(n)) = \Theta(g(n))$ sse $g(n) = \Theta(f(n))$
5. $f(n) = \mathcal{O}(g(n))$ e $g(n) = \mathcal{O}(h(n))$ implica $f(n) = \mathcal{O}(h(n))$

---

### Esercizi - Albero delle Ricorrenze

Usare l'albero delle ricorrenze per dare un'ipotesi di soluzione e poi dimostrare con il metodo di sostituzione:

- $T(n) = T(n/2) + n^3$
- $T(n) = 4T(n/3) + n$
- $T(n) = 4T(n/2) + n$
- $T(n) = 3T(n-1) + 1$

---

### Ricorrenze Master Theorem

Dimostrare le seguenti ricorrenze utilizzando il master theorem:

1. $T(n) = 2T(n/4) + 1$
2. $T(n) = 2T(n/4) + \sqrt{n}$
3. $T(n) = 2T(n/4) + \sqrt{n}\log^2n$
4. $T(n) = 2T(n/4) + n$
5. $T(n) = 2T(n/4) + n^2$
