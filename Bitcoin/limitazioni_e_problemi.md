# Vulnerabilità del protocollo

Fonte: [cryptocurrencymadesimple.com](http://cryptocurrencymadesimple.com/bitcoin-vulnerabilities/)

## Il problema del 50%+1

Se un'entità dovesse avere il controllo del 50% + 1 dei nodi della rete bitcoin sarebbe in grado di prendere decisioni sulla validità di ogni transazione il 50% + 1 delle volte, riuscendo ad avedere un'influenza troppo alta sulla rete.

Ma come visto nella sezione __incentivi e disincentivi__, non conviene ottenere il 50% + 1 del controllo sulla rete perchè il valore dei bitcoin crollerebbe, rendendo inutile l'attacco. Di conseguenza, tutte le volte che un gruppo arrivò vicino alla soglia pericolosa nel passato, la sua crescità fu fermata oppure il gruppo si divise per evitare la possibilità dell'attacco.

## "Transation Malleability" attack

Questo attacco è una forma di __Denial of Service (DoS)__ che consiste nell'inviare più volte la stessa transazione (con lo stesso mittente, destinatario e quantità) ma cambiando i meta dati allegati in modo che la rete debba spendere una quantità di tempo considerevole nel decidere quale delle transazioni è quella valida.

A un certo punto, con una grande quantità di transazioni clone inserite nella rete, il tempo impiegato per validare una transazione reale diventa troppo lungo, rendendo difficile muovere fondi e di conseguenza rendendo inutile la rete.

Ma sempre a causa degli __incentivi__ nel mantenere la rete funzionante, è difficile che qualcuno voglia far crollare il valore della moneta. Inoltre questo attacco richiede un'enorme quantità di potenza di calcolo a causa del __proof of work__ richiesto per ogni transazione.

## Vulnerabilità della crittografia asimmetrica

Il concetto di Bitcoin dipende interamente dalla crittografia asimmetrica, di conseguenza tutti i problemi di sicurezza legati ad essa e alla gestione delle __chiavi private__ sono applicabili al protocollo Bitcoin.

## Il furto del portafoglio

La maggior parte dei __client__ memorizza il portafoglio in un semplice file __wallet.dat__. Se qualcuno dovessere copiare questo file, potrebbe trasferire l'intera somma contenuta nel portafoglio in un'altro portafoglio!

Una possibile soluzione è, __tramite Electrum__, non memorizzare il portafoglio ma rigenerarlo ogni volta usando una __passphrase__ (portafoglio parametrico). Ovviamente, la __passphrase__ deve essere segreta e sicura!
