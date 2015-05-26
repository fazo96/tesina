## Concetti

Il protocollo Bitcoin consiste in una rete decentralizzata (da ora in poi detta semplicemente __"la rete"__) di nodi che processano le richieste di trasferimento di denaro e da una __blockchain__ ovvero una lista di tutte le transazioni eseguite a partire dall'origine della moneta.

- Un __portafoglio__ è usato come contenitore di denaro (__Bitcoins__) identificato dalla sua __chiave pubblica__, ma in realtà è semplicemente una __coppia di chiavi crittografiche__ usate per associare la quantità di denaro posseduta al proprietario.
    - E' possibile creare liberamente uno o più __portafogli__.
- Una __transazione__ è un trasferimento di denaro: tutte le transazioni vanno validate dalla rete e sono poi aggiunte, se valide, alla __blockchain__.
    - la rete considera valida una __transazione__ solo se il  __portafoglio sorgente__ possiede __sufficienti bitcoin__ per poterli trasferire al __portafoglio destinatario__.
- un __nodo della rete Bitcoin__ consiste semplicemente in un computer in grado di comunicare con altri membri della rete.
    - i nodi eseguono il software di una delle implementazioni del protocollo Bitcoin.
    - i nodi collaborano e si fidano delle informazioni ricevute dagli altri nodi solo se possono verificarne la validità indipendentemente. In alternativa, vengono considerate valide le informazioni solo se gran parte della rete le considera valide.

Dalle suddette informazioni possiamo dedurre che: 
- non esiste alcun tipo di centralizzazione o server se non un __tracker__ usato dai nodi per scoprire gli indirizzi IP degli altri nodi
- un portafoglio vuoto è irrilevante per la rete, ma entra a far parte della blockchain se riceve dei bitcoin.
- ovviamente, per generare una transazione da un portafoglio, essa va comunicata alla rete e __firmata digitalmente__ con la __chiave privata__ associata al __portafoglio__.
- le transazioni vengono diffuse e validate da ogni nodo. Se considerate valide (ovvero il portafoglio sorgente ha sufficienti bitcoin), vengono aggiunte alla __blockchain__ da tutta la rete.
- la quantità di bitcoin in un portafoglio è calcolabile semplicemente leggendo tutte le transazioni che lo riguardano in ordine cronologico

Esistono inoltre:

- __hardware wallet__, ovvero portafogli contenuti in un dispositivo hardware come una chiavetta USB, che possono essere usati solo mentre sono connessi alla macchina.
- __fondi condivisi__, ovvero dei fondi che richiedono la firma digitale di __multipli portafogli__ per essere trasferiti.
