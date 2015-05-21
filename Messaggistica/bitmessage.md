# Bitmessage

Bitmessage è un __protocollo__ per lo scambio di __posta elettronica__ in maniera __sicura__, __privata__, __intracciabile__ e, volendo, __anonima__.

Ne esiste una sola implementazione completa (al momento della scrittura di questo documento) chiamata __PyBitmessage__ e disponibile per __Windows__, __GNU/Linux__ e __OSX__.

il protocollo, in breve, definisce che:

- ogni utente è identificato da una __coppia di chiavi crittografiche__ e da un __indirizzo__ derivato dalla __chiave pubblica__
- ogni messaggio è __firmato__ con la chiave privata del mittente e __interamente crittografato__ con la chiave pubblica del destinatario.
    - l'unica informazione visibile del messaggio è il __TTL__ che ha lo scopo di evitare il __flooding__ della rete con lo stesso messaggio
    - i messaggi rimangono nella rete solo per qualche giorno, poi sono persi per sempre se il mittente non decide di reinviare
    - è necessario completare un __Proof Of Work__ (spiegato nel capitolo Bitcoin di questo documento) per l'invio di un messaggio 
- la rete implementa meccanismi __anti-flooding__ per evitare la saturazione della stessa

## Come si usa

__PyBitmessage__ è disponibile gratuitamente sul sito [bitmessage.org](https://bitmessage.org). Il software è molto semplice da usare e ulteriori informazioni sono contenute nello stesso.

- il software creerà un nuovo indirizzo Bitmessage al suo avvio
- è possibile mantenere una lista contatti in cui memorizzare gli indirizzi conosciuti
- Esistono i __Canali__ di Bitmessage che agiscono da Mailing List.

## Come funziona

Essenzialmente, il protocollo __Bitmessage__ è molto semplice, infatti ogni nodo:

- si collega direttamente ad altri nodi
- ogni messaggio che riceve tenta di decrittografarlo con la propria chiave privata
    - se funziona, allora il messaggio è destinato a questo nodo
    - se non funziona, il TTL viene diminuito e il messaggio viene rispedito sulla rete
- ai messaggi inviati va allegato un __proof of work__ molto tassante
    - questo è necessario per il funzionamento della rete, ma il software deve usare molte risorse per il __proof of work__

In realtà, esso descrive procedure di __proof of work__ e __anti flooding__ molto complesse che permettono il corretto funzionamento della rete e il blocco di eventuali attaccanti.

