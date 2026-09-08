# Reasoning e RAG con un modello LLM

Questo progetto è stato realizzato come esercitazione sui principali argomenti affrontati nel modulo dedicato ai Large Language Model.

L'obiettivo non è costruire un'applicazione completa, ma mettere insieme in un'unica pipeline alcuni concetti: caricamento di un modello quantizzato, prompt engineering, reasoning, RAG, classificazione zero-shot e output JSON.

## Cosa fa il notebook

Il notebook:

- carica un modello instruction da Hugging Face;
- usa la quantizzazione a 4 bit quando è disponibile una GPU NVIDIA;
- crea una piccola knowledge base testuale;
- divide il testo in chunk;
- genera gli embedding con `all-MiniLM-L6-v2`;
- indicizza i vettori con FAISS;
- recupera i chunk più pertinenti rispetto a una domanda;
- usa il contesto recuperato per generare una risposta;
- esegue una semplice sentiment analysis zero-shot;
- prova a restituire il risultato della sentiment analysis in JSON valido;
- mostra un esempio di streaming dell'output.

## Modello utilizzato

Per rendere l'esercitazione facilmente eseguibile su Google Colab ho usato `Qwen/Qwen2.5-1.5B-Instruct`, che è più leggero e non richiede l'accettazione di una licenza sul repository Hugging Face.

La logica della pipeline rimane la stessa richiesta dalla traccia: il modello può essere sostituito con Llama 3 modificando il valore di `MODEL_ID`, a condizione di avere accesso al repository Hugging Face e memoria GPU sufficiente.

## Esecuzione

Il modo più semplice è aprire il notebook in Google Colab e selezionare una GPU dal menu Runtime.

Le celle sono pensate per essere eseguite in ordine. La prima installa le dipendenze, le successive caricano il modello, preparano il RAG ed eseguono alcuni test finali.

## Struttura

- `progetto_reasoning_rag.ipynb`: notebook principale
- `knowledge_base.md`: piccolo documento usato dal sistema RAG
- `requirements.txt`: dipendenze Python

## Note

Il progetto ha volutamente una struttura semplice. Lo scopo è verificare il funzionamento dei vari passaggi senza introdurre framework aggiuntivi che non sono necessari per questa esercitazione.
