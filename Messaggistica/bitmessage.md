# Bitmessage

Bitmessage è un __protocollo__ per lo scambio di __posta elettronica__ in maniera __sicura__, __privata__, __intracciabile__ e, volendo, __anonima__.

Ne esiste una sola implementazione completa (al momento della scrittura di questo documento) chiamata __PyBitmessage__ e disponibile per __Windows__, __GNU/Linux__ e __OSX__.

il protocollo, in breve, definisce che:

- ogni utente è identificato da una __coppia di chiavi crittografiche__ e da un __indirizzo__ derivato dalla sua __chiave pubblica__
- ogni messaggio è __firmato__ con la chiave privata del mittente e __interamente crittografato__ con la chiave pubblica del destinatario.
    - l'unica informazione visibile del messaggio è il __TTL__ che ha lo scopo di evitare il __flooding__ della rete con lo stesso messaggio
    - i messaggi rimangono nella rete solo per qualche giorno, poi sono persi per sempre se il mittente non decide di reinviare
    - è necessario completare un __Proof Of Work__ per l'invio di un messaggio
- la rete implementa meccanismi __anti-flooding__ per evitare la saturazione della stessa

__flooding__: come dice il nome, si tratta dell'_allagamento_ di una rete, ovvero di un flusso di dati in ingresso nella rete maggiore di quello in uscita che arriverà prima o poi a rendere inutilizzabile il sistema.

__Proof Of Work__: si tratta di una _prova_ che dimostra che una certa quantità di _lavoro_ è stata effettuata. Viene inserito nei servizi come __Bitmessage__ in allegato ai messaggi per provare che del tempo (pochi secondi o minuti) è stato speso per creare il proof of work. Essendo obbligatorio un nuovo proof of work in ogni messaggio, questo sistema rende quasi impossibile il flooding.

## Come si usa

__PyBitmessage__ è disponibile gratuitamente sul sito [bitmessage.org](https://bitmessage.org). Il software è molto semplice da usare e ulteriori informazioni sono contenute nello stesso.

- il software creerà un nuovo indirizzo Bitmessage al suo avvio
- è possibile mantenere una lista contatti in cui memorizzare gli indirizzi conosciuti
- Esistono i __Canali__ di Bitmessage che agiscono da _Mailing List_, permettendo una variante della messaggistica di gruppo.

## Come funziona

Essenzialmente, il protocollo __Bitmessage__ è molto semplice, infatti ogni nodo:

- si collega direttamente ad altri nodi
- tenta di decrittografare ogni messaggio che riceve con la propria chiave privata
    - se funziona, allora il messaggio è destinato a questo nodo
    - se non funziona, il TTL viene diminuito e il messaggio viene rispedito sulla rete
- ai messaggi inviati va allegato un __proof of work__ molto tassante
    - questo è necessario per il funzionamento della rete, ma il software deve usare molte risorse per il __proof of work__

Il protocollo descrive procedure di __proof of work__ e __anti flooding__ molto complesse che permettono il corretto funzionamento della rete e fungono da repellente per eventuali attaccanti.

## Confronto con E-Mail

La maggior parte dei problemi di __PyBitmessage__ derivano dal suo alto livello di sicurezza, che porta però a __bassa accessibilità__ e mancanza di __comodità__ nell'uso del software.

Alcuni dei maggiori problemi di accessibilità del software sono:

- mancanza di __client avanzati__ che invece esistono per le __E-Mail__ (ad esempio Mozilla _Thunderbird_ o Microsoft _Outlook_) e permettono di organizzare in maniera complessa la posta,
- impossibilità di un'istanza del software di ricevere messaggi _non destinati ad essa_ (a scopo di _caching_). Anche se in futuro fosse possibile, sarebbero necessarie le __chiavi private__ di accesso dei destinatari
- impossibilità (per ora) di usare __indirizzi arbitrari__ come ad esempio _nome.cognome@azienda.it_, costringendo invece gli utenti ad usare indirizzi auto generati impossibili da memorizzare,
- elevato uso di __risorse hardware__ ed elevata __congestione di rete__ causata dal software,
- mancanza di __client per tutte le piattaforme__ e di __client web__, questi ultimi perchè non permetterebbero di mantenere la sicurezza,
- non ancora supportato (al momento della scrittura) l'uso di __password__ per proteggere le proprie chiavi private.

Finchè non viene trovata soluzione ad almeno _parte_ di questi problemi, BitMessage __non è pronto__ per rimpiazzare le __E-Mail__.
