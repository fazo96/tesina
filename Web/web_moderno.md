## Dalle origini al Web 2.0

Quando __Internet__ è stato creato, il protocollo __HTTP__ (utilizzato per visitare le pagine web) è stato pensato per trasferire dei semplici __ipertesti__ (da qui il nome _Hyper Text Transfer Protocol_) arricchiti tramite fogli di stile __CSS__ (_Cascading Style Sheet_). Successivamente, durante l'enorme, rapida evoluzione della rete, il protocollo ha implementato la possibilità di inviare qualsiasi tipo di file.

Contemporaneamente, i browser si solo evoluti per permettere l'esecuzione di __script__ (piccoli programmi) inviati insieme agli ipertesti, __rendendo possibile trasformare una pagina web da un semplice documento a un vero e proprio programma applicativo.__

Anche se l'accesso ai dati del dispositivo da parte degli script è molto limitato, __un sito web è in grado di allegare uno o più script insieme all'ipertesto, i quali vengono eseguiti immediatamente alla loro ricezione dal browser dell'utente__.

Questi script possono comunicare ai server remoti numerosi dati riguardo la visita al sito, in particolare:

- i click che sono stati fatti
- le sezioni che sono (probabilmente) state lette
- le pagine che sono state visitate e per quanto tempo
- le righe che sono state copiate
- indirizzo IP, browser usato e sistema operativo con relative versioni

Con l'importanza crescente di un metodo per inviare dati importanti con sicurezza, il protocollo __SSL__ (successivamente __TLS__) è stato creato, e con esso lo standard __HTTPs__ che permette di utilizzare __HTTP__ in maniera sicura incapsulando il traffico all'interno di pacchetti __SSL__.

Grazie ad __HTTPs__ è possibile garantire la _privatezza_, l'_integrità_ e l'_affidabilità_ delle informazioni durante una comunicazione con un server.

## Persistenza

Gli script possono istruire i browser web a salvare delle informazioni o, se presenti, spedirle al server permettendogli di __riconoscere l'utente anche durante le prossime visite__ con una procedura molto semplice.

Queste informazioni sono dette __cookie__. Vediamo ora come funzionano:

- il server richiede al client il cookie che gli ha rilasciato precedentemente
- __se il client non ha un cookie__, allora è la sua prima visita e gli viene assegnato un nuovo cookie:
    - il server memorizza l'associazione __cookie-utente__ nel proprio database (o nella propria memoria);
    - i cookie possono essere __temporanei__ (si cancellano alla chiusura del browser) o __permanenti__ (si cancellano dopo un certo tempo o mai);
- __se il client ha un cookie__, allora il server può usarlo per riconoscerlo confrontandolo con le associazioni __cookie-utente__ memorizzate;

Queste caratteristiche evidenziano chiaramente dei problemi di sicurezza, ad esempio se un attaccante riuscisse a __copiare un cookie valido da un dispositivo altrui__ potrebbe __utilizzare liberamente l'account della vittima__.

Grazie alla persistenza, i server dietro ai più visitati siti web possono profilare gli utenti, analizzando il loro comportamento.

La collaborazione tra i diversi colossi del web tra cui __Facebook, Google, Microsoft eccetera__ e la loro __integrazione con la maggior parte dei siti web__ consente a loro di __tracciare ogni attività online di ogni utente che utilizza questi servizi__.

## Perchè?

Ci sono numerosi motivi per questa raccolta dati:

- __Pubblicità mirate:__ Google inserisce le pubblicità sulle pagine web in base agli interessi dell'utente che andrà a visualizzarle, in modo da ottenere più click e di conseguenza più guadagni;
- __Vendita dei dati:__ i social network possono vendere dati riguardo, ad esempio, l'interesse degli utenti verso un prodotto piuttosto che un altro;
- __Studio del mercato:__ analizzando le mode e le discussioni sociali è possibile in certi casi prevedere svolte nel mercato di certe categorie o brand di prodotti;
- __Correlazioni tra soggetti apparentemente indipendenti:__ combinando i profili dello stesso utente su servizi diversi, è possibile ottenere una visione completa dei suoi interessi e, confrontando una grande quantità di profili, dei modelli da utilizzare per prevedere i probabili interessi di una persona.

## Opinione pubblica: privacy e controversie

Questa raccolta dati diventa problematica quando gli utenti __si rendono conto__ che le loro __conversazioni private__ tenute tramite Facebook, Twitter, WhatsApp e altri servizi __non sono effettivamente private.__

Soprattutto dopo __le scandalose rivelazioni di Edward Snowden riguardo le attività della NSA Statunitense__, in particolare la sorveglianza totale dei sistemi di comunicazione senza permesso, molti utenti __hanno deciso di rivolgersi ad alternative sicure dei servizi che utilizzavano regolarmente__ poichè se l'NSA è in grado di _sorvegliare l'attività degli utenti su servizi pubblici_ con ma anche senza _permesso dei loro gestori_, allora qualunque esperto con le risorse necessarie potrebbe farlo.

Una semplice ricerca sul Web riguardo a tutto ciò porta a scoprire l'esistenza di _numerose soluzioni_ per ridurre questa continua propagazione di dati dai nostri browser alle terze parti con cui ci interfacciamo e le pubblicità mirate che vediamo.

Alcune comuni soluzioni sono:

- __Ghostery__ e __disconnect.me__ per evitare di immagazzinare __cookie__; inutili per noi ma utili per le corporazioni che tracciano le nostre attività
- __AdBlock__ per eliminare o ridurre le pubblicità.

__Attenzione:__ _AdBlock_ è un software __Closed Source__, dunque non è possibile sapere esattamente che tipo di operazioni esegua sul proprio dispostivo. E' molto consigliata l'alternativa __uBlock__, che è un _Software Libero_ e _Open Source_.

### Il problema di Google

Google è uno dei servizi che raccoglie il maggior numero di dati dai propri utenti. Esistono delle alternative non invasive, ad esempio:

- il motore di ricerca __DuckDuckGo__ per evitare l'immensa quantità di dati recuperati da Google ad ogni nostra mossa con il suo motore di ricerca
- __OpenStreetMap__ al posto di __Google Maps__;
- le soluzioni illustrate nel capitolo __"Condividere File Con Sicurezza"__ al posto di Google Drive;
- un mail server gestito personalmente in accoppiata con un client mail sicuro al posto di GMail.

Purtroppo, spesso la comodità e qualità dei servizi di Google va ben oltre quella delle sue alternative.
