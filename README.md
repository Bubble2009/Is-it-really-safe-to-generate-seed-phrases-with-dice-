# SeedPhrase, Dadi e Security Tradeoff

### Chiunque si sia dimostrato interessato a Bitcoin, prima o poi ha dovuto affrontare la generazione di una seedphrase.

Ci sono svariati metodi per generare questa serie di 12 o 24 parole, ma ognuno ha divverenti livelli di entropia e, di conseguenza, differenti livelli di sicurezza.

Una volta generata la SeedPhrase, sarà poi necessaio conservalra in maniera sicura, ma questo è un disxorso che magari affronteremo in un altro momento.

# Generazione Seedphrase con i dadi

Non è mia intenzione dare l'ennesima guida du come generare la SeedPhrase, ma volgio solo mettervi a conoscenza di considerazioni che ho fatto nel tempo.

### Monete o Dadi 6 facce

Come sapete, per descrivere in maniera binaria il numero corrispondente alle 2048 parole intodotte con il [BIP39](https://github.com/bitcoin/bips/tree/master/bip-0039), servono 11 bit, per questo motivo vengono spesso utilizzate 11 monete oppure 11 dadi da 6 facce.

Se non conoscete questa pratica, vi consigio di leggere la guida redatta da [Turtlecute](https://github.com/Turtlecute33) e pubblicata su suo sito: [turtlecute.org/seed](https://turtlecute.org/seed/). La stessa procedura può essere utilizzata utilizzando 11 monete.

Ho appositamente menzinato le monete, perchè ritengo che possa essere più semplice recuperare 11 monete identiche piuttosto che 11 dadi.
E' anche vero che si puà utilizzare un solo dato e lanciarlo 11 volte per parola da generare, ma tutta la trafila risulterà più lunga.

A questo proposito, però, vi segnalo una procedura che ha studiato un amico, che vi permette di generare la SeedPhrase lanciando un dado da 6, un numero limitato di volte. Per il momento potete trovare la guida di **Leo** su questo gruppo Telegram: [ABC del ₿itcoin](https://t.me/+GlEaD0WD53BmNGE0).

### Altri tipi di Dadi

Molto spesso mi sono imbattuto in guide che esortano gli utenti ad utilizare altri tipi di dadi.
La maggiorparte di queste guide alternative, però, spingono gli utenti ad utilizzare i ***dadi da 16 facce***.

Da giocatore di D&D, quasi cascai dalla sedia quando sentii nominare questi dadi. Mai sentiti, mai utilizati, mai visti in nessun negiozo e nessuna fiera.

Così, pieno di curiosità e aspettative, ho acquistato (*voi non fatelo*) [questi dadi](https://amzn.to/48HkGFp) da 16 facce su Amazon. All'arrivo ho subito notato che le 16 facce non erano tutte uguali, anzi, erano presenti 3 tipi di facce ed oltreutto erano **forme gemetriche IRREGOLARI**.

Spinto dalla filosofia *"don't trust, verify"*, mi sono lanciato nella sperimentazione e nella ricerca.

I ricordi delle lezioni di Gemetria, sono oramai del tutto sbiaditi, pertanto ho dovuto dare affidamento alla rete per tornare a riscoprire **I Solidi Platonici**.

## I Solidi Platonici

**Platone**, insieme al suo maestro **Socrate** e al suo allevo **Aristotele** ha posto le basi del *pensiero filosofico occidentale*.
La rilevanza tra un filosofo e la gemetria, a noi non interessa, ma quello che è fondamentale capire è la definizione di **Solido Platonico**.

Il **solido platonico**, sinonimo di **solido regolare** e di **poliedro convesso regolare**, indica un [poliedro convesso](https://it.wikipedia.org/wiki/Poliedro_convesso) con le seguenti caratteristiche:

* le sue [facce](https://it.wikipedia.org/wiki/Faccia_(geometria)) hanno tutte la stessa superficie, essendo [poligoni regolari](https://it.wikipedia.org/wiki/Poligoni_regolari) [congruenti](https://it.wikipedia.org/wiki/Congruenza_(geometria)) (cioè sovrapponibili esattamente);
* i suoi [spigoli](https://it.wikipedia.org/wiki/Spigolo) hanno tutti la stessa lunghezza;
* i suoi [vertici](https://it.wikipedia.org/wiki/Vertice_(geometria)) sono tutti equivalenti, sicché i suoi [angoloidi](https://it.wikipedia.org/wiki/Angoloide) (angoli interni tridimensionali) hanno tutti la stessa ampiezza.

Vi sono in tutto cinque tipologie di solidi con queste caratteristiche:


| Tetraedro | Esaedro | Ottaedro | Dodecaedro | Icosaedro |
| ----------- | --------- | ---------- | ------------ | ----------- |
|  ![Tetraedro](assets/Tetrahedron.gif)  |  ![Esaedro](assets/Hexahedron.gif)  | ![Ottaedro](assets/Octahedron.gif) | ![Dodecaerdo](assets/Dodecahedron.gif) |  ![Icosaedro](assets/Icosahedron.gif)   |
| D4                                                 | D6      | D8       | D10        | D12       |
