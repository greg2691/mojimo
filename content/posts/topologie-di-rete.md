+++
title = 'Topologie Di Rete'
date = 2024-05-13T20:36:31+02:00
draft = false
tags = ['network', 'topologie', 'star', 'point-to-point', 'mesh', 'bus', 'ring', 'hybrid']
categories = ['Network']
+++

Identifica o determina tutte le componentistiche che rendono queste connessioni possibili, così come i metodi di accesso ai mezzi di trasmissione. 

Con topologia ci riferisce alla disposizione tipica e alla connessione fisica o logica dei dispositivi in una rete. 

La connessione fisica riguarda esattamente i materiali fisici, come le componenti utilizzate per le connessioni. Parliamo quindi di cavi, router, swtiches, bridges, hub ecc. ecc. Anche la posizione dei nodi riguarda la connessione fisica. Per connessione logica invece ci riferiamo al modo in cui queste connessioni sono possibili, a come il segnale si muove attraverso la rete. 

**Possiamo racchiudere la topologia di rete in tre macro categorie:**

## 1 - Connessioni: 
1. Possono essere via cavo, come cavi coassiali, fibra ecc. ecc.
2. Possono essere wireless, come la rete cellulare, il satellite o appunto il wi-fi

## 2 - Nodi (network interface controller):
Sono i punti di connessione fra il mittende e il destinatario del segnale

## 3 - Classificazioni: 

Pensiamo alla topologia come ad una rappresentazione virtuale della rete. Non necessariamente questa disposizione rappresenta la realtà, per questo parliamo di connessioni fisica o logica. Prendiamo ad esempio la disposizione fisica dei computer all'interno di una stanza: possiamo disporli in cerchio ma questo non necessariamente significa che la topologia utilizzata è la ring topology (topologia ad anello). 

### Fra le classificazioni abbiamo: 

**1. Point-to-point:**
La point-to-point è la classificazione più semplice, l'host-a comunica con l'host-b con un cavo diretto fra i due. Si parla di una connessione dedicata fra questi due dispositivi e si parla letteralmente di un cavo diretto fra i due. Immagino ad esempio un cavo ethernet che collega due computer.

**2. Bus:**
Nella connessione bus tutti gli hosts sono connessi fra di loro con un solo mezzo di trasmissione (transmission medium) che può essere ad esempio un cavo coassiale. Non esiste un componente di rete centrale che controlla il processo. Essendo il mezzo di trasmissione condiviso con tutti gli altri host solamente uno di loro può inviare il segnale, tutti gli altri potranno solo riceverlo. 

**3. Star:** 
Nella topologia star abbiamo un componente di rete centrale che può essere un router o uno switch che gestisce il traffico dei pacchetti di rete. Tutti gli hosts sono collegati a lui tramite connessioni singoli, uniche, private, separate, monogami ;) . Data la natura centrale del componente di rete il traffico su di lui può essere molto elevato. 

**4. Ring:** 
Nella topologia ad anello (ring) possiamo parlare dei due tipi di connessione, fisica e logica. 
Nella topologia fisica ogni host è collegato all'anello attraverso due cavi: uno per il segnale in entrata ed uno per il segnale in uscita. In questa topologia non abbiamo bisogno di componenti di rete attivi, come possono essere: switch, bridge, hub. Queste componenti rafforzano il segnale di rete facendo in modo che nel loro tragitto non perdano qualità o potenza. L'accesso ed il controllo al mezzo di comunicazione sono regolate in questo caso da un protocollo a cui tutti gli host aderiscono. 
Nella topologia logica invece quella che viene applicazione fisicamente è la topologia a stella. Dove un componente di rete centrale simula l'anello inoltrando il segnale da una porta all'altra. 

Nella topologia ad anello il segnale è spesso distribuito in una direzione predeterminata, che può essere a senso orario o anti-orario. Solitamente il segnale passa attraverso il media di comunicazione passando da host in host (stazione a stazione) utilizzando un sistema di recupero dalla stazione centrale o un token. Un token è un modello di bit che passa continuamente nell'anello seguendo una direzione che funziona secondo il processo di rivendicazione del token. 

**5. Mesh:** 
Nella topologia mesh ci sono svariati nodi che decidono riguardo le connessioni sul livello fisico e il routing sul livello logico. Possiamo però dividerla in due sotto categorie: 
1. Fully meshed: In questa topologia ogni singolo host è collegato ad un altro. Questa è una configurazione tipica delle reti WAN e MAN poichè conferisce una maggiore stabilità e ampiezza di banda. In questa topologia anche mezzi di rete importanti come i router sono collegati fra di loro, con il vantaggio che se uno di questi router si guasta è possibile utilizzare gli altri, poiché ogni nodo in questa configurazione ha gli stessi settaggi di routing e la stessa conoscenza dei nodi vicini. 
2. Partially Meshed: in questo caso gli endpoint o host sono collegati attraverso una sola connessione.

**6. Tree**: 
La topologia tree è una variante estesa della topologia star ed è solitamente utilizzata da reti estese e se vogliamo dirlo più "complesse". È solitamente utile quando vogliamo applicare più topologie diverse ed è spesso usata in aziende molto grandi. Ne esistono sia fisiche che logiche. Sono spesso usate anche per tipi di rete a banda larga e reti cittadine MAN. 


**7. Hybrid (topologia ibrida che utilizza 2 o più classificazioni di cui sopra)**: 
In questa topologia si utilizzano diverse topologie di rete, ad esempio quando connettiamo una topologia tree ad una star. Dobbiamo però avere le due topologie base diverse, nel caso in cui connettiamo due topologie tree o due star si avranno comunque o una topologia star o una tree. 


**8. Daisy chain**: 
In questa topologia gli host sono collegati in serie fra di loro attraverso una connessione fisica dei nodi. In questo caso il segnale è inviato attraverso il nodo precedende. È l'unica topologia fisica che rispecchia la topologia logica. 

Per il momento questo è quanto sulle topologie di rete.


