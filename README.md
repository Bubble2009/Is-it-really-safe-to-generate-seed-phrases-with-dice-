# SeedPhrase, Dadi e Security Tradeoff

### Chiunque si sia dimostrato interessato a Bitcoin, prima o poi ha dovuto affrontare la generazione di una SeedPhrase.

Ci sono svariati metodi per generare questa serie di 12 o 24 parole, ma ognuno ha differenti livelli di entropia e, di conseguenza, differenti livelli di sicurezza.

Una volta generata la SeedPhrase, sarà poi necessario conservarla in maniera sicura, ma questo è un discorso che magari affronteremo in un altro momento.

# Generazione SeedPhrase con i dadi

Non è mia intenzione dare l'ennesima guida di come generare la SeedPhrase, ma voglio solo mettervi a conoscenza di considerazioni che ho fatto nel tempo.

### Monete o Dadi 6 facce

Come sapete, per descrivere in maniera binaria il numero corrispondente alle 2048 parole introdotte con il [BIP39](https://github.com/bitcoin/bips/tree/master/bip-0039), servono 11 bit, per questo motivo vengono spesso utilizzate 11 monete oppure 11 dadi da 6 facce.

Se non conoscete questa pratica, vi consiglio di leggere la guida redatta da [Turtlecute](https://github.com/Turtlecute33) e pubblicata su suo sito: [turtlecute.org/seed](https://turtlecute.org/seed/). La stessa procedura può essere utilizzata utilizzando 11 monete.

Ho appositamente menzionato le monete, perché ritengo che possa essere più semplice recuperare 11 monete identiche piuttosto che 11 dadi.
E' anche vero che si può utilizzare un solo dato e lanciarlo 11 volte per parola da generare, ma tutta la trafila risulterà più lunga.

A questo proposito, però, vi segnalo una procedura che ha studiato un amico, che vi permette di generare la SeedPhrase lanciando un dado da 6, un numero limitato di volte. Per il momento potete trovare la guida di **Leo** su questo gruppo Telegram: [ABC del ₿itcoin](https://t.me/+GlEaD0WD53BmNGE0).

### Altri tipi di Dadi

Molto spesso mi sono imbattuto in guide che esortano gli utenti ad utilizzare altri tipi di dadi.
La maggior parte di queste guide alternative, però, spingono gli utenti ad utilizzare i ***dadi da 16 facce***.

Da giocatore di **D&D** (il più famoso [GdR](https://it.wikipedia.org/wiki/Gioco_di_ruolo)), quasi cascai dalla sedia quando sentii nominare questi dadi.

* Mai sentiti;
* Mai utilizzati;
* Mai visti in nessun negozio e nessuna fiera.

Così, pieno di curiosità e aspettative, ho acquistato (*voi non fatelo*) [questi dadi](https://amzn.to/48HkGFp) da 16 facce su Amazon. All'arrivo ho subito notato che le 16 facce non erano tutte uguali, anzi, erano presenti 3 tipi di facce ed oltretutto erano **forme geometriche IRREGOLARI**.

Spinto dalla filosofia *"don't trust, verify"*, mi sono lanciato nella sperimentazione e nella ricerca.

I ricordi delle lezioni di Geometria, sono oramai del tutto sbiaditi, pertanto ho dovuto dare affidamento alla rete per tornare a riscoprire **I Solidi Platonici**.

## I Solidi Platonici

**Platone**, insieme al suo maestro **Socrate** e al suo allevo **Aristotele** ha posto le basi del *pensiero filosofico occidentale*.

La rilevanza tra un filosofo e la geometria, a noi non interessa, quello che invece è fondamentale è capire le caratteristiche di un **Solido Platonico** e perché la sua regolarità è molto importante.

Il **solido platonico**, sinonimo di **solido regolare** e di **poliedro convesso regolare**, indica un [poliedro convesso](https://it.wikipedia.org/wiki/Poliedro_convesso) con le seguenti caratteristiche:

* le sue [facce](https://it.wikipedia.org/wiki/Faccia_(geometria)) hanno tutte la stessa superficie, essendo [poligoni regolari](https://it.wikipedia.org/wiki/Poligoni_regolari) [congruenti](https://it.wikipedia.org/wiki/Congruenza_(geometria)) (cioè sovrapponibili esattamente);
* i suoi [spigoli](https://it.wikipedia.org/wiki/Spigolo) hanno tutti la stessa lunghezza;
* i suoi [vertici](https://it.wikipedia.org/wiki/Vertice_(geometria)) sono tutti equivalenti, sicché i suoi [angoloidi](https://it.wikipedia.org/wiki/Angoloide) (angoli interni tridimensionali) hanno tutti la stessa ampiezza.

Esistono **soltanto cinque solidi** con queste caratteristiche e sono:

| Tetraedro                            | Esaedro                           | Ottaedro                           | Dodecaedro                             | Icosaedro                            |
| -------------------------------------- | ----------------------------------- | ------------------------------------ | ---------------------------------------- | -------------------------------------- |
| ![Tetraedro](assets/Tetrahedron.gif) | ![Esaedro](assets/Hexahedron.gif) | ![Ottaedro](assets/Octahedron.gif) | ![Dodecaerdo](assets/Dodecahedron.gif) | ![Icosaedro](assets/Icosahedron.gif) |

Le caratteristiche di un Solido Platonico, garantiscono una perfetta simmetria tra le varie facce, garantendo che nessuna faccia abbia una probabilità *fisica* si avere un vantaggio/svantaggio rispetto alle altre in caso di rotolamento.

Per questo motivo, da questi solidi, derivano i dadi che utilizziamo comunemente.
Quello a 6 facce è quello universalmente più diffuso; gli altri, invece, sono mno diffusi, ma molto utilizzati nei [GdR](https://it.wikipedia.org/wiki/Gioco_di_ruolo) (giochi di ruolo).

| D4                        | D6                        | D8                        | D12                         | D20                         |
| --------------------------- | --------------------------- | --------------------------- | ----------------------------- | ----------------------------- |
| ![D4](assets/Dice_D4.jpg) | ![D6](assets/Dice_D6.jpg) | ![D8](assets/Dice_D8.jpg) | ![D12](assets/Dice_D12.jpg) | ![D20](assets/Dice_D20.jpg) |

| Dado 10 facce | D10                         |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- | 
| Da notare che nei GdR si utilizza anche un dado da 10 facce, ma sebbene le sue [facce](https://it.wikipedia.org/wiki/Faccia_(geometria)) siano sovrapponibili, essendo [poligoni regolari](https://it.wikipedia.org/wiki/Poligoni_regolari) [congruenti](https://it.wikipedia.org/wiki/Congruenza_(geometria)), gli spigoli non hanno tutti la stessa lunghezza e di conseguenza i vertici non sono equivalenti. Avendo uno solo dei tre requisiti, il D10 non può essere considerato un Solido Platonico. Nonostante questo, le facce omogenee garantiscono una discreta euristica, sicché i giocatori di ruolo, possono stare tranquilli.| ![D10](assets/Dice_D10.jpg) | 

## il Dado a 16 facce
Questa brevissima analisi dei Solidi Platonici ci serve per comprendere che il D16 non è un solido platonico, ma non come il D10, il D16 non rispecchia NESSUNA delle caratteristiche che identificano un Solido Platonico.
Quanto descritto fino ad ora, si rispecchia perfettamente nei test che ho effettuato. Sebbene per il momento il quantitativo di lanci su cui ho basato la mia analisi sia esiguo, già si vedono le prime devianze nei risultati.

