![Tor](http://upload.wikimedia.org/wikipedia/commons/0/09/Tor-logo-2011-shaded.svg)

> Tor is free software and an open network that helps you defend against traffic analysis, a form of network surveillance that threatens personal freedom and privacy, confidential business activities and relationships, and state security.

> From https://www.torproject.org/

Tor è un protocollo e la sua implementazione open source in grado di collegare gli utenti tra loro in una rete virtuale che viene poi usata per _instradare_ il traffico dei suoi utenti allo scopo di renderlo anonimo.

## Come funziona

La rete di Tor usa una topologia a maglia: ogni utente connesso consiste in un __nodo anche detto relay__. Un nodo può anche fungere da __nodo di uscita (exit node, exit relay)__, ovvero prende i pacchetti originati da altri nodi e li spedisce al reale destinatario fuori dalla rete Tor (ad esempio un sito web).

![Step 1](https://www.torproject.org/images/htw1.png)

- Alice recupera la lista dei __nodi__ della rete Tor da un __directory server__.
- Alice si collega direttamente a uno dei __nodi__ della rete Tor.

![Step 2](https://www.torproject.org/images/htw2.png)

- Il client Tor di Alice sceglie un percorso per raggiungere la destinazione dei dati.
- I collegamenti __in verde__ sono __crittografati__ mentre quelli in rosso sono __non necessariamenti protetti__

![Step 3](https://www.torproject.org/images/htw3.png)

- Il percorso può cambiare in qualsiasi momento al fine di rendere ancora più difficile il tracciamento

### Confronto con una VPN

Sul Web è facile trovare molti provider di accesso a __VPN__ pensate per oscurare il traffico che offrono _sicurezza_, _anonimato_, _possibilità_ di superare _filtri_ o _censure_ e alta velocità di navigazione. Una VPN però, per definizione, non è sicura quanto la rete __Tor__ perchè:

- una __VPN__ è un sistema centralizzato, dunque:
    - il gestore della __VPN__ può origliare sul traffico e raccogliere informazioni, mentre questo è possibile da parte degli __exit node__ di __Tor__ solo se l'utente vittima non è attento (vedasi sezione Limitazioni e Problemi di Tor)
    - una __VPN__ (in particolare con __OpenVPN__) è soggetta a diverse _vulnerabilità_ se il gestore non ha le competenze per proteggersi, mentre un singolo utente di __Tor__ non può compromettere il servizio per gli altri utenti.
- l'accesso alla __VPN__ si basa comunque su un account, mentre l'uso di __Tor__ è totalmente anonimo.
- un servizio __VPN__ per la navigazione è quasi sempre _a pagamento_, mentre __Tor__ è anonimo e gratuito.

### Perché è sicuro e anonimo

Quando un nodo decide di spedire un pacchetto fuori dalla rete:
- calcola la strada necessaria per raggiungere un nodo di uscita
- prende le __chiavi pubbliche__ di tutti i nodi sulla strada in ordine
- __crea un layer (strato) di crittografia per ogni nodo sulla strada verso l'uscita__, effettivamente incapsulando il pacchetto in numerosi strati
  - Da qui deriva il nome _"Tor"_, che originariamente significava _"The Onion Router"_ (l'instradatore a cipolla).

Quindi:

- A ogni __hop__ nella rete, ogni nodo rimuove il proprio strato di crittografia. In questo modo si è certi che il pacchetto originale possa essere letto solo dal __nodo di uscita__ e che il percorso del pacchetto __sia per forza quello stabilito in origine dal mittente__.

- A partire dal momento dell'uscita di un pacchetto dalla rete Tor, esso non è più protetto dalla sicurezza della rete ma appare come originato dal __nodo di uscita__ quindi l'identità del __nodo__ mittente è sconosciuta.

Di conseguenza qualsiasi intercettazione di un pacchetto a metà strada del percorso nella rete Tor è inutile poichè:

- il pacchetto si trova __incapsulato in almeno uno strato crittografico__
- il mittente e il destinatario scritti nel __pacchetto intercettato__ sono quelli delle __due estremità del singolo collegamento tra due nodi Tor__, non quelli dell'originale destinatario e mittente.
- __solo l'exit node__ sa chi è il vero _destinatario_ del pacchetto.
- __solo il nodo del primo hop__ sa chi è il vero _mittente_ del pacchetto.

__Attenzione__ alle intercettazioni dal _nodo di uscita_ alla _destinazione finale_ del pacchetto:

- il pacchetto si trova tra __il nodo di uscita__ e la __destinazione finale__
- il pacchetto __non è più incapsulato nella crittografia di Tor__
- se il pacchetto __non dispone di ulteriori strati di sicurezza come TLS, OpenSSL o un sistema custom__ allora:
    - chiunque può leggere il pacchetto
    - il __nodo di uscita__ può _leggere_ ed _alterare_ il pacchetto

## Servizi Nascosti

Tor offre anche la possibilità di __gestire un servizio nascosto__ accessibile __esclusivamente tramite Tor__. Gli __hidden services__ di __Tor__ sono raggiungibili tramite la rete Tor attraverso il loro __onion address (.onion)__, un indirizzo che permette ai pacchetti di essere instradati alla corretta destinazione esattamente come i normali __hostname__ (ad esempio _google.it_ o _facebook.com_). Un __hidden service__ può essere mantenuto anche da dietro un qualsiasi __NAT__, __Firewall__ o sistema di sicurezza a patto che la macchina che lo ospita sia connessa alla rete __Tor__. Lo scopo degli __hidden service__ è di offrire un servizio senza però che gli utenti possano sapere il suo indirizzo __IP__ e dunque la sua _posizione fisica di origine_, particolarmente utile per nascondere l'identità dei gestori di servizi illegali.

### WWW To Onion Gateway

Esistono dei servizi denominati __WWW to Onion gateway__ che permettono agli utenti di accedere ai servizi __.onion__ attraverso una normale navigazione __web__. Essi agiscono da __proxy web__ in modo da contattare i servizi attraverso __Tor__ per conto dell'utente. Ovviamente in questo modo i benefici di __Tor__ vengono annullati e l'utente è completamente tracciabile, in compenso però __Tor__ non è richiesto sul computer dell'utente.
