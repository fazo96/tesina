# Condividere file con Sicurezza

## Il Cloud Storage

Con __Cloud Storage__ si intende l'_immagazzinare dei dati in remoto_ a scopo di File Sharing, File Hosting o backup personale, utilizzando _un servizio offerto da una terza parte_. Questo sistema presenta molteplici vantaggi:

- i dati sono accessibili da ovunque sia presente una connessione a Internet
- è possibile concedere l'accesso ai dati a qualcuno senza doverli trasferire fisicamente
- non si è limitati dallo spazio disponibile sul proprio dispositivo
- non è necessario sincronizzare le informazioni manualmente tra dispositivi diversi

Per promuovere la chiarezza del documento, con __File Sharing__ intendiamo la condivisione di file tra utenti, ad esempio un documento che coinvolge i propri colleghi o amici e parenti. Con __File Hosting__ intendiamo invece la condivisizone di file tra utenti su larga scala, ad esempio un cortometraggio distribuito liberamente in rete e scaricato da milioni di persone. Spesso i __provider__ che offrono questi servizi (come Dropbox, Google Drive o Mega) offrono entrambe le soluzioni.

I più diffusi servizi di __Cloud Storage__ sono __Google Drive__ e __Dropbox__.

## Vulnerabilità e problemi

Questa tecnologia presenta anche degli svantaggi:

- è necessario affidare le proprie informazioni a __una terza parte__, facendo emergere problematiche di __privacy__, __sicurezza__ e __fiducia__;
- vi sono spesso limiti di __spazio__ o di __utilizzo__ ed è necessario pagare per alleviarli o rimuoverli;
- non sempre è disponibile una buona connessione a internet;
- in caso di fallimento dell'infrastruttura della terza parte, __i dati privati potrebbero essere divulgati o resi inaccessibili__.

## La soluzione: i sistemi decentralizzati

La maggior parte delle problematiche del __Cloud Storage__ sono derivate da __centralizzazione__ e __delega__ della gestione a una __terza parte__. Questi problemi non esistono se vengono utilizzate tecnologie di __Cloud Storage decentralizzato__, infatti queste tecnologie:

- funzionano indipendentemente (o quasi, in alcuni casi), senza bisogno di una __terza parte__, dunque non esiste il problema del fallimento dell'infrastruttura centralizzata gestita dalla terza parte;
- non hanno bisogno di __server__ per conservare le informazioni, perchè i dati sono inviati direttamente da un dispositivo all'altro;
- funzionano anche in una rete locale non connessa a Internet;
- sono limitati solo dalla _potenza di calcolo_ dei dispositivi e dalla _qualità della connessione_ tra loro.

I più diffusi sistemi di _File Sharing_ decentralizzati sono __Bittorrent Sync__ e __Syncthing__, mentre per il _File Hosting_ su larga scala il servizio dominante è __BitTorrent__ seguito da _E-Mule_.

### Bittorrent

BitTorrent è un __protocollo__ di __file hosting__ su larga scala che permette di creare un file chiamato __torrent__ molto leggero (pochi kilobyte) che, tramite un client __BitTorrent__, può essere aperto per contattare gli utenti che possiedono il/i file descritti dal torrent per scaricarli direttamente dai loro computer, senza passare per alcun server se non il __tracker__ necessario per trovare gli indirizzi __IP__ di chi possiede il file.

Un utente che entra in possesso di un __torrent__ legato ad esempio a una collezione di cortometraggi amatoriali può, tramite un client Bittorrent, scaricare i file dei cortometraggi dal computer degli altri utenti. I dati si diffondono nella rete partendo dai creatori del __torrent__.

Il file __.torrent__ contiene semplicemente:

- il nome e la dimensione dei file legati al torrent;
- il/i __tracker__ a cui collegarsi per trovare gli utenti che possiedono i file.

Tramite __tracker__, gli utenti pubblicizzano il fatto di possedere un determinato __torrent__ in modo da trovare gli interessati e diffondere ulteriormente i file o ottenere le parti mancanti. Questo significa che:

- un __.torrent__ popolare è molto più veloce da scaricare. In gergo viene chiamato __healthy torrent__;
- un __.torrent__ abbandonato è impossibile da scaricare, rendendo persi per sempre i dati contenuti. Questo viene chiamato __dead torrent__.

In particolare, coloro che hanno il __100%__ dei dati del torrent ma rimangono connessi alla rete sono chiamati __Seed__ perchè fanno da __seme__ per la diffusione dei dati, mentre gli altri sono chiamati __peer__. I __leech__, invece, sono coloro che scaricano dati ma non li redistribuiscono (consumando la preziosa banda in upload dei seed e dei peer) e sono ovviamente nocivi per la vita dei __torrent__.

BitTorrent supporta anche __crittografia__ e __hole punching__ per superare __NAT__ non simmetrici e promuovere la privacy. Utilizza principalmente __UDP__ per le connessioni. A causa della decentralizzazione e della conseguente difficoltà nel bloccare l'accesso ai file, viene usato spesso dai __pirati informatici__ ma a differenza dall'__opinione popolare__, è usato solo parzialmente dai __pirati__ ed è __illegale__ solo se usato per distribuire materiale protetto da copyright senza permesso.

### Bittorrent Sync

__Bittorrent Sync__ (anche detto __BTSync__) è un software proprietario di __Bittorrent Incorporated__ che implementa il __file sharing decentralizzato__.

Il software è disponibile per __Windows__, __GNU/Linux__, __OSX__, __Android__, __iOS__, __Windows Phone__ e __Kindle Fire__.

Differisce da __BitTorrent__ poichè Sync, come si può capire dal nome, permette la _sincronizzazione dei dati_ usando il protocollo BitTorrent, senza limitarsi alla _diffusione dei dati_ come le implementazioni standard di quest'ultimo.

Esso è però considerato dalla comunità come una __soluzione parziale__ al problema del file sharing, perchè Bittorrent Sync è una __tecnologia proprietaria, chiusa__ e dunque __potenzialmente inaffidabile__ dal punto di vista __della sicurezza e della privacy__.
