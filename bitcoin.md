# Bitcoin

Bitcoin è una valuta digitale (la prima nella storia ad avere un reale valore) e un protocollo per lo scambio della stessa via rete. Esistono numerose implementazioni, varianti ed evoluzioni del protocollo Bitcoin, anche usate per motivi diversi dallo scambio di denaro.

## Concetti

Il protocollo Bitcoin consiste in una rete decentralizzata (da ora in poi detta semplicemente __"la rete"__) di nodi che processano le richieste di trasferimento di denaro e da una __blockchain__ ovvero una lista di tutte le transazioni eseguite a partire dall'origine della moneta.

- Un __portafoglio__ è usat come contenitore di denaro (__Bitcoins__) identificato dalla sua __chiave pubblica__, ma in realtà è semplicemente una __coppia di chiavi crittografiche__ usate per associare la quantità di denaro posseduta al proprietario.
    - E' possibile creare liberamente uno o più __portafogli__.
- Una __transazione__ è un trasferimento di denaro: tutte le transazioni vanno validate dalla rete e sono poi aggiunte, se valide, alla __blockchain__.
    - la rete considera valida una __transazione__ solo se il  __portafoglio sorgente__ possiede __sufficienti bitcoin__ per poterli trasferire al __portafoglio destinatario__.
- __un nodo della rete Bitcoin__ consiste semplicemente in un computer in grado di comunicare con altri membri della rete.
    - i nodi eseguono il software di una delle implementazioni del protocollo Bitcoin
    - i nodi collaborano e si fidano delle informazioni ricevute dagli altri nodi solo se possono verificarne la validità indipendentemente. In alternativa, vengono considerate valide le informazioni solo se gran parte della rete le considera valide

Dalle suddette informazioni possiamo dedurre che: 
- non esiste alcun tipo di centralizzazione o server se non un __tracker__ usato dai nodi per scoprire gli indirizzi IP degli altri nodi
- un portafoglio vuoto è irrilevante per la rete, ma entra a far parte della blockchain se riceve dei bitcoin.
- ovviamente, per generare una transazione da un portafoglio, essa va comunicata alla rete e __firmata digitalmente__ con la __chiave privata__ associata al __portafoglio__.
- le transazioni vengono diffuse e validate da ogni nodo. Se considerate valide (ovvero il portafoglio sorgente ha sufficienti bitcoin), vengono aggiunte alla __blockchain__ da tutta la rete.
- la quantità di bitcoin in un portafoglio è calcolabile semplicemente leggendo tutte le transazioni che lo riguardano in ordine cronologico

### La messa in circolo tramite Bitcoin Mining

I bitcoin vengono messi in circolazione tramite __bitcoin mining__, che consiste nel diffondere una __"taglia"__ per la __soluzione di un complesso problema matematico__ in modo che __la rete conceda dei bitcoin come premio a chi lo risolva per primo__. Limitando il numero di problemi matematici e impostando una quantità specifica come premio, viene decisa la quantità di bitcoin totale.

Nel tempo, i Bitcoin hanno acquistato __un valore anche di centinaia di dollari per un singolo Bitcoin__ quindi il __bitcoin mining__ può essere un'attività estremamente __lucrativa__.

## Anonimato

Secondo le regole suddette, __tutti possono sapere quanti soldi ci sono in ogni portafoglio e l'intero elenco di tutte le transazioni della storia__, però __i portafogli sono identificabili esclusivamente tramite la loro chiave pubblica, non conservano informazioni sul proprietario__.

I Bitcoin sono infatti molto usati per __pagare servizi o merci illegali__, ma vengono anche accettati da alcuni legittimi negozi o come donazioni.

## Limitazioni, problemi e vulnerabilità

## L'esplosione di popolarità e la nascita dei cloni

### La caduta di Mt. Gox

### Il mistero delle origini dei Bitcoin