## Calcolo del checksum

Ora vedremo come calcolare il cehcksum.<br>
Per chi volesse cimentarsi in un calcolo a dir poco complicato, lascio un link in cui viene descritto come effettuare il calcolo de checksum con carta e penna: [:link: SHA 256 from scratch with pen and paper](https://armantheparman.com/sha256/).

Visto che in pochi saranno così temerari, vediamo come poter effettuare questo calcolo in maniera più pratica.<br>
Quì vedremo come effettuare questo calcolo utilizzando un comando linux.<br>
E' possibile utilizzare una qualsiasi distribuzione GNU/LINUX o Unix (pertanto anche un sistema MacOS), ma per il massimo della privacy, vi consiglio vivamente di utilizzare [:link: Tails](https://tails.net/).

***
#### Tails, una distribuzione con l'*Amnesia*<br>
Apro una piccola parentesi su Tails, per chi conoscesse già questo sistema, può saltare questa sezione.<br>
Tails è una distribuzione GNU/Linux basata su Debian che funziona in modalità live da chiavetta USB.<br>
A differenza di altri sistemi live, Tails ha la particolarità di ripartire tutte le volte da un sistema pulito. Non è quindi possibile effettuare alcuna modifica al sistema operativo.<br>
Questa sua peculiarità gli ha donato il nome in codice di "*amnesia*".<br>
Prossimamente pubblicherò anche qualcosa su questo geniale sistema operativo.

---

L'utilizzo di Tails è consigliato perché in questo modo utilizzeremo sempre un sistema sicuramente pulito, privo di software di terze parti potenzialmente dannoso.<br>
Se avete una istanza di Tails che già utilizzate, per questa operazione non dovrete abilitare la partizione permanente.<br>
Una volta avviata Tails (o un'altra distribuzione GNU/Linux o Unix), disconnettete la rete (wifi, lab cablata e bluetooth), dopo di che aprite un terminale e procedete come segue:

* prendete il numero che avete precedentemente generato e, nel caso sia in un formato differente, convertitelo in binario;
* verificate di avere l'intera stringa, ovvero che sia composta da:
  * seed da 12 parole:
    * 11 blocchi da 11 bit;
    * 1 blocco da 7 bit;
      * che concatenati formano un numero da 128 bit;
  * seed da 24 parole:
    * 23 blocchi da 11 bit;
    * 1 blocco da 3 bit;
      * che concatenati formano un numero da 256 bit;
* digitare nel terminale questo comando: `echo xXxXxXxXxXx | shasum -a 256 -0`[^1]<br>
ovviamente sostituite `xXxXxXxXxXx` con la vostra stringa da 128 o 256 bit;
* a questo punto vi apparirà una stringa esadecimale di 64 caratteri (equivalenti a 256 bit in binario); di questa stringa noi dovremo considerare:
    * seed da 12 parole:
        * il primo carattere partendo da sinistra
    * seed da 24 parole:
        * ii primi due caratteri (quelli più a sinistra)
* a questo punto basterà convertire il risultato di questa operazione del formato da voi utilizzato in precedenza, utilizzando la tabella che trovate in [questa pagina](Conversion_Table.md);
* aggiungete il numero ottenuto all'ultimo blocco generato parzialmente e troverete la vostra parola che fungerà da checksum per le altre.




[^1]: Spiegazione del comando linux:
