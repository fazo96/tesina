# Tor

![Tor Logo](http://upload.wikimedia.org/wikipedia/commons/0/09/Tor-logo-2011-shaded.svg)

> Tor is free software and an open network that helps you defend against traffic analysis, a form of network surveillance that threatens personal freedom and privacy, confidential business activities and relationships, and state security.

> From https://www.torproject.org/

Tor è un software in grado di collegare gli utenti tra di loro in una rete virtuale allo scopo di rendere anonimi gli utenti che navigano il web attraverso di esso.

La rete di Tor è a maglia, e ogni utente connesso consiste in un __nodo anche detto relay__. Un nodo può anche fungere da __nodo di uscita (exit node, exit relay)__, ovvero prende i pacchetti originati da altri nodi e li spedisce al reale destinatario fuori dalla rete Tor (ad esempio un sito web).

A partire dal momento dell'uscita di un pacchetto dalla rete Tor, esso non è più protetto dalla sicurezza della rete ma appare come originato dal __nodo di uscita__ quindi l'identità del __nodo__ mittente è sconosciuta.

Qualsiasi operazione di __backtracking__ ovvero di analisi del percorso del pacchetto è inutile poichè il pacchetto si trovava __incapsulato in pacchetti Tor__ e __ogni nodo conosce solo l'indirizzo IP dei nodi a cui è direttamente collegato e del nodo di uscita__.

## La crittografia di Tor

Quando un nodo decide di spedire un pacchetto fuori dalla rete, calcola la strada necessaria per raggiungere un nodo di uscita, poi prende le __chiavi pubbliche__ di tutti i nodi sulla strada in ordine e __crea un layer (strato) di crittografia per ogni nodo sulla strada verso l'uscita__, effettivamente incapsulando il pacchetto in numerosi strati. Da qui deriva il nome "Tor", che originariamente significava "The Onion Router" (l'instradatore a cipolla).

A ogni __hop__ nella rete, ogni nodo rimuove il proprio strato di crittografia. In questo modo si è certi che il pacchetto originale possa essere letto solo dal __nodo di uscita__ e che il percorso del pacchetto __sia per forza quello stabilito in origine dal mittente__.

## Servizi Nascosti

## In pratica

Il software Tor presenta una interfaccia _a riga di comando (command line)_ che permette di specificare varie opzioni, anche se la maggior parte di esse vanno specificate nel file di configurazione denominato _torrc_.

Tor permette l'instradamento del traffico nella propria rete offrendo all'utente un __proxy SOCKS__: istruendo le applicazioni di dirigere i propri __socket__ attraverso il __proxy__, il loro traffico passerà per la rete di Tor.

### Vidalia

### Tor Browser

### Gestire il proprio servizio nascosto

## Bloccare l'accesso a Tor

Un ente potrebbe voler bloccare l'accesso alla rete Tor all'interno della propria infrastruttura per ovvie ragioni di sicurezza. Il miglior metodo è bloccare completamente il traffico destinato __agli indirizzi IP che corrispondo ai nodi Tor pubblici__, bloccando effettivamente l'accesso poichè il software ha bisogno di connettersi ad almeno un nodo direttamente per avere l'accesso alla rete.

Un limite di questo tipo è però facilmente aggirabile tramite l'utilizzo di __bridge node (bridge relay)__, ovvero dei __nodi Tor non pubblici__. __Tor è software libero__, di conseguenza __chiunque può aprire un proprio (bridge) relay__ e __accedere alla rete da luoghi che bloccano i nodi pubblici attraverso di esso__.

Purtroppo __non è possibile bloccare completamente l'accesso a Tor senza applicare enormi, irrealistiche restrizioni all'accesso a internet__.

## Punti deboli

Tor presenta una serie di punti deboli che vanno considerati da ogni utilizzatore del programma:

- Gli __exit node__ possono leggere tutto il traffico di tutti gli utenti tor che li usano agendo effettivamente da __man in the middle__ per la natura stessa del protocollo
- Tor viene convenzionalmente usato per mascherare l'origine del traffico HTTP, però un utente inesperto potrebbe __abilitare vari plugin del browser__ che sono in grado di __comunicare in rete liberamente__ (ad esempio __Adobe Flash__) e dunque finirebbero per __contattare direttamente il destinatario senza passare per Tor__ rendendo potenzialmente vani i tentativi di preservare l'anonimato
- Un sito web potrebbe includere tra i propri script delle subroutine in grado di __ottenere informazioni sul sistema client__ compromettendo l'anonimato
- Un utente potrebbe __lasciare indizi sulla propria identità__ durante la normale navigazione sul web tramite Tor

Queste considerazione non comprendono la possibilità di attacchi mirati al controllo della rete Tor che rischierebbero di compromettere l'anonimato e la privacy di tutti gli utenti.

Inoltre, la rete di Tor è __estremamente lenta__ perchè:
- ogni nodo deve sottoporre ogni pacchetto a grande quantità di operazioni di crittografia
- è impossibile stabilire il contenuto dei pacchetti e dunque è impossibile scartare quelli inutili o deleteri
- i pacchetti sono incapsulati in numerosi strati crittografici, che aumentano di molto la dimensione dei dati da inviare
- potrebbe essere necessario ricalcolare spesso il percorso di routing a causa dell'instabilità dei nodi

Per questi motivi è anche possibile __saturare la rete con dati inutili allo scopo di deterrente per gli utenti di Tor__.
