# 📘 Guida Completa all’Esecuzione delle Query SQL

## 📌 Introduzione

Il linguaggio SQL (Structured Query Language) è utilizzato per **interrogare, manipolare e gestire dati** in un sistema di gestione di basi di dati relazionali (RDBMS). Capire come funziona **l’esecuzione di una query** è essenziale per scrivere codice efficiente, scalabile e corretto.

---

## 🧠 Ordine Logico di Esecuzione di una Query SQL

### ❗️ Attenzione: l’ordine con cui si scrive una query SQL **non corrisponde** all’ordine in cui il database la esegue.

### 🔄 Ordine Logico Interno (Execution Flow)

1. **FROM**  
   Identifica la tabella di partenza, applica JOIN ed eventuali alias.

2. **ON**  
   Definisce le condizioni dei JOIN.

3. **JOIN**  
   Unisce i dati di più tabelle.

4. **WHERE**  
   Filtra le righe sulla base di condizioni booleane.

5. **GROUP BY**  
   Raggruppa i dati secondo una o più colonne.

6. **HAVING**  
   Filtra i gruppi ottenuti da `GROUP BY`.

7. **SELECT**  
   Seleziona le colonne da restituire, calcola espressioni e aggregazioni.

8. **DISTINCT**  
   Rimuove i duplicati dai risultati.

9. **ORDER BY**  
   Ordina le righe in base a una o più colonne.

10. **LIMIT / OFFSET**  
    Limita il numero di righe restituite (paginazione).

---

## ✍️ Ordine Sintattico: Come si Scrive una Query

```sql
SELECT nome, COUNT(*) as totale
FROM utenti
WHERE attivo = 1
GROUP BY nome
HAVING COUNT(*) > 10
ORDER BY totale DESC
LIMIT 10;
