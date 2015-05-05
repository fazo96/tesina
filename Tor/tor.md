# Tor

![Tor Logo](http://upload.wikimedia.org/wikipedia/commons/0/09/Tor-logo-2011-shaded.svg)

> Tor is free software and an open network that helps you defend against traffic analysis, a form of network surveillance that threatens personal freedom and privacy, confidential business activities and relationships, and state security.

> From https://www.torproject.org/

Tor è un protocollo e la sua implementazione open source in grado di collegare gli utenti tra loro in una rete virtuale allo scopo di rendere anonimo il loro traffico.

## Come funziona

La rete di Tor usa una topologia a maglia: ogni utente connesso consiste in un __nodo anche detto relay__. Un nodo può anche fungere da __nodo di uscita (exit node, exit relay)__, ovvero prende i pacchetti originati da altri nodi e li spedisce al reale destinatario fuori dalla rete Tor (ad esempio un sito web).

- Alice recupera la lista dei __nodi__ della rete Tor da un __directory server__.
- Alice si collega direttamente a uno dei __nodi__ della rete Tor.

![Step 1](https://www.torproject.org/images/htw1.png)

- Il client Tor di Alice sceglie un percorso per raggiungere la destinazione dei dati.
- I collegamenti __in verde__ sono __crittografati__ mentre quelli in rosso sono __non necessariamenti protetti__

![Step 2](https://www.torproject.org/images/htw2.png)

- Il percorso può cambiare per destinazioni diverse, al fine di rendere ancora più difficile il tracciamento

![Step 3](https://www.torproject.org/images/htw3.png)

### Perché è sicuro e anonimo

Quando un nodo decide di spedire un pacchetto fuori dalla rete:
- calcola la strada necessaria per raggiungere un nodo di uscita
- prende le __chiavi pubbliche__ di tutti i nodi sulla strada in ordine
- __crea un layer (strato) di crittografia per ogni nodo sulla strada verso l'uscita__, effettivamente incapsulando il pacchetto in numerosi strati
  - Da qui deriva il nome "Tor", che originariamente significava "The Onion Router" (l'instradatore a cipolla).

Inoltre:

- A ogni __hop__ nella rete, ogni nodo rimuove il proprio strato di crittografia. In questo modo si è certi che il pacchetto originale possa essere letto solo dal __nodo di uscita__ e che il percorso del pacchetto __sia per forza quello stabilito in origine dal mittente__.

- A partire dal momento dell'uscita di un pacchetto dalla rete Tor, esso non è più protetto dalla sicurezza della rete ma appare come originato dal __nodo di uscita__ quindi l'identità del __nodo__ mittente è sconosciuta.

Di conseguenza qualsiasi intercettazione di un pacchetto a metà strada è inutile poichè:

- il pacchetto originale si trovava __incapsulato in strati crittografici__
- il sorgente e il destinatario scritti nel __pacchetto intercettato__ sono quelli delle __due estremità del singolo collegamento tra due nodi__, non quelli dell'originale destinatario e sorgente.
- __solo l'exit node__ sa chi è il vero destinatario del pacchetto.
- __solo il nodo del primo hop__ sa chi è il vero sorgente del pacchetto.

## Servizi Nascosti
