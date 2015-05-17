## Syncthing

__Syncthing__ è un __Software Libero__ pubblicato su [syncthing.net](http://syncthing.net) sotto licenza __Mozilla Public License Versione 2.0__. Sono disponibili distribuzioni per __Windows__, __OSX__, __GNU/Linux__, __BSD__, __Solaris__ e __Android__.

L'intero ecosistema di __Syncthing__ è _libero_, _aperto_ e _Open Source_.

### Come si usa

Passi da seguire su ogni dispositivo (almeno due sono necessari):

1. ottenere il software navigando sul sito [syncthing.net](http://syncthing.net) e scaricando la versione per il proprio sistema operativo
1. dopo aver avviato il software seguendo le istruzioni offerte dal sito web, aggiungere alla lista dei dispositivi un'altro dispositivo con cui sincronizzare i propri dati.
1. aggiungere una o più cartelle alla lista dei percorsi da sincronizzare e scegliere con quali dispositivi condividerle

Quando i due dispositivi __sono accesi contemporaneamente__ e __sono in grado di comunicare via rete locale o internet__, cominceranno a sincronizzare il contenuto delle cartelle.

- il comportamento del software in caso di conflitto dei file è configurabile.
- il software supporta più sistemi di __Version Control__ per i dati delle cartelle.
- è possibile scegliere un dispositivo __Master__ per ogni cartella:
    - solo il __Master__ sarà in grado di modificare il contenuto.
    - gli altri nodi accetteranno modifiche solo dal __Master__.
- alternativamente, un nodo può essere configurato in __sola lettura__ per una o più cartelle

### Dettagli tecnici

Syncthing è un software a riga di comando con interfaccia _Web_, accessibile tramite un _Web Browser_. Ogni dispositivo è identificato tramite __TLS__ e l'indirizzo __IP__ degli altri dispositivi viene trovato tramite un __Software Tracker__ anch'esso __Open Source__. E' possibile utilizzare il tracker gestito dagli sviluppatori del software oppure usarne uno gestito personalmente.

Il software è implementato usando il linguaggio di programmazione __Go__ (anche detto __Golang__).

### Block Exchange Protocol

Syncthing è un'implementazione del __Block Exchange Protocol (BEP)__, che offre una soluzione al problema della sincronizzazione decentralizzata di una o più cartelle di file tra due o più dispositivi. Questo protocollo è nato e cresciuto insieme a Syncthing.

Le [specifiche del protocollo](https://github.com/syncthing/specs/blob/master/BEPv1.md) sono incluse insieme alla documentazione di Syncthing.

__BEP__ utilizza __TCP__ per comunicare e __TLS__ per crittografia e autenticazione.

### Problemi di connessione

Spesso i dispositivi possono trovarsi dietro __NAT__ e/o __Firewall__. Syncthing include delle tecniche basilari di _NAT Trasversal_, ma per essere sicuri la cosa migliore è posizionare i dispositivi da sincronizzare temporaneamente nella stessa rete locale in modo da essere sicuri che sincronizzino, oppure utilizzare un terzo dispositivo 
