## Bloccare l'accesso a Tor

Un ente potrebbe voler bloccare l'accesso alla rete Tor all'interno della propria infrastruttura per ovvie ragioni di sicurezza. Il miglior metodo è bloccare completamente il traffico destinato __agli indirizzi IP che corrispondo ai nodi Tor pubblici__, bloccando effettivamente l'accesso poichè il software ha bisogno di connettersi ad almeno un nodo direttamente per avere l'accesso alla rete.

Un limite di questo tipo è però facilmente aggirabile tramite l'utilizzo di __bridge node (bridge relay)__, ovvero dei __nodi Tor non pubblici__. __Tor è software libero__, di conseguenza __chiunque può aprire un proprio (bridge) relay__ e __accedere alla rete da luoghi che bloccano i nodi pubblici attraverso di esso__.

Purtroppo __non è possibile bloccare completamente l'accesso a Tor senza applicare enormi, irrealistiche restrizioni all'accesso a internet__.