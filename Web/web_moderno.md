## Dalle origini al Web 2.0

Quando __Internet__ è stato creato, il protocollo __HTTP__ (utilizzato per visitare le pagine web) è stato pensato per trasferire dei semplici __ipertesti__ (da qui il nome _Hyper Text Transfer Protocol_) arricchiti tramite fogli di stile __CSS__ (_Cascading Style Sheet_) ma con l'enorme, rapida evoluzione della rete, il protocollo ha implementato la possibilità di inviare qualsiasi tipo di file.

Contemporaneamente, i browser si solo evoluti per permettere l'esecuzione di __script__ inviati insieme agli ipertesti, __rendendo possibile trasformare una pagina web da un semplice ipertesto a un vero e proprio programma.__

Anche se l'accesso ai dati del dispositivo da parte degli script è molto limitato, __un sito web è in grado di allegare uno o più script insieme all'ipertesto, i quali vengono eseguiti immediatamente alla loro ricezione__.

Questi script possono comunicare ai server remoti numerosi dati riguardo la visita al sito, in particolare:

- i click che sono stati fatti
- le sezioni che sono (probabilmente) state lette
- le pagine che sono state visitate e per quanto tempo
- le righe che sono state copiate
- indirizzo IP, browser usato e sistema operativo con relative versioni

Con l'importanza crescente di un metodo per inviare dati importanti con sicurezza, il protocollo __SSL__ (successivamente sostituito da __TLS__) è stato creato, e con esso lo standard __HTTPs__ che permette di utilizzare __HTTP__ in maniera sicura incapsulando il traffico all'interno di pacchetti __SSL__.

## Persistenza

Gli script possono istruire i browser web a salvare delle informazioni o, se presenti, spedirle al server (__cookie__) permettendogli di __riconoscere l'utente anche durante le prossime visite__ con una procedura molto semplice:

1. il server richiede al client il cookie che gli è stato rilasciato precedentemente dallo stesso server
1. __se il client non ha un cookie__, allora non può essere riconosciuto dal server (per ora) e gli viene assegnato un nuovo cookie
    - il server memorizza l'associazione __cookie-utente__ nel proprio database (o nella propria memoria)
    - i cookie possono essere __temporanei__ (si cancellano alla chiusura del browser) o __permanenti__ (si cancellano dopo un certo tempo o mai)
1. __se il client ha un cookie__, allora il server può usarlo per riconoscerlo confrontandolo con le associazioni __cookie-utente__ memorizzate

Grazie alla persistenza, i server dietro ai più visitati siti web possono profilare gli utenti, analizzando il loro comportamento.

La collaborazione tra i diversi colossi del web tra cui __Facebook, Google, Microsoft eccetera__ e la loro __integrazione con la maggior parte dei siti web__ consente a loro di __tracciare ogni attività online di ogni utente che utilizza questi servizi__.

## Perchè?

Ci sono numerosi motivi per questa raccolta dati:

- __Pubblicità mirate:__ Google inserisce le pubblicità sulle pagine web in base agli interessi dell'utente che andrà a visualizzarle, in modo da ottenere più click e di conseguenza più guadagni
- __Vendita dei dati:__ i colossi possono vendere dati riguardo, ad esempio, l'interesse degli utenti verso un prodotto piuttosto che un altro
- __Studio del mercato:__ analizzando le mode e le discussioni sociali è possibile in certi casi prevedere svolte nel mercato di certe categorie o brand di prodotti
- __Correlazioni tra soggetti apparentemente indipendenti__, ad esempio si può scoprire che un utente di Facebook è interessato anche a prodotti Apple e creare correlazioni

## Opinione pubblica: privacy e controversie

Questa raccolta dati diventa problematica quando gli utenti __si rendono conto__ che le loro __conversazioni private__ effettuate tramite Facebook, Twitter, WhatsApp, eccetera __non sono effettivamente private.__

Soprattutto dopo __le scandalose rivelazioni di Edward Snowden riguardo le attività della NSA Statunitense__ molti utenti __hanno deciso di rivolgersi ad alternative sicure dei servizi che utilizzavano regolarmente.__

Una semplice ricerca sul Web riguardo a tutto ciò porta a scoprire l'esistenza di numerose soluzioni per ridurre questa continua fornitura di dati dai nostri browser ai proprietari dei servizi che usiamo e le pubblicità mirate che vediamo come:

- __Ghostery__ e __disconnect.me__ per evitare di immagazzinare __cookie__ inutili per noi ma utili per le corporazioni che tracciano le nostre attività
- __AdBlock__ per eliminare o ridurre le pubblicità

__Attenzione:__ _AdBlock_ è un software __Closed Source__, dunque non è possibile sapere esattamente che tipo di operazioni esegua sul proprio dispostivo. E' molto consigliata l'alternativa __uBlock__, che è un _Software Libero_ e _Open Source_.

### Il problema di Google

Google è uno dei servizi che raccoglie il maggior numero di dati dai propri utenti. Volendone approfittare, esistono dei servizi che si offrono come alternativa non invasiva, ad esempio:

- il motore di ricerca __DuckDuckGo__ per evitare l'immensa quantità di dati recuperati da Google ad ogni nostra mossa con il suo motore di ricerca
- __OpenStreetMap__ al posto di __Google Maps__
- le soluzioni illustrate nel capitolo __"Condividere File Con Sicurezza"__ al posto di Google Drive
- un mail server gestito personalmente in accoppiata con un client mail sicuro al posto di GMail