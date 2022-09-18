# Shell Playground
Avviando questo tutorial imparerai:
- a muovere i primi passi all'interno di `Cloud Shell Editor`:
    - aprire/chiudere il terminale (also known as: shell oppure linea di comando)
    - aprire/chiudere l'editor
- eseguire i tuoi primi comandi nella `shell`:
    - stampare un testo
    - mostrare il percorso (path) in cui ti trovi
    - creare una nuova cartella
    - spostarti dentro la nuova cartella creata
    - creare un nuovo file al suo interno
    - installare `nano` tramite `apt-get`
    - modificare il contenuto di un file
    - rendere il file eseguibile
    - eseguire un eseguibile

## 

## Aprire/Chiudere il terminale (aka shell)
Potete aprire e chiudere l'interfaccia del terminale cliccando sul pulsante con questa icona:
<walkthrough-cloud-shell-icon></walkthrough-cloud-shell-icon>

All'interno del terminale potrete interagire solamente attraverso la tastiera: scrivendo o incollando comandi testuali e premendo invio per lanciarne l'esecuzione.

## Aprire/chiudere l'editor
Potete aprire e chiudere l'interfaccia dell'editor cliccando sul pulsante con questa icona: <walkthrough-cloud-shell-editor-icon></walkthrough-cloud-shell-editor-icon>

L'editor ci sarà utile soprattuto per **controllare** la struttura di cartelle e file nel nostro host.

In realtà l'editor, interagendo con il 
<walkthrough-editor-spotlight spotlightId="file-explorer">riquadro sulla sinistra</walkthrough-editor-spotlight>, ci dà la possibilità di creare/cancellare/modificare cartelle e files attraverso una interfaccia grafica molto più pratica del terminale.

Tuttavia noi cercheremo di imparare a fare tutte queste operazioni direttamente dalla shell. 

### Perché imparare a fare queste operazioni da shell?
A volte capita di dover utilizzare la shell per interagire con degli host non avendo a disposizione alcuna interfaccia grafica, per questo è importante imparare a muoversi anche soltanto tramite la shell.

### Prima di andare avanti:
Chiudiamo l'editor (<walkthrough-cloud-shell-editor-icon></walkthrough-cloud-shell-editor-icon>) e lasciando aperto il terminale (<walkthrough-cloud-shell-icon></walkthrough-cloud-shell-icon>), in modo tale da avere il massimo dello spazio dello schermo a disposizione.


## Stampare un testo
Copiare il seguente comando nella shell:
```sh
echo "Hello World"
```
e premere invio

Nota che subito dopo aver premuto invio è stato stampato il testo che abbiamo indicato dopo il comando `echo`.

### I box grigi dei comandi
D'ora in poi quando troverai un box grigio simile a quello precedente implicitamente intenderemo di copiarne il testo nella shell e premere invio (come abbiamo appena fatto per il comando `echo "Hello World"`).

Nella sezione in alto a destra di ogni box grigio ci sono due piccoli bottoni:
- il primo ti permette di copiare il testo in automatico direttamente nella shell 
- il secondo ti permette di copiare il testo nella clipboard di sistema (per poi poterlo incollare dove preferisci).

Prova entrambi i bottoni prima di andare avanti.


## Mostrare il percorso (path) in cui ti trovi
Quando lavoriamo con la shell è necessario avere delle coordinate circa la posizione in cui ci troviamo all'interno delle directory di sistema.

Il comando `pwd` (`Current Working Directory`) restituisce il path (percorso assoluto rispetto alla root di sistema) alla cartella nella quale siamo posizionati in questo momento.

Proviamo ad eseguirlo:
```sh
pwd
```



## Creare una nuova cartella

Il comando `mkdir` (`Make Directory`) permette di creare una nuova cartella se questa non esiste già:
```sh
mkdir data
```
Il comando precedente crea una cartella di nome `data` all'interno del percorso dove ci troviamo in questo momento (vedi `pwd`).


## Verifichiamo la creazione della cartella
### Usando il comando ls:
Per verificarne a creazione, eseguiamo il comando `ls`(`List Files`) la cui esecuzione visualizza la lista dei files presenti nella cartella corrente (vedi `pwd`):
```sh
ls
```
Se nella lista dei files è elencata anche la cartella `data` allora il comando è andato a buon fine (ammesso che la cartella non esistesse già). Cartelle e files sono mostrati nella lista con colori diversi.


### Usando il Cloud Shell Editor:
Un altro modo più semplice che possiamo adottare su `Cloud Shell` è aprire l'editor <walkthrough-cloud-shell-editor-icon></walkthrough-cloud-shell-editor-icon> e posizionarci, nel <walkthrough-editor-spotlight spotlightId="file-explorer">riquadro sulla sinistra</walkthrough-editor-spotlight> sulla cartella corrente (vedi `pwd`). Se dentro la cartella corrente è presente una cartella `data` il comando è sicuramente andato a buon fine (ammesso che la cartella non esistesse già).


## Spostarti dentro la nuova cartella creata
Per spostare la `working directory` è necessario utilizzare il comando `cd` (`Change Directory`):
```sh
cd data
```

adesso prova ad eseguire il seguente comando:
```sh
pwd
```


## Creare un nuovo file al suo interno

Eseguire il seguente comando:
```sh
> myfile.txt
ls
echo 'echo "Hello World"' > myfile.txt
chmod +x myfile.txt
sh ./myfile.txt
# sudo apt-get install nano
```

[comment]: # (<walkthrough-editor-open-file filePath="data/myfile.txt">data/myfile.txt</walkthrough-editor-open-file>)



## Congratulations

<walkthrough-conclusion-trophy></walkthrough-conclusion-trophy>

Hai finito il tuo primo tutorial, congratulazioni!