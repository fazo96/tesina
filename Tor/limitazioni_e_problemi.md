# Limitazioni e Problemi

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
