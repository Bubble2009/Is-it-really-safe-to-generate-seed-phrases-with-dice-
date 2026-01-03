## Calcolo del checksum

Ora vedremo come calcolare il cehcksum.<br>
Per chi volesse cimentarsi in un calcolo a dir poco complicato, lascio un link in cui viene descritto come effettuare il calcolo de checksum con carta e penna: [:link: SHA 256 from scratch with pen and paper](https://armantheparman.com/sha256/).

Visto che in pochi saranno così temerari, vediamo come poter effettuare questo calcolo in maniera più pratica.<br>
Quì vedremo come effettuare questo calcolo utilizzando un comando linux.<br>
E' possibile utilizzare una qualsiasi ditribuzione GNU/LINUX o Unix (peranto anche un sistema MacOS), ma per il massimo della privacy, vi consiglio vivamente di utilizzare [:link: Tails](https://tails.net/).

#### Tails, una distribuzione con l'*Amnesia*<br>

Apro una piccola parentesi su Tails, per chi conoscesse già questo sistema, può saltare questa sezione.<br>
Tails è una distribuzione GNU/Linux basata su Debian che funziona in modalità live da chiavetta USB.<br>
A differenza di altri sistemi live, Tails ha la particolarità di ripartire tutte le volte da un sistema pulito. Non è quindi possibile effettuare alcuna modifica al sistema operativo.<br>
Questa sua peculiarità gli ha donato il nome in codice di "*amnesia*".<br>
Prossimamente pubblicherò anche qualcos su questo genial sistema operativo.

---

L'utilizzo di Tails è consigliato perchè siamo sicuri di utilizzare un sistema sicuramente pulito, senza software di terze parti potenzialmente dannoso.<br>
Ovviamente se avete una istanza di Tails che già utilizzate, non dovete abilitare la partizione permanente, lameno per questa operazione.<br>
Quindi, avviate Tails (o un'altra distribuzione GNO/Linux o Unix), disconnettete la rete (wifi, lab cablata e bluethoot), dopo di che aprite un terminale e procedete come segue:

* prendete il numero che avete generato e, nel caso sia in un formato differente, convertitelo in binario;
* verificate di avere l'intera stringa, ovvert che sia composta da:
  * seed da 12 parole:
    * 11 blocchi da 11 bit;
    * un blocco da 7 bit;
    * che concatenati formano un numero da 128 bit;
  * seed da 24 parole:
    * 23 blocchi da 11 bit;
    * un blocco da 3 bit;
    * che concatenati formano un numero da 256 bit;
* digitare nel terminale questo comando: `echo 00000000000000000000 | shasum -a 256 -0`[^1]<br>
ovviamente sostituite 00000000000000000000 con la vostra stringa da 128 o 256 bit;
* a questo punto vi apparirà una stringa esadecimale di 64 caratteri (equivalenti a 256 bit in biario), di questa stringa noi dovremo considerare:
    * seed da 12 parole:
        * il primo carattere partendo da sinsitra
    * seed da 24 parole:
        * ii primi due caratteri (quelli più a sinistra)
* a questo punto basterà convertire il risultato di questa operazione del formato da voi utilizato in precendenza, utilizzando la tabella che trovate in [questa pagina](Conversion_Table.md);
* aggiungete il numero ottenuto all'ultimo blocco generato parzialmente e troverete la vostrsa parola che fungerà da checksum per le altre.




[^1]: Spiegazione del comando linux:
