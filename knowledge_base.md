# Piccola knowledge base per il progetto

L'intelligenza artificiale generativa usa modelli probabilistici che stimano quale token sia più probabile dopo quelli già presenti nella sequenza.

Il Retrieval-Augmented Generation, o RAG, permette di recuperare informazioni da documenti esterni prima della generazione della risposta. In questo modo il modello dispone di un contesto più pertinente e può ridurre alcune allucinazioni.

La quantizzazione a 4 bit consente di ridurre sensibilmente la memoria richiesta da un modello linguistico. È utile soprattutto quando si lavora con GPU consumer o ambienti come Google Colab.

Il Chain of Thought è una tecnica di prompting che invita il modello a scomporre un problema complesso in più passaggi logici prima di fornire la risposta finale.

FAISS è una libreria usata per effettuare ricerche veloci tra vettori numerici. In una pipeline RAG può essere usata per trovare i chunk semanticamente più vicini alla domanda dell'utente.

I modelli Sentence Transformers trasformano frasi e documenti in vettori numerici. Testi con significato simile tendono ad avere rappresentazioni vicine nello spazio vettoriale.
