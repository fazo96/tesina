# Bitmessage

Bitmessage è un __protocollo__ per lo scambio di __posta elettronica__ in maniera __sicura__, __privata__, __intracciabile__ e, volendo, __anonima__.

Ne esiste una sola implementazione completa (al momento della scrittura di questo documento) chiamata __PyBitmessage__ e disponibile per __Windows__, __GNU/Linux__ e __OSX__.

il protocollo, in breve, definisce che:

- ogni utente è identificato da una __coppia di chiavi crittografiche__ e da un __indirizzo__ derivato dalla __chiave pubblica__
- ogni messaggio è __firmato__ con la chiave privata del mittente e __interamente crittografato__ con la chiave pubblica del destinatario.
    - l'unica informazioni visibile del messaggio è il __TTL__ che ha lo scopo di evitare il __flooding__ della rete con lo stesso messaggio
