# Bitcoin

Bitcoin è una valuta digitale (la prima nella storia ad avere un reale valore) e un protocollo per lo scambio della stessa via rete. Esistono numerose implementazioni, varianti ed evoluzioni del protocollo Bitcoin, anche usate per motivi diversi dallo scambio di denaro.

## Concetti

Il protocollo Bitcoin consiste in una rete decentralizzata (da ora in poi detta semplicemente __"la rete"__) di nodi che processano le richieste di trasferimento di denaro e da una __blockchain__ ovvero una lista di tutte le transazioni eseguite a partire dall'origine della moneta.

- Un __portafoglio__ è usato come contenitore di denaro (__Bitcoins__) identificato dalla sua __chiave pubblica__, ma in realtà è semplicemente una __coppia di chiavi crittografiche__ usate per associare la quantità di denaro posseduta al proprietario.
    - E' possibile creare liberamente uno o più __portafogli__.
- Una __transazione__ è un trasferimento di denaro: tutte le transazioni vanno validate dalla rete e sono poi aggiunte, se valide, alla __blockchain__.
    - la rete considera valida una __transazione__ solo se il  __portafoglio sorgente__ possiede __sufficienti bitcoin__ per poterli trasferire al __portafoglio destinatario__.
- un __nodo della rete Bitcoin__ consiste semplicemente in un computer in grado di comunicare con altri membri della rete.
    - i nodi eseguono il software di una delle implementazioni del protocollo Bitcoin
    - i nodi collaborano e si fidano delle informazioni ricevute dagli altri nodi solo se possono verificarne la validità indipendentemente. In alternativa, vengono considerate valide le informazioni solo se gran parte della rete le considera valide

Dalle suddette informazioni possiamo dedurre che: 
- non esiste alcun tipo di centralizzazione o server se non un __tracker__ usato dai nodi per scoprire gli indirizzi IP degli altri nodi
- un portafoglio vuoto è irrilevante per la rete, ma entra a far parte della blockchain se riceve dei bitcoin.
- ovviamente, per generare una transazione da un portafoglio, essa va comunicata alla rete e __firmata digitalmente__ con la __chiave privata__ associata al __portafoglio__.
- le transazioni vengono diffuse e validate da ogni nodo. Se considerate valide (ovvero il portafoglio sorgente ha sufficienti bitcoin), vengono aggiunte alla __blockchain__ da tutta la rete.
- la quantità di bitcoin in un portafoglio è calcolabile semplicemente leggendo tutte le transazioni che lo riguardano in ordine cronologico

## Incentivi e disincentivi

Per disincentivare la creazione di __enormi quantità di transazioni in poco tempo__ (che creerebbe numerosi problemi alla rete) le transazioni vanno accompagnate con un __proof of work__, ovvero la soluzione ad un complesso problema matematico, per provare che del tempo è stato speso per generare la transazione.

### La messa in circolo tramite Bitcoin Mining

All'origine della rete, essa è __inutilizzabile__ a causa delle sue stesse regole: __se nessuno può trasferire bitcoins senza possederli, come è possibile ottenere dei bitcoin?__

I bitcoin vengono messi in circolazione tramite __bitcoin mining__, che consiste nel effettuare i controlli matematematici per __provare la validità di una transazione__.

Il processo di __controllo della validità di una transazione__ è lento e richiede molta potenza di calcolo, di coseguenza __per incentivarlo, la rete premia i "lavoratori" inserendo dei bitcoin nel loro portafoglio__.

Nel tempo, i Bitcoin hanno acquistato __un valore anche di centinaia di dollari per un singolo Bitcoin__ quindi il __bitcoin mining__ può essere un'attività estremamente __lucrativa__.

### Proof of Work

Un proof of work consiste semplicemente nel trovare un __valore__ il cui __hash SHA-256__, quando rappresentato tramite notazione esadecimale, inizia con una certa quantità di __zeri__.

Esempi:

| Valore | Hash (Troncato)|
| -- | -- |
| test | 9f86d081884c7d65... |
| valore_di_esempio | a9a23159b7c4555b... |
| stringa_hash | 4b4c1b2efca629b62... |

Essendo l'__hashing__ una procedura __non prevedibile__, l'unico modo per trovare un hash che soddisfi i requisiti è __procedere casualmente__.

Dunque il tempo richiesto per calcolare __miliardi di hash__ fino a trovare un valore che soddisfi i __requisiti__ è immenso, rendendo il __proof-of-work__ una procedura inventata per essere lenta, in modo da __provare__ che numerosi minuti sono stati usati.

### Bitcoin mining come reddito principale


## Anonimato



Secondo le regole suddette, __tutti possono sapere quanti soldi ci sono in ogni portafoglio e l'intero elenco di tutte le transazioni della storia__, però __i portafogli sono identificabili esclusivamente tramite la loro chiave pubblica, non conservano informazioni sul proprietario__.

I Bitcoin sono infatti molto usati per __pagare servizi o merci illegali__, ma vengono anche accettati da alcuni legittimi negozi o come donazioni.

## Limitazioni, problemi e vulnerabilità

## L'esplosione di popolarità e la nascita dei cloni

### La caduta di Mt. Gox

### Il mistero delle origini dei Bitcoin