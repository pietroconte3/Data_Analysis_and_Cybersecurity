# Data Analysis & Cybersecurity

Questo repository contiene il progetto di ricerca sviluppato su Google Colab per il corso di **Data Analysis and Cybersecurity**, incentrato sull'applicazione del Class Incremental Learning (CIL) per i sistemi di rilevamento delle intrusioni di rete (NIDS) in ambienti IoT.

## 🎓 Informazioni sul Corso

* **Università:** Università degli Studi di Napoli Federico II
* **Corso di Laurea:** Laurea Magistrale
* **Corso:** Data Analysis and Cybersecurity
* **Autori:** Pietro Conte, Camilla D'Andria, Serena Savarese

---

## 🛡️ Progetto: Class Incremental Learning per IoT Intrusion Detection

Ricerca e sperimentazione su come i sistemi NIDS per IoT possano adattarsi continuamente a nuovi tipi di attacchi senza dimenticare quelli precedenti, mitigando il problema del *catastrophic forgetting*. Il progetto confronta approcci CIL standard su architetture CNN e Transformer, proponendo inoltre un adattamento del modello ROBUSTA per il dominio del traffico di rete IoT.

### 🔍 Fasi della Ricerca e Sperimentazione
*   **Confronto Architetturale:** Valutazione sistematica delle prestazioni tra reti neurali convoluzionali (2D CNN) e Transformer (ViT_CCT_TON) nell'ambito della classificazione del traffico di rete.
*   **Strategie di Mitigazione (CIL):** Implementazione e testing di diverse tecniche per il mantenimento della conoscenza, tra cui Bias Correction (BiC) e Memento, confrontate con l'approccio nativo per Transformer ROBUSTA.
*   **Scenari Incrementali:** Esecuzione di esperimenti su molteplici scenari di apprendimento incrementale basati sul dataset TON-IoT: aggiornamento singolo (+1 e +6) e sequenziale multistadio (+1+1+1+1+1+1).
*   **Few-Shot Learning:** Analisi delle performance in scenari di scarsità di dati (es. l'attacco `dos-tcp` con soli 153 campioni disponibili), dove l'approccio ROBUSTA ha dimostrato un'elevata plasticità ottenendo un F1 New del 97.4%.

---

## ⚙️ Tecnologie e Strumenti
*   **Architetture Deep Learning:** 2D CNN, Vision Transformer (ViT_CCT_TON), ROBUSTA.
*   **Metodi CIL & Distillazione:** Bias Correction (BiC), Memento, Knowledge Distillation, Prefix Tuning (Delta Parameters).
*   **Dataset & Data Processing:** TON-IoT (estrazione di 6 feature di intestazione dai primi 10 pacchetti per ogni biflow).
