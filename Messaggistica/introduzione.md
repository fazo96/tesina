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

Risolvere questo problema è molto difficile, poichè un sistema di messaggistica _decentralizzata_ che supporti il __VoIP__ è molto difficile da realizzare. Attualmente in svilppo esistono __Ricochet__ e __Tox__, mentre un'alternativa matura ma non più in evoluzione è __TorChat__.

### TorChat

TorChat è un servizio di messaggistica anonima nato nel 2007 e non più sviluppato attivamente che offre _decentralizzazione_ e _totale anonimato_ appoggiandosi alla rete __Tor__.

Il software è distribuito online

### Ricochet

[Ricochet.im](http://ricochet.im) è un _Software Libero_ sviluppato dal gruppo [Invisible.im](http://invisible.im). Si basa sui __Tor Hidden Services__, offre _anonimato_ e _decentralizzazione_ ed è pensato per essere __facilmente utilizzabile__ anche da utenti non esperti, anche se si trova ancora in stato sperimentale.

### Tox

[Tox.im](http://tox.im) è il nome dato a un protocollo e la sua implementazione _Open Source_ (chiamata __libtoxcore__) che permettono la comunicazione _sicura_, _anonima_ e _privata_ usando una rete decentralizzata. __Tox__ in se è una _libreria_ e non un programma direzionato agli _utenti finali_: per essi esistono i cosiddetti __Tox Client__, realizzati per diverse piattaforme tra cui __Windows__, __Linux__, __OSX__ e __Android__. Tutti i __Tox Client__ popolari sono _Open Source_.

__Tox__ è ancora in stato sperimentale, e solo di recente alcuni client hanno iniziato a supportare le __telefonate e videochiamate__. Inoltre, anche i __Tox Client__ più avanzati sono ancora __complessi e inaccessibili__ soprattutto per gli utenti meno esperti.

Nonostante ciò, lo sviluppo di __Tox__ è in piena attività e i client sono in continuo miglioramento.
