# Soluzioni ai problemi del Web

Dopo aver definito le caratteristiche _problematiche_ del moderno _World Wide Web_, vediamo le loro possibili soluzioni.

## Navigazione

Riassumendo, i problemi del navigare il web sono: il __tracciamento__, l'__analisi comportamentale__ e le __pubblicità mirate__: vediamo ora come risolverli.

### Ad Blocker

Un __Ad Blocker__ è un software in grado di nascondere le pubblicità sulle pagine web visitate. Gli __Ad Blocker__ più avanzati sono in grado di:

- nascondere gli elementi della pagina dedicati alle pubblicità;
- evitare l'esecuzione di __script__ o memorizzazione di __cookie__ non necessari per la fruizione dei contenuti della pagina, principalmente quelli dedicati alle pubblicità o alla raccolta dati;

Gli __Ad Blocker__ più conosciuti sono __AdBlock__ e __AdBlock Plus__, entrambi però sono __Closed Source__ e generalmente considerati meno affidabili dell'alternativa __uBlock__, che si presenta come una soluzione più moderna, performante e completamente __Open Source__.

### Ghostery

Tramite il plugin __Ghostery__, disponibile per tutti i browser web più usati, è possibile:

- vedere le informazioni di tracciamento che vengono inviate ai server dei vari siti web che utilizziamo
- conoscere le aziende a cui sono destinate tali informazioni
- bloccare l'invio delle informazioni di tracciamento

__Per provare tutto ciò__ è infatti sufficiente installare __Ghostery__ e, seguendo le istruzioni su [ghostery.com/it](http://ghostery.com/it/), collegarsi a uno o più social networks o servizi come Google, LinkedIn, Facebook, notando __immediatamente__ lo scambio di dati di tracciamento tra noi e i server di questi servizi.

Attenzione però: __Ghostery è un software Closed Source__, dunque non è possibile sapere esattamente che tipo di operazioni esegua, la qualità della sua efficacia, e eventuali __backdoor__ presenti o __raccolte dati__ effettuate dal software.

## Servizi

Per i servizi come __File Sharing__, __Messaggistica__ e __Cloud Storage__ le soluzioni devono preferibilmente essere:

- __Open Source__ per permettere la revisione del codice da parte degli utenti e degli esperti di sicurezza,
- __decentralizzate__ o, alternativamente, permettere il __self-hosting__,
- sicure utilizzando __crittografia__ e __firme digitali__,
- configurabili e adattabili a diverse situazioni e casi d'uso,
- rispettare la __privacy__ e consentire l'__anonimato__, limitando i dati immagazzinati o evitandone completamente la raccolta.

### Self-Hosting

Il __self-hosting__ è la caratteristica di un __servizio__ che permette di creare diverse __istanze personalizzate__ gestite internamente da un'organizzazione o un privato. Questa caratteristica è associata ai servizi __liberi ma non decentralizzabili__ come ad esempio un __DBMS__.

### Decentralizzazione

La __decentralizzazione__ è la caratteristica di un __servizio__ che permette di non dipendere da un singolo __server__ o un'insieme di pochi server, consentendogli di funzionare semplicemente con una rete di __client__ collegati tra loro. Spesso, per far si che i client scoprano i rispettivi _indirizzi IP_ permettendo loro di connettersi, è comunque necessario un server di tipo __tracker__.

Un __tracker__ differisce da un classico server perchè agisce semplicemente da punto di incontro per i client, permettendo di avvisare della propria esistenza e quindi di conoscersi. Le informazioni scambiate tra i client non passano mai direttamente dal __tracker__. Usando un servizio decentralizzato (come __Syncthing__) è spesso possibile scegliere quale o quali tracker utilizzare o di non utilizzarne alcuni ma tentare direttamente la connessione ad alcuni indirizzi IP oppure di gestire il proprio tracker privato.

Una __Distributed Hash Table__ è una tecnologia che permette di avere un __key-value store__ (tabella a due colonne) condivisa dai nodi di una rete decentralizzata.  Un key-value store contiene dati in formato _coppia-valore_: questo permette di accedere al valore determinato da una cerca chiave.

Per capire meglio, possiamo immaginare un __key-value store__ come una tabella a due colonne dove per ogni riga la prima colonna è la _chiave_, ovvero l'identificativo del dato mentre la seconda contiene il dato stesso.

- Nelle reti distribuite viene spesso usato per associare l'__indirizzo IP__ di un utente con il suo profilo, indirizzo, chiave pubblica o altro
- in caso di __BitTorrent__, ad esempio, per ogni _torrent_ (che agisce da chiave) il valore è una lista di _indirizzi IP_ di clients che posseggono quel torrent
- La __DHT__, come da definizione, non è offerta da un server ma è distribuita nella rete di _clients_.

La conbinazione tra __DHT__ e __Trackers__ affidabili rende stabile un servizio decentralizzato, permettendo ai nodi di collegarsi tra loro in maniera efficiente.
