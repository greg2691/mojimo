+++
title = 'Proxy'
date = 2024-05-15T15:36:11+02:00
draft = false
tags = ['network', 'proxy', 'forward proxy', 'reverse proxy', 'transparent proxy']
categories = ['Network']
+++

Proxy

Il proxy è essenzialmente un mediatore nella connessione, si siede li nel mezzo fra noi e la nostra destinazione MA in quanto mediatore deve essere in grado di poter ispezionare il contenuto del traffico, altrimenti staremmo parlando di un gateway. 

## Esistono principalmente tre tipologie di proxy: 

**1. Dedicated Proxy / Forward Proxy:** 
filtra le richieste in uscita. Questo  è quanto. Non è vero... diciamo che il Forward (o dedicated) Proxy è un filtro fra noi e la meta che vogliamo raggiungere. Facciamo un esempio: come sempre siamo in una grande azienda e ci sono dei computer sensibili magari utilizzati con molta probabilità da dei completi imbecilli. Questi computer quindi non possono connettersi direttamente ad internet, devono usare delle protezioni :wink: , questa protezione è il Forward Proxy, la nostra connessione sarà quindi filtrata dal Proxy. È particolarmente utile nel non prendere malware... Solamente io qui vedo delle analogie potentissime con il preservativo? :joy: Tornando a noi, generalmente un malware potrebbe bypassare il filtro web senza troppi problemi ma potrebbe difficilmente bypassare un proxy in quanto ne dovrebbe essere a conoscenza, per così dire dovrebbe essere "proxy aware" o utilizzare una C2 non tradizionale (sarebbe un modo per i malware di ricevere compiti o task). In questo caso possiamo fare due differenze: 

1. Firefox: se l'azienda utilizza solamente il proxy di Firefox le probabilità di beccarsi un malware proxy-aware sono veramente basse, in quanto firefox utilizza librerie libcurls ed è configurabile a prescindere dal sistema operativo su cui risiede. Detto in altre parole il suo codice è configurabile e indipendente dal sistema operativo.
2. Altri browser: diverso nel caso in cui si usano browser come Chrome, Edger, Internet Explorer (chi lo usa ancora 'sto qua?). Questi browser rispondono esclusivamente al proxy di sistema e nel caso in cui il malware utilizza WinSock (API di windows native) le probabilità che sia proxy aware sono molto alte senza utilizzare codice aggiuntivo come C2.

Come abbiamo avuto modo quindi di vedere, nel primo caso il malware dovrebbe essere in grado di ricevere le informazioni di Firefox, cosa che un malware non è quasi mai in grado di fare. 

Ci sarebbe un modo per i malware di aggirare questo ed è con l'utilizzo dei DNS come meccanismo di C2, ma se l'organizzazione monitora i DNS questo tipo di traffico è facilmente identificabile. 

**2. Reverse Proxy:**
indovinate? Esatto!! Filtra le richieste in entrata. Principalmente ascolta il traffico in entratata e lo devia ad una rete vicina. Questo è importante: ascolta le richieste su un particolare indirizzo e le veicola ad una rete vicina. Quanti ipotetici scenari siete riusciti ad immaginare? 

Conoscete CloudFare? CloudFare ha delle ottime reti che possono restitere ad attacchi DDoS importanti, grazie all'utilizzo di CloudFare ad esempio possiamo controllare la quantità e il tipo di traffico indirizzati al nostro server web. Come possiamo dedurre questo è utile, ma supponiamo questo scenario: in qualità di pentster configuriamo dei rever proxy su un endpoint infetto (un endpoint è un dispositivo come un computer o uno smartphone che comunica con un server), questo endpoint viene impostato in ascolto su una determinata porta e tutte le richieste che arrivano dai client su quella determinata porta vengono veicolati alla nostra porta. In questo caso utilizziamo l'endpoint come "veicolatore" di richieste. Questo ci consente di aggirare ad esempio i firewall o eludere i sistemi di registrazione. È possibile difenderci da questo tipo di attacco con l'utilizzo di un IDS (Intrusion Detection System) il quale controlla le richieste web esterne ma nel caso in cui otteniamo l'accesso tramite tunnel SSH possiamo veicolare le richieste li ed eludere così l'IDS.

Esiste in fine un altro comune Rever Proxy chiamato ModSecurity, che sarebbe in pratica un WAF (Web Application Firewall). Un WAF ispezione le richieste web in ricerca di contenuti dannosi e blocca la richieste se dannose. Anche CloudFare può comportarsi come un WAF ma bisognerebbe impostarlo affinché decripti il traffico HTTSP cosa che non molte organizzazioni vogliono per loro stesse.  

**3. Transparent Proxy:** 
Tutte queste tipologie di proxy possono essere eseguite (o "comportarsi") in modo trasparente o in modo non trasparente. 

1. Transparent proxy: in questo caso il cliente non è conoscenza dell'esistenza del proxy e quest'ultimo intercetta le richieste di comunicazione del cliente verso internet e si comporta come istanza sostitutiva, cioè si sostituisce al client. Dall'esterno sia il proxy trasparente che quello non trasparente si comportano come partner di comunicazione. 

2. Non-transparent Proxy: in questo caso siamo a conoscenza del proxy e con quest'ultimo andrà utilizzata una configurazione speciale che ci assicura che il traffico verso internet sia indirizzato prima al proxy. Senza questa comunicazione non possiamo comunicare con il proxy ed essendo in questo caso il proxy l'unico "veicolatore" o percorso di comunicazione verso le altre reti non possiamo comunicare efficacemente, questo, in altre parole, significa che non potremmo connetterci alla rete. 

Questo è quanto per il momento sui proxy. See you next time bro!!!

