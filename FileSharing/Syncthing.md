![Syncthing](https://syncthing.net/images/logo-horizontal.svg)
![SyncthingPDF](http://i.imgur.com/2xQnykS.png)

__Syncthing__ è un __Software Libero__ pubblicato su [syncthing.net](http://syncthing.net) sotto licenza __Mozilla Public License Versione 2.0__. Sono disponibili distribuzioni per __Windows__, __OSX__, __GNU/Linux__, __BSD__, __Solaris__ e __Android__.

![Screenshot](http://2.bp.blogspot.com/-l9nooLvGiq0/U49JiCnoTKI/AAAAAAAATEI/qZGrWb1SGKQ/s1600/syncthing.png)
- _Immagine:_ __GUI__ di __Syncthing__ in funzione su __Ubuntu Linux__

L'intero ecosistema di __Syncthing__ è _libero_, _aperto_ e _Open Source_: il software nasce come applicativo a riga di comando con un'aggiunta interfaccia _Web_, accessibile tramite un _Web Browser_. Ogni dispositivo è identificato tramite coppia di chiavi crittografiche (usando __TLS__) e l'indirizzo __IP__ degli altri dispositivi viene comunicato tramite un __Tracker__ anch'esso __Open Source__. E' possibile utilizzare il Tracker gestito dagli sviluppatori del software, usarne uno gestito personalmente o connettersi direttamente a indirizzi conosciuti senza usare un tracker.

Il software è implementato usando il linguaggio di programmazione __Go__ (anche detto __Golang__).

### Come si usa

Passi da seguire su ogni dispositivo (almeno due dispositivi sono necessari):

1. ottenere il software navigando sul sito [syncthing.net](http://syncthing.net) e scaricando la versione per il proprio sistema operativo
1. dopo aver avviato il software seguendo le istruzioni offerte dal sito web, aggiungere alla lista dei dispositivi un'altro dispositivo con cui sincronizzare i propri dati.
1. aggiungere una o più cartelle alla lista dei percorsi da sincronizzare e scegliere con quali dispositivi condividerle

Quando almeno due dispositivi __sono accesi contemporaneamente__ e __sono in grado di comunicare via rete locale o Internet__, cominceranno a sincronizzare il contenuto delle cartelle.

- il comportamento del software in caso di conflitto dei file è configurabile;
- il software supporta più sistemi di __Version Control__ per i dati delle cartelle;
- è possibile scegliere un dispositivo __Master__ per ogni cartella:
    - solo il __Master__ sarà in grado di modificare il contenuto;
    - gli altri nodi accetteranno modifiche solo dal __Master__.
- alternativamente, un nodo può essere configurato in __sola lettura__ per una o più cartelle.

### Block Exchange Protocol

Syncthing è un'implementazione del __Block Exchange Protocol (BEP)__, che offre una soluzione al problema della sincronizzazione decentralizzata di una o più cartelle di file tra due o più dispositivi. Questo protocollo è nato e cresciuto insieme a Syncthing.

Le [specifiche del protocollo](https://github.com/syncthing/specs/blob/master/BEPv1.md) sono incluse insieme alla documentazione di Syncthing.

__BEP__ utilizza __TCP__ per comunicare e __TLS__ per crittografia e autenticazione.

### Problemi di connessione

Spesso i dispositivi possono trovarsi dietro __NAT__ e/o __Firewall__.

Syncthing include delle tecniche basilari di _NAT Traversal_, ma per comunicare stabilmente uno dei due interlocutori deve poter ricevere __connessioni in ingresso__.

Dunque, _per avere la totale certezza che due dispositivi comunichino_, è necessario posizionarli temporaneamente nella stessa rete locale, oppure utilizzare un __terzo dispositivo__ in grado di ricevere __connessioni in ingresso__ che può fungere da tramite e soprattutto permette la sincronizzazione anche se i due dispositivi da sincronizzare non sono mai accesi contemporaneamente o mai connessi direttamente tra loro.
