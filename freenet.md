# Freenet

__"The Free Network"__ è un __software libero__ disponibile sul sito [freenetproject.org](https://freenetproject.org/) che consente di collegarsi agli altri utilizzatori del software e di navigare su un __piccolo web__ gestito interamente usando il software __Freenet__, composto da siti detti __"freesites"__.

Freenet si basa sul concetto di __archivio decentralizzato__, ovvero le informazioni dei siti stessi sono __distribuite sulla rete__ in modo da non avere il problema della __centralizzazione__.

Dunque __Freenet__ offre:

- __Forums__ su cui discutere con gli altri utenti,
- __Chat__ per parlare direttametne con gli altri utenti,
- __Freesites__ ovvero classici siti web esclusivi di Freenet, distribuiti sulla rete e quindi la cui origine non è tracciabile.

Chiunque può __pubblicare il proprio Freesite__ semplicemente usando il software __Freenet__.

Freenet esiste dal __marzo 2000__ ed è tutt'ora in sviluppo.

### Interfaccia grafica

![Freenet Screenshot](http://cdn.canadiancontent.net/t/screenshot/750/freenet.jpg)
- _Immagine:_ __Freenet__ in esecuzione su __Debian Linux__ usando il web browser __Iceweasel__ (il _fork_ di __Firefox__ sviluppato dal team di __Debian__)

Per interfacciarsi a __Freenet__ è necessario un Browser Web. Questo perchè il __client di Freenet__ si limita a recuperare i file __HTML, CSS__ dei __Freesites__ offrendoli tramite un'interfaccia __HTTP__ e accettando, tramite la stessa, richieste __HTTP__ per interagire con i __Freesites__. Il browser web si occupa di _visualizzare questi file_ rendendo possibile la navigazione per gli utenti umani.

## Come funziona

__Freenet__ usa un modello di comunicazione __molto simile a quello di Tor__ (dettagliato nel capitolo dedicato a Tor), crittografando tutte le comunicazioni. Inoltre grazie alla sua __decentralizzazione__, combatte efficacemente la censura, e non permette di __origliare__ sulle comunicazioni.

Come detto in precedenza, i dati sono organizzati in un __database distribuito__ che non ha centralizzazione ma si trova su tutti i computer degli utenti di __Freenet__, permettendo di accedere ai dati pubblicati in origine da un utente anche se esso non è più collegato da tempo alla rete __Freenet__. I dati sono mantenuti finchè rimangono abbastanza popolari, poi vengono scartati gradualmente per lasciare posto a dati più importanti e popolari.

A partire dalla versione __0.7__, __Freenet__ può essere configurato per __nascondere attivamente__ il suo utilizzo, promuovendo __l'anonimato__ e la lotta contro la __censura__.
