
## Come si usa

Per usare Bitcoin è necessario:

1. scaricare un client (erroneamente chiamato __wallet__ in molti casi), ovvero un'implementazione software del protocollo.
    - esistono client disponibili per ogni piattaforma comune, come android, iOS, Windows, OSX eccetera
1. usando il client:
    1. creare un __wallet__
    1. cominciare a effettuare transazioni

Da notare che _la maggior parte_ dei client, per funzionare, richiedono il download dell'intera __blockchain__ dalla rete, che al momento della scrittura di questo documento equivale a __33 GB__.

### Bitcoin Client

Ne esistono numerosi per molte piattaforme. Uno dei migliori, considerato più affidabile e utile è [Electrum](https://electrum.org).

#### Electrum

- supporta Windows, OSX, Linux e Android
- è __Open Source__ e dunque affidabile poichè gli sviluppatori non possono nascondere __backdoor__ o __vulnerabilità__ nel codice.
- permette di generare un __wallet__ usando __una passphrase__, in modo che se un wallet viene perso è possibile rigenerarlo usando la stessa frase.
- permette di __evitare di dover scaricare l'intera blockchain__ usando i server di Electron. Questa opzione apre una serie di possibili vulnerabilità non gravi, ma chi non si fida può semplicemente evitare di utilizzarla.
- offre un'interfaccia web che, tramite la __chiave pubblica__ del proprio __wallet__, permette di visualizzare i dati del proprio portafoglio ma non di compiere azioni.
- permette di utilizzare __portafogli hardware__, __multipli portafogli__ e __fondi condivisi__.
