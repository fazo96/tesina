# Il Cloud Storage

Con __Cloud Storage__ si intende l'_immagazzinare dei dati in remoto_, utilizzando _un servizio offerto da una terza parte_. Questo sistema presenta molteplici vantaggi:

- i dati sono accessibili da ovunque sia presente una connessione a internet
- è possibile dare l'accesso ai dati a qualcuno senza doverli trasferire fisicamente
- non si è limitati dallo spazio disponibile sul proprio dispositivo
- non è necessario sincronizzare le informazioni manualmente tra dispositivi diversi

I più diffusi servizi di __Cloud Storage__ sono __Google Drive__ e __Dropbox__.

## Il problema del Cloud Storage

Questa tecnologia presenta anche degli svantaggi:

- è necessario affidare le proprie informazioni a __una terza parte__, facendo emergere problematiche di __privacy__, __sicurezza__ e __fiducia__
- vi sono spesso limiti di __spazio__ o di __utilizzo__ ed è necessario pagare per alleviarli o rimuoverli
- non sempre è disponibile una buona connessione a internet
- in caso di fallimento dell'infratruttura della terza parte, __i dati o la loro accessibilità potrebbe compromettersi__

## La soluzione: i sistemi decentralizzati

La maggior parte delle problematiche del __Cloud Storage__ sono derivate da __centralizzazione__ e __delega__ della gestione a una __terza parte__. Questi problemi non esistono se vengono utilizzate tecnologie di __Cloud Storage decentralizzato__, infatti queste tecnologie:

- funzionano indipendentemente (o quasi, in alcuni casi), senza bisogno di una __terza parte__, dunque
    - non esiste il problema del fallimento dell'infrastruttura della terza parte
- non hanno bisogno di __server__ per conservare le informazioni, perchè
    - i dati sono inviati direttamente da un dispositivo all'altro
- funzionano in una rete locale non connessa a internet
- solo limitati solo dalla potenza fisica dei dispositivi e dalla qualità della connessione tra loro

I più diffusi sistemi di Cloud Storage decentralizzati sono __Bittorrent Sync__ e __Syncthing__.

### Bittorrent Sync

__Bittorrent Sync__ (anche detto __BTSync__) è un software proprietario di __Bittorrent Incorporated__ che implementa il __Cloud Storage decentralizzato__.

Il software è disponibile per __Windows__, __GNU/Linux__, __OSX__, __Android__, __iOS__, __Windows Phone__ e __Kindle Fire__.

Esso è però considerato dalla comunità come una __soluzione parziale__ al problema del Cloud Storage, perchè Bittorrent Sync è una __tecnologia proprietaria, chiusa__ e dunque __potenzialmente inaffidabile__ dal punto di vista __della sicurezza e della privacy__.
