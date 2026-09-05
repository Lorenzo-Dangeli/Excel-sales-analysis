# 🛒 POF (Planty of Food) - Business Intelligence & Analisi Vendite E-Commerce

## 📌 Panoramica del Progetto
Questo repository contiene l'analisi delle vendite e dei comportamenti d'acquisto per **POF (Planty of Food)**, un e-commerce focalizzato sulla distribuzione sostenibile di prodotti alimentari *plant-based* biologici, etici e a basso impatto ambientale in Italia[cite: 1].

L'obiettivo dell'elaborato Excel è trasformare i dati grezzi delle transazioni aziendali in **KPI azionabili** e **Business Intelligence**, identificando i reparti più redditizi, i picchi stagionali di vendita e la distribuzione geografica e per scontrino medio.

---

## 📂 Struttura della Cartella di Lavoro (Workbook)

Il file `Progetto Excel di Lorenzo D'Angeli.xlsx` è strutturato in 3 fogli di lavoro interconnessi:

| Foglio di Lavoro | Descrizione e Contenuto |
| :--- | :--- |
| **`Food E-commerce Plant Based`** | Dataset principale contenente i dati delle transazioni (25 scontrini), la classificazione dell'importo, la logica di popolamento delle città e la sezione di audit con quesiti e formule implementate. |
| **`Città`** | Tabella di lookup di riferimento con la mappatura biunivoca tra *Provincia* e *Città* principale. |
| **`Pivot`** | Tabella Pivot multidimensionale che incrocia il fatturato aggregato per **Mese** (righe) e **Reparto** (colonne). |

---

## 📊 Key Performance Indicators (KPI) & Risultati Chiave

Dall'elaborazione analitica emergono i seguenti risultati chiave di performance:

* **Fatturato Totale Complessivo**: **€ 1.597,65** (su un totale di 25 transazioni registrate).
* **Scontrino Medio (AOV - Average Order Value)**: **€ 63,91**
  * Scontrino medio ordini > €20: **€ 74,22**
  * Scontrino medio ordini < €106: **€ 44,55**
* **Reparto Top Performer**: **Dispensa** con **€ 551,13** di incasso totale (pari a oltre il 34,5% delle vendite complessive).
* **Mese di Picco delle Vendite**: **Aprile** con un fatturato mensile di **€ 327,25**.
* **Ordini ad Alto Valore (> €100)**: **6 transazioni** identificate tramite formattazione condizionale.

---

## 🛠️ Tecniche e Formule Excel Utilizzate

Nel progetto sono state applicate le seguenti metodologie analitiche e sintassi di calcolo:

### 1. Funzioni Statistiche e Aritmetiche
* **Aggregazione Totale**: `=SOMMA(Importo Scontrino)` per il calcolo del volume d'affari totale.
* **Calcolo della Media**: `=MEDIA(Importo Scontrino)` per determinare l'AOV di riferimento (€ 63,91).
* **Media Condizionata**: `=MEDIA.SE()` per estrarre il valore medio stimato sugli ordini sopra la soglia dei 20€ e sotto i 106€.

### 2. Funzioni Logiche e di Conteggio Condizionato
* **Conteggio Monocriterio**: `=CONTA.SE()` per identificare la frequenza d'acquisto per specifica area geografica (es. 2 vendite a Latina).
* **Conteggio Multicriterio**: `=CONTA.PIÙ.SE()` per filtrare transazioni combinate (es. 6 vendite registrate a Roma nel mese di aprile).
* **Somma Condizionata**: `=SOMMA.SE()` per calcolare i ricavi specifici per reparto e periodo (es. € 250,85 per il reparto Dispensa a gennaio).
* **Classificazione Logica (IF)**: `=SE(Importo > 63,91; "Alto"; "Basso")` per la segmentazione automatica degli scontrini sopra o sotto la media.

### 3. Ricerca Dati e Formattazione
* **Integrazione Dati (VLOOKUP / CERCA.VERT)**: Popolamento dinamico della colonna *Città* effettuando il lookup della colonna *Provincia* dal foglio `Città`.
* **Formattazione Condizionale**: Evidenziazione visiva automatica per tutti gli scontrini con importo superiore a € 100,00.

---

## 📈 Analisi Multidimensionale (Tabella Pivot)

La tabella Pivot integrata nel terzo foglio analizza la ripartizione del fatturato per categoria merceologica:

| Reparto Prodotto | Fatturato Generato (€) | Quota sul Totale |
| :--- | :---: | :---: |
| **Dispensa** | € 551,13 | 34,5% |
| **Cereali** | € 351,85 | 22,0% |
| **Banco Frigo** | € 247,19 | 15,5% |
| **Bevande** | € 188,90 | 11,8% |
| **Vitamine e Integratori** | € 143,90 | 9,0% |
| **Ortofrutticolo** | € 114,68 | 7,2% |
| **TOTALE** | **€ 1.597,65** | **100,0%** |

---

## 🚀 Istruzioni per la Consultazione

1. Scaricare o clonare il repository.
2. Aprire il file `Progetto Excel di Lorenzo D'Angeli.xlsx` con Microsoft Excel o software compatibile.
3. Consultare le risposte dettagliate alle domande di audit direttamente nella colonna `Risposta` del foglio `Food E-commerce Plant Based`.
4. Navigare verso il foglio `Pivot` per esplorare la matrice dinamica delle vendite e il relativo grafico di sintesi temporale.
