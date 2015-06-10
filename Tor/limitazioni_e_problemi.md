# Limitazioni e Problemi

## Punti deboli

Tor presenta una serie di punti deboli che vanno considerati da ogni utilizzatore del programma:

- Gli __exit node__ possono leggere tutto il traffico di tutti gli utenti tor che li usano agendo effettivamente da __man in the middle__ per la natura stessa del protocollo
- Tor viene convenzionalmente usato per mascherare l'origine del traffico HTTP, però un utente inesperto potrebbe __abilitare vari plugin del browser__ che sono in grado di __comunicare in rete liberamente__ (ad esempio __Adobe Flash__ e __Microsoft Silverlight__) e dunque finirebbero per __contattare direttamente il destinatario senza passare per Tor__ rendendo potenzialmente vani i tentativi di preservare l'anonimato
- Un sito web potrebbe includere tra i propri script delle subroutine in grado di __ottenere informazioni sul sistema client__ compromettendo l'anonimato
- Un utente potrebbe __lasciare indizi sulla propria identità__ durante la normale navigazione sul web tramite Tor

Queste considerazione non comprendono la possibilità di attacchi mirati al controllo della rete Tor che rischierebbero di compromettere l'anonimato e la privacy di tutti gli utenti.

## Lentezza

La rete Tor è __estremamente lenta__ perchè:
- ogni nodo deve sottoporre ogni pacchetto a grande quantità di operazioni di crittografia
- è impossibile stabilire il contenuto dei pacchetti e dunque è impossibile scartare quelli inutili o deleteri
- i pacchetti sono incapsulati in numerosi strati crittografici, che aumentano di molto la dimensione dei dati da inviare
- potrebbe essere necessario ricalcolare spesso il percorso di routing a causa dell'instabilità dei nodi

Per questi motivi è anche possibile __saturare la rete con dati inutili come deterrente per gli utenti di Tor__.

### Exit node monitoring

Operando un __Exit Node__ è possibile catturare tutto il traffico degli utenti __Tor__ poichè come visto prima, __Tor__ protegge il traffico solo fino all'__exit node__. Se il traffico dall'__exit node__ alla destinazione finale non è crittografato, l'__exit node__ può leggere il traffico senza problemi.

Un utente inesperto potrebbe dunque inviare dati importanti in chiaro attraverso __Tor__: la sorgente di questi dati sarebbe anonima, ma il contenuto potrebbe essere letto da chiunque si trovi nel percorso tra __exit node__ e __destinatario__, __exit node compreso__.
