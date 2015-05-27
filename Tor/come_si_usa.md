## In pratica

Il software Tor presenta una interfaccia _a riga di comando (command line)_ che permette di specificare varie opzioni, anche se la maggior parte di esse vanno specificate nel file di configurazione denominato _torrc_.

![man tor](http://i.imgur.com/ML6ZGZQ.png)
- _Immagine:_ pagina di manuale __UNIX__ parziare per __Tor__.

Tor permette l'instradamento del traffico nella propria rete offrendo all'utente un __proxy SOCKS__: istruendo le applicazioni di dirigere i propri __socket__ attraverso il __proxy__, il loro traffico passerà per la rete di Tor.

### Vidalia

Essendo __Tor__ un software con interfaccia __a riga di comando__, è stata sviluppata l'interfaccia grafica __Vidalia__ che permette di gestire e configurare __Tor__ senza mai modificare manualmente __file di configurazione__ o utilizzare la __riga di comando__.

![Vidalia](http://i.imgur.com/ZJ4JF7a.png)
- _Immagine:_ __Vidalia__ in esecuzione sul mio computer, connesso alla rete __Tor__.

Questa interfaccia è molto apprezzata dagli utenti meno esperti che necessitano di eseguire applicazioni o servizi attraverso Tor.

![Vidalia Network](http://i.imgur.com/d0iqO9N.png)
- _Immagine:_ mappa (disegnata da __Vidalia__) che mostra la posizione nel mondo dei __nodi Tor__ a cui il mio computer era connesso durante la mia prova.

Per chi ha __solo bisogno__ di __navigare il Web attraverso Tor__, è consigliato invece il __Tor Browser__.

### Tor Browser

Il __Tor Browser__ (in precedenza chiamato __Tor Browser Bundle__) è una versione _estesa_ e _modificata_ di __Mozilla Firefox__ che consiste in un __browser web indipendente__ che __naviga esclusivamente tramite Tor__ e contiene una serie di __componenti aggiuntivi utili per proteggere la propria privacy e identità__

__Tor Browser__ è __portatile (dunque non richiede installazione)__ ed è disponibile per __Windows__, __OSX__ e __GNU/Linux__.

Il progetto, molto popolare per la sua accessibilità, è nato per __rendere la navigazione tramite Tor semplice e immediata per tutti__.

I componenti aggiuntivi inclusi sono:

- __NoScript__ che permette di gestire l'esecuzione degli __script__ inclusi nelle pagine web.
- __HTTPS Everywhere__ che permette di forzare l'uso di __HTTPs__ per proteggersi dall'attacco __exit node monitoring__ trattato successivamente.

### Gestire il proprio servizio nascosto

Per gestire il proprio servizio web nascosto, è sufficiente __una macchina GNU/Linux connessa alla rete Tor__, anche se si trova dietro __firewall o altri sistemi__.

Configurando correttamente __Tor__, è possibile istruirlo a ridirezionare le connessioni in ingresso tramite la sua rete a una certa porta sul proprio dispositivo, creando un canale di comunicazione tra __Tor__ e il __servizio__.

Gestire un servizio anonimo però __non è semplice__ soprattutto per i __problemi di sicurezza__ tra cui:
- __correlation attack__ se un servizio è accessibile anche senza __Tor__
- errori di configurazione e informazioni inviate per sbaglio nei report di errore del server
- __analisi statistiche di uptime__ e confronto
- __errori umani__ vari tra cui informazioni chiave sulla segretezza incluse direttamente nel sito


