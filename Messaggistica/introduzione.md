# E-Mail

Il concetto di __E-Mail__ (posta elettronica) è una delle prime applicazioni pratiche di __Internet__ e delle reti di calcolatori in generale. Si basa su protcolli standard, in particolare:

- __SMTP__ (Simple Mail Transfer Protocol) per l'invio della posta.
- __POP3__ e __IMAP__ per la ricezione e la lettura della posta contenuta in una __casella di posta elettronica__.

## Problemi

Le E-Mail sono però distribuite __in chiaro__, senza __crittografia o firme digitali__, usando __server centralizzati__. Queste caratteristiche rendono le email un sistema __poco sicuro__, __tracciabile__ e __vulnerabile__ soprattutto perchè:

- ogni messaggio intercettato è _leggibile_ e _alterabile_
- il sistema è vulnerabile a moltissime tipologie di attacchi
- mittenti e destinatari sono difficilmente identificabili a causa della mancanza di __firme digitali__

Questi problemi sono _parzialmente_ risolti usando i protocolli __GPG__ e __S/MIME__ rispettivamente per gestire l'aspetto di _firma_ e _crittografia_ e per integrarlo nelle __E-Mail__ insieme ad _allegati_, _immagini_ e altri documenti multimediali.

Anche lo _spam_ può essere limitato usando dei filtri anti-spam particolari nel proprio client di posta, resta però il problema che __i messaggi di spam sono scaricati comunque__ rallentando pesantemente la rete.

## Soluzioni

Bitmessage è un esempio di servizio _libero_, _sicuro_, _anonimo_ e _decentralizzato_. che risolve la maggior parte dei problemi descritti, illustrato nella sezione dedicata.

# Messaggistica istantanea e VoIP

La messaggistica istantanea (spesso arracchita con __VoIP__ (telefonate via Internet) come nel caso di __Skype__ e __WhatsApp__) presenta numerosi problemi, tra cui:

- profonda centralizzazione
- mancanza di crittografia __end-to-end__, ovvero dal mittente al destinatario, che causa:
    - possibilità dei _server centralizzati_ di origliare ogni conversazione e alterare messaggi
    - la divulgazione di tutte le conversazioni degli utenti (in caso i _server centralizzati_ vengano compromessi)

## Soluzioni

Risolvere questo problema è quasi impossibile, poichè a causa delle caratteristiche richieste, un sistema di messaggistica _decentralizzata_ che supporti il __VoIP__ è molto difficile da realizzare.

__Perchè?__

Innanzi tutto, un sistema di messaggistica istantanea richiede che il destinatario riceva sempre i messaggi a lui inviati e nel caso sia offline i __server__ mantengono i messaggi in memoria in modo da inviarli appena il destinatario si __collega__. Inoltre, i __server__ fungono da _ponte_ per l'invio dei messaggi in modo che sia sempre possibile il trasferimento, infatti __una connessione diretta tra interlocutori presenta una serie di problemi__, tra cui:

- ogni interlocutore deve conoscere l'indirizzo __IP__ di almeno uno dei coinvolti nella conversazione: questo può essere risolto usando un __DHT__ e/o uno o più __tracker__, come fanno gli altri servizi decentralizzati, ad esempio __BitTorrent__ usa entrambe le soluzioni per massimizzare i guadagni.
- se due utenti si trovano entrambi dietro un __NAT__ diverso, si verifica la situazione molto comune chiamata __NAT simmetrico__ che rende quasi impossibile la connessione diretta tra i due. Questo è risolvibile creando una connessione __indiretta__ tra gli interlocutori, passando per altri nodi, oppure incaricando altri nodi di consegnare i messaggi in maniera simile alla soluzione di __Bitmessage__.
- difficoltà di immagazzinare i __metadati__ come, nel caso di conversazione di gruppo, il nome del gruppo o la storia di messaggi o il profilo degli utenti, perchè la mancanza di __server centrali__ rende potenzialmente __inaffidabile__ ogni utente. Questo può essere risolto creando un sistema di metadati distribuito simile alla soluzione di __Freenet__, usando firme digitali e crittografia per definire i permessi di modifica.
- impossibilità di scambiare messaggi se due utenti __non sono online contemporaneamente__. Questo può essere risolto mantenendo una __cache distribuita__ e/o mantenendo in circolo i messaggi nella rete, in maniera simile alla soluzione di BitMessage.

Questi problemi sono quasi tutti risolvibili in qualche modo, ma con enorme difficoltà. Attualmente in svilppo esistono alcuni servizi di messaggistica e/o __VoIP__ sperimentali tra cui __Ricochet__ e __Tox__, mentre un'alternativa matura ma non più in evoluzione è __TorChat__.

### TorChat

TorChat è un servizio di messaggistica anonima nato nel 2007 e non più sviluppato attivamente che offre _decentralizzazione_ e _totale anonimato_ appoggiandosi alla rete __Tor__.

### Ricochet

[Ricochet.im](http://ricochet.im) è un _Software Libero_ sviluppato dal gruppo [Invisible.im](http://invisible.im). Si basa sui __Tor Hidden Services__, offre _anonimato_ e _decentralizzazione_ ed è pensato per essere __facilmente utilizzabile__ anche da utenti non esperti, anche se si trova ancora in stato sperimentale.

### Tox

[Tox.im](http://tox.im) è il nome dato a un protocollo e la sua implementazione _Open Source_ (chiamata __libtoxcore__) che permettono la comunicazione _sicura_, _anonima_ e _privata_ usando una rete decentralizzata. __Tox__ in se è una _libreria_ e non un programma direzionato agli _utenti finali_: per essi esistono i cosiddetti __Tox Client__, realizzati per diverse piattaforme tra cui __Windows__, __Linux__, __OSX__ e __Android__. Tutti i __Tox Client__ popolari sono _Open Source_.

__Tox__ è ancora in stato sperimentale, e solo di recente alcuni client hanno iniziato a supportare le __telefonate e videochiamate__. Inoltre, anche i __Tox Client__ più avanzati sono ancora __complessi e inaccessibili__ soprattutto per gli utenti meno esperti.

Nonostante ciò, lo sviluppo di __Tox__ è in piena attività e i client sono in continuo miglioramento.
