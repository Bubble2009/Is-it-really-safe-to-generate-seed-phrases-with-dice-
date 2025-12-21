# Generazione di una SeedPhrase con d4 e d8.
Ora che vi è ben chiaro quali dadi **non usare**, vediamo come generare una SeedPhrase utilizzando dadi che derivino da Solidi Platonici.

Rimane sempre valida la guida di **Turtlecute** per utilizzare 11 dadi da 6 facce (d6) e anche quella redatta da **Il Leo** che utilizza un solo d6, ma in questo documento illustro una alternativa che utilizza un d4 e tre d8.

La guida di Turtlecute (o similari), genera la SeedPhrase utilizzando il codice **binario**, questa guida, invece, utilizza il sistema **ottale**.

## Preparazione
Prima di procedere, dovete procurarvi un d4 e tre d8.<br> Vi consiglio di recuperare 3 d8 di colori differenti in modo da azzerare il fattore decisionale umano che potrebbe indebolire l'entropia.<br> E' vero che potete anche utilizzare un solo dado da 8 e lanciarlo 3 volte per ogni parola, ma questo aumenterebbe di molto il numero di lanci da effettuare.<br>
Per questa guida utilizziamo di d4 ed i d8 che sono dadi derivanti da Solidi Geometrici. Vi consiglio di effettuare i test di bilanciamento spiegati in [:link: questo documento](test_bilanciamento.md).<br>
Se riuscirete a procurarvi questi 4 dadi, vi basterà effettuare un lancio di questo set per ogni parola.<br>
Oltre ai dadi vi servirà un taccuino in cui appuntarvi i risultati e poi un computer per calcolare il checksum.
### Lettura del d4
![444](assets/444.jpg)
Questi tre dadi, indicano il valore 4, ma, come potete vedere, il dado giallo (poco leggibile in foto) ed il dado rosso hanno il quattro nella base, mentre quello verde ha il 4 nel vertice.<br>
Che io sappia, esistono solo queste due tipologie di d4, ma non escludo che possiate trovarne di differenti.

### Perché 3 dadi di colore differente?

**piccola premessa**<br>
in una stringa binaria, il numero più a sinistra viene chiamato **msb** (most significative bit o bit più significativo) e quello più a destra **lsb** (less significative bit o bit meno significativo). In questo caso, però non stiamo parlando di bit ma di caratteri (digit) così definiremo **msd** e **lsd** le nostre cifre agli  estremi.

Con i nostri lanci dovremo generare un numero ottale che andrà da 0000 fino a 3777 (equivalente ottale di 2047).<br>
Prendiamo per esempio un lancio **4335**.

![4335_2](assets/4335.jpg)

Questo numero è composto da 4 caratteri: abbiamo il 4 che è il **msd**, poi il 3, ancora il 3 e finiamo con il 5 che è l'**lsd**.<br>

![488](assets/4888.jpg)

Il primo carattere verrà generato con il dado da 4, mentre gli altri tre, con i dadi da 8. Per massimizzare l'entropia è molto utile definire a priori quale dado da 8 fornirà il valore lsd e quali dadi gli altri due valori.<br>
I colori differenti servono a identificare univocamente i 3 dadi da 8 e posizionare i valori ottenuti nella apposita posizione della stringa che fornirà il valore.<br>
Nel mio caso, il dado verde sarà l'**lsd**, poi metterò alla sua sinistra il dado giallo e per finire il dado bianco.<br>
Rispettando questo codice colore, evitiamo che una decisione umana possa ridurre l'entropia.

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
E' però necessario eseguire una semplicissima operazione matematica annotandosi i risultati.
Potete decidere se farlo subito, oppure se farlo dopo per tutti i risultati.<br>
In pratica, bisogna sottrarre uno ad ogni faccia pertanto, tornando all'esempio di prima:

![4335_2](assets/4335.jpg)

Il valore 4335 dovrà esse trascritto in bella come 3224.<bs>
Segue un esempio di come potrebbe essere fatta la tabella di lanci.
Per la 12a o la 24a parola, attendere il capitolo successivo.

| Esempio Lanci 12 parole | Esempio Lanci 24 parole |
|---------------------------|---------------------------|
|![12_word](assets/Lanci_12_word.jpg)|![12_word](assets/Lanci_24_word.jpg)|

## L'ultima parola
Siamo ora arrivati a dover individuare la parola del checksum.
Arrivati a questo punto con 11 o 23 parole, possiamo utilizzare vari tools per generare l'ultima parola ma, in questo caso avremo un intervento umano che abbasserà l'entropia visto che:
* SeedPhrase con 12 parole (di cui 11 generate casualmente)
    * abbiamo 128 possibili parole che possono fungere da checksum
* SeedPhrase con 24 parole (di cui 23 generate casualmente)
    * abbiamo 8 possibili parole che possono fungere da checksum

potete verificare tutto questo con uno dei numerosi tools presenti online, tra cui [questo](https://sutterseba.de/bip39-checksum-calculator/).
Mi raccomando, **non provate questi tools con le parole appena generate con i dadi**.

Per generare l'ultima utilizzando la medesima entropia utilizzata fino ad ora, possiamo fare queste ulteriori operazioni. Le operazioni sono differenti perché, avendo 11 parole, dobbiamo generare 7 degli 11 bit per identificare una sola tra quelle 128 parole, mentre partendo da 23 parole, dobbiamo generare solo 3 degli 11 bit per identificare quella singola parola tra 8.

### Generazione di 7 bit (SeedPhrase 12 parole)
Usando sempre i dadi usati in precedenza, dobbiamo generare un numero che vada da 111 a 288 che una volta trascritto sarà un valore compreso tra 000 e 177.<br>
Non abbiamo un dado a due facce. Potremmo utilizzare una moneta, ma, volendo continuare con i dadi, dobbiamo decidere come gestire il dado da 4 facce.
* possiamo decidere di assegnare 1 ai numeri pari;
* possiamo decidere di assegnare 1 al risultato di 1 e 2;
* possiamo decider un qualsiasi metodo, a patto che venga deciso a priori e non variato.

Una volta deciso questo metodo, lanciamo 1 d4 e 2 d8.<br>
Lanciando solo due d8, dobbiamo decidere quale dei due sarà l'**lsd** per non dover aggiungere una decisione umana che potrebbe diminuire l'entropia.<br>
Ricordiamoci che, anche in questo caso, dovremo trascrivere il valore finale sottraendo 1 ad ogni numero ottenuto.<br>
Nell'esempio di sopra, io avevo ottenuto un 4 che con il metodo da me scelto ho convertito in 2. Quando ho trascritto il numero ottale è diventato, quindi, un 1.

### Generazione di 3 bit (SeedPhrase 24 parole)
Per generare i 3 bit necessario ad una SeedPhrase da 24 parole, ci basta lanciare un unico d8.<br>
Anche in questo caso, andremo poi a sottrarre 1 quando trascriveremo il "bella" i risultati.<br>
Nel mio esempio di sopra, ho tirato il dado bianco ed è uscito un 7 che ho convertito in un 6 una volta trascritto.





****
[^1]: per validi intendo quelli che non avete scartato se avere effettuato più lanci del dovuto.