# Messaggistica: problemi e soluzioni

## Il problema delle E-Mail

Il concetto di __E-Mail__ (posta elettronica) è una delle prime applicazioni pratiche di __Internet__ e delle reti di calcolatori in generale. Si basa su protcolli standard, in particolare:

- __SMTP__ (Simple Mail Transfer Protocol) per l'invio della posta.
- __POP3__ e __IMAP__ per la ricezione e la lettura della posta contenuta in una __casella di posta elettronica__.

Le E-Mail sono però distribuite __in chiaro__, senza __crittografia o firme digitali__, usando __server centralizzati__. Queste caratteristiche rendono le email un sistema __poco sicuro__, __tracciabile__ e __vulnerabile__ soprattutto perchè:

- ogni messaggio intercettato è _leggibile_ e _alterabile_
- il sistema è vulnerabile a moltissime tipologie di attacchi
- mittenti e destinatari sono difficilmente identificabili a causa della mancanza di __firme digitali__

Questi problemi sono _parzialmente_ risolti usando i protocolli __GPG__ e __S/MIME__ rispettivamente per gestire l'aspetto di _firma_ e _crittografia_ e per integrarlo nelle __E-Mail__ insieme ad _allegati_, _immagini_ e altri documenti multimediali.

Anche lo _spam_ può essere limitato usando dei filtri anti-spam particolari nel proprio client di posta, resta però il problema che __i messaggi di spam sono scaricati comunque__ rallentando pesantemente la rete.

### Soluzioni

Bitmessage è un esempio di servizio _libero_, _sicuro_, _anonimo_ e _decentralizzato_ descritto nella sezione dedicata.

## Il problema della messaggistica istantanea e del VoIP

La messaggistica istantanea (spesso arracchita con __VoIP__ (telefonate via Internet) come nel caso di __Skype__ e __WhatsApp__) presenta numerosi problemi, tra cui:

- profonda centralizzazione
- mancanza di crittografia __end-to-end__ ovvero dal mittente al destinatario, che causa:
    - possibilità dei _server centralizzati_ di origliare ogni conversazione e alterare messaggi
    - la divulgazione di tutte le conversazioni degli utenti (in caso i _server centralizzati_ vengano compromessi)

### Soluzioni

Risolvere questo problema è molto difficile, poichè un sistema di messaggistica _decentralizzata_ che supporti il __VoIP__ è molto difficile da realizzare. Attualmente in svilppo esistono __TorChat__ e __Tox__.
