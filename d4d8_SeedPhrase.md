# Generazione di una SeedPhrase con d4 e d8.
Ora che vi è ben chiaro quali dadi **non usare**, vediamo come generare una SeedPhrase utilizzando dadi che derivino da Solidi Platonici.

Rimane sempre valida la guida di **Turtlecute** per utilizzare 11 dadi da 6 facce (d6) e anche quella redatta da **Il Leo** che utilizza un solo d6, ma in questo documento illustro una alternativa che utilizza un d4 e tre d8.

La guida di Turtlecute (o similari), genera la SeedPhrase utilizzando il codice **binario**, questa guida, invece, utilizza il sistema **ottale**.

## Preparazione
Prima di procedere, dovete procurarvi un d4 e tre d8.<br> Vi consiglio di recuperare 3 d8 di colori differenti in modo da azzerare il fattore decisionale umano che potrebbe indebolire l'entropia.<br> E' vero che potete anche utilizzare un solo dado da 8 e lanciarlo 3 volte per ogni parola, ma questo aumenterebbe di molto il numero di lanci da effettuare.<br>
Per questa guida utilizziamo di d4 ed i d8 che sono dadi derivanti da Solidi Geometrici. Vi consiglio di effettuare i test di bilanciamento spiegati in [:link: questo documento](test_bilanciamento.md).<br>
Se riuscirete a procurarvi questi 4 dadi, vi basterà effettuare un lancio di questo set per ogni parola.<br>
Oltre ai dadi vi servirà un taccuino in cui appuntarvi i risultati e poi un computer per calcolare il checksum.

**Perché 3 dadi di colore differente?**<br>
Con i nostri lanci dovremo generare un numero ottale che andrà da 0000 fino a 3777 (equivalente ottale di 2047).<br>
Prendiamo per esempio un lancio **2546**.<br>
Questo numero è composto da 4 caratteri: abbiamo il 2 che è il **msb** (most significative byte o byte più significativo), poi il 5, il 4 e finiamo con il 6 che è l'**lsb** (less significative byte o byte meno significativo).<br>
Il primo carattere verrà generato con il dado da 4, mentre gli altri tre, con i dadi da 8. Per massimizzare l'entropia è molto utile definire a priori quale dado da 8 fornirà il valore lsb e quali dadi gli altri due valori.<br>
I colori differenti servono a identificare univocamente i 3 dadi da 8 e posizionare i valori ottenuti nella apposita posizione della stringa che fornirà il valore.

## Esecuzione dei lanci aumentando l'entropia
Quelle che seguono, sono personali considerazioni su come aumentare l'entropia generata dal lancio dei dadi.<br>
Se si ripetesse esattamente lo stesso lancio, clonando alla perfezione tutti i movimenti e le condizioni del primo lancio, con molta probabilità i risultati sarebbero i medesimi. Effettuando lanci a mano, questo è pressoché impossibile, però, i consigli che seguono, potrebbero aumentare l'entropia, pertanto consiglio di seguirli.
* Cambiate tipologia di lancio ogni volta che tirate i dadi.<br> Quelli che seguono sono le tipologie di lanci che effettuo io, se ne individuate di differenti, fatemelo sapere che li aggiungerò.
    * lancio da seduto con dadi in mano fatti cadere sul tavolo;
    * lancio da in piedi con i dadi in mano fatti cadere sul tavolo;
    * dadi inseriti in un bicchiere capiente, magari con anche qualche dado in più che non userete nel risultato fatti cadere sul tavolo;
    * le precedenti tipologie di lanci, ma facendo cadere i dadi per terra;
* Non abbiate fretta di terminare tutti i lanci: prendetevi delle pause dopo qualche lancio;
* Decidendo a priori una metrica per validare i lanci buoni, effettuate molti più lanci del dovuto (ad esempio il doppio prendendo il primo e scartando il secondo).

Decidete come effettuare i lanci ed eseguite l'operazione fino ad avere:
* 11 lanci validi[^1] per creare una SeedPhrase da 12 parole
* 23 lanci validi[^1] per creare una SeedPhrase da 24 parole



****
[^1]: per validi intendo quelli che non avete scartato se avere effettuato più lanci del dovuto.