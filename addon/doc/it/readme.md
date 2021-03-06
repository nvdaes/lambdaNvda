﻿# Add-On di NVDA per LAMBDA
Questo add-on permette di utilizzare il software LAMBDA con NVDA. Deriva da un lavoro precedente di Peter Lecky della  Comenius University ed è stato studiato e realizzato per rendere l'accesso all'ambiente LAMBDA il più semplice e simile a ciò che già avviene con altri screen reader.

Per maggiori informazioni sul software LAMBDA si invita a consultare:
[http://www.lambdaproject.org/it/](http://www.lambdaproject.org/it/)
e [http://veia.it/](http://veia.it/)

Si precisa che lo sviluppo di questo add-on è avvenuto in maniera volontaria e del tutto indipendente dall'azienda rivenditore del prodotto LAMBDA, con la quale l'autore non intrattiene alcun rapporto di lavoro e/o di collaborazione. 
Per richieste in merito al prodotto si invita pertanto a contattare il servizio di supporto tecnico messo a disposizione dal fornitore del prodotto.

Per ulteriori informazioni sull'addon, richieste o altro è possibile contattare l'autore tramite email o su GitHub.

L'attuale versione del componente aggiuntivo dispone di tabelle braille adattate per l'uso con Lambda sia per l'Italiano che per lo Spagnolo. I messaggi e l'interfaccia sono disponibili nella maggior parte delle lingue ufficiali di NVDA, poiché la traduzione dell'addon è mantenuta dal gruppo di traduzione internazionale. 

## Audio presentazione
Se volete scoprire nel dettaglio alcune delle caratteristiche di questo addon potete ascoltare la audio presentazione disponibile a 
[questo indirizzo](https://drive.google.com/file/d/0B52OCBeOqw26ZU5aZnptTWFNTVk/view?usp=sharing)

## Caratteristiche principali:
Per quello che riguarda l'accesso in sintesi vocale:
* Vocalizza correttamente le finestre di dialogo ed i menù;
* Vocalizza le formule matematiche utilizzando il sistema di processamento di testi di LAMBDA, quindi legge correttamente ed in modo naturale il testo matematico (ad esempio "radice 3 di 3x più 24, fine radice");
* Permette di leggere per carattere, riga, o con il leggi-tutto;
* Vocalizza correttamente la selezione dei blocchi;
* Vocalizza correttamente gli spostamenti all'interno del testo utilizzando i principali tasti standard di Windows e quelli specifici di LAMBDA;
* Vocalizza sia in maniera compatta che estesa;
* Vocalizza le finestre di esplorazione struttura, la calcolatrice e la finestra di esplorazione delle matrici;
* Il riscontro in scrittura avviene usando il sistema di processamento testi di LAMBDA.

Per quello che riguarda il braille:
* Installa una tabella braille personalizzata costruita a partire da quella a standard di LAMBDA per JAWS (la simbologia quindi è identica a quella usata per JAWS);
* Crea e configura un profilo applicativo apposito (in questo modo la tabella braille speciale per LAMBDA sarà attivata solo su questo software e non su altri);
* Permette la navigazione nei menù e nelle finestre di dialogo in braille;
* Espone in braille il testo matematico e permette di raggiungere le porzioni dello schermo grazie ai tasti di cursor routing (CR) presenti;
* A partire dalla versione 1.1.0 presenta una doppia modalità per il braille: "Flat Mode" e non "Flat Mode". Quando "Flat Mode" è attivata, NVDA userà l'intercettatore grafico per determinare cosa è presente a schermo. Questo è utile per poter spaziare con il braille anche in aree "bianche", dove non è presente testo. Con la modalità "Flat Mode" disattivata, si avrà maggior potenza nell'elaborazione del testo, in quanto NVDA utilizzerà le funzioni messe a disposizione dal sistema operativo Windows per determinare la presenza di testo. Di contro però, non sarà possibile esplorare in braille aree bianche, prive di alcun testo. Di default la modalità "Flat Mode" è attiva. Per attivarla o disattivarla usare il comando NVDA+SHIFT+F. Si consiglia caldamente di disattivare la "Flat Mode" qualora si sia cambiato il valore dei DPI dello schermo (da 100% ad un ingrandimento maggiore).
* Rende più sintetiche le finestre di dialogo delle matrici e della esplorazione struttura in modo che non confondano l'utente che le deve leggere;
* Marca in braille in modo corretto quando il testo viene selezionato.

## Consigli post l'installazione
L'addon provvede alla creazione automatica di un nuovo profilo di NVDA chiamato "lambda" associato all'applicazione "lambda.exe". Questa operazione viene effettuata automaticamente all'avvio dell'applicativo Lambda. In particolare vengono correttamente impostate le preferenze relative alla tabella braille, al tracciamento del cursore ed alla modalità flat del braille.

Se è già presente un profilo chiamato "lambda", l'addon non lo sovrascriverà e si dovrà provvedere manualmente alla configurazione.

Per rendere il compito più facile, se si desidera preservare alcune delle impostazioni del precedente profilo, è possibile utilizzare la funzionalità di "Ripristino guidato impostazioni di LAMBDA". Il comando rapido per questo comando è NVDA+alt+r.

Una soluzione più semplice è quella di cancellare il precedente profilo chiamato "lambda" accedendo al menù di NVDA, quindi andando in "Gestione profili".

La rimozione del profilo può essere utile anche nel caso di problemi legati alla configurazione di NVDA con LAMBDA.
Se si nota, dopo un certo periodo, che NVDA non funziona più correttamente con LAMBDA, provare a rimuovere il profilo "lambda" dalla lista dei profili. In questo modo l'addon si preoccuperà di creare un nuovo profilo con i parametri configurati nel modo corretto e l'utente non dovrà preoccuparsi di modificare manualmente i file di configurazione.

Ad ogni avvio dell'applicazione Lambda, questo componente aggiuntivo controlla se un profilo chiamato "lambda" esiste. Se non esiste, procede alla sua creazione automatica secondo questo formato:

```
nome file : userData\profiles\lambda.ini :

[braille]
	readByParagraph = False
	tetherTo = focus
	translationTable = percorso-della-cartella-brailleTable-del-componente-aggiuntivo\nomeTabella

[lambda]
	brailleFlatMode = True

```

Dove :
* percorso-della-cartella-brailleTable-del-componente-aggiuntivo : è il percorso assoluto della directory dell'addon a cui segue "\brailleTables"
* nomeTabella : dipende dalla lingua di NVDA.

## Comandi da tastiera del componente aggiuntivo:

* **NVDA+Shift+f**: Abilita o disabilita la modalità braille flat;
* **NVDA+alt+r**: Apre la finestra di dialogo "Ripristino guidato impostazioni di LAMBDA".


