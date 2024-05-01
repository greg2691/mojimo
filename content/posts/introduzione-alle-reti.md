+++
title = 'Introduzione Alle Reti'
date = 2024-05-01T21:23:19+02:00
draft = false
tags = ['red']
categories = ['Network']
+++

Oh bro!! La rete è un sistema (semplice?) reso dannatamente complesso che consente a due dispositivi di comunicare fra loro. 
Questo è semplice, un computer comunica con un altro computer (in questo caso chiamato server) attraverso una rete. In realtà quel computer potrebbe essere addirittura attaccato con un cavo all'altro computer (il server) e comunicare in questo modo MA! C'è un enorme ma ed è qui che subentra il concetto di rete bello complesso che "conosciamo"... 







Supponiamo quindi, utilizzando una metafora che possa spiegare la logica, che io voglia inviare un pacco pieno di cacca ad una persona che mi sta antipatica. Di questa persona però conosco solo il nome. Andrò al mio ufficio postale locale e affiderò loro il mio pacco dicendo di spedirlo a Bob Smith. L'ufficio postale prenderà il pacco e con questo il mio nome e indirizzo e lo invierà all'hub postale principale, questo hub si preoccuperà di cercare l'indirizzo di Bob Smith nella sua enorme agenta e invierà il pacchetto a Bob Smith. 

Bob Smith felice di aver ricevuto la cacca che tanto aspettava da me decide di inviarmi una letterina di ringraziamento, così... per rinoscenza!!

Porterà la letterina al suo ufficio postale locale (il mio nome e il mio indirizzo sono informazioni ricevuto con il pacco), il suo ufficio postale invierà la letterina all'hub principale che a sua volta lo invierà al mio ufficio postale locale che a sua volta ancora mi porterà la letterina a casa.

Quello che è appena avvenuto è uno scambio fra due persone. Supponiamo però che queste due persone siano computer, o iPhone o la merda che più preferite. 

Supponiamo che io devo collegarmi su amazon.it per fare shopping: 

Il mio computer (identificato da un indirizzo IP) una volta premuto invio nel browser dopo aver digitato amazon.it invierà un pacchetto (sì sono pacchetti anche questi) contenente la mia richiesta al mio router (che sarebbe l'ufficio postale locale) il router (tramite complesse traduzioni dell'indirizzo IP locale a non-locale) invierà il pacchetto all'ISP (l'hub postale principale). 

L'ISP controllerà il DNS (il grande librone degli indirizzi) dove è contenuto l'indirizzo IP di amazon.it, una volta trovato invierà il pacchetto al suo server (quello di amazon.it).

Una volta ricevuta la richiesta dal server amazon.it lui mi rimanderà la sua home page (o qualsiasi pagina specifica richiesta) al mio indirizzo IP, quello contenuto nel pacchetto che ho inviato io insieme alla richiesta,  comunicando con il suo router e a sua volta con l'ISP, ripassando per il mio router e arrivando fresco fresco al mio browser. 

Essenzialmente è così che funziona una rete. 

Ovviamente i processi sono resi veramente MOOOLTO semplici in questo esempio, non è stato specificato come queste comunicazioni sono possibili, non sono specificati gli strumenti e i protocolli con cui avvengono. 

Ci sono tanti sotto-aspetti tecnici che non abbiamo nominato e abbiamo semplicemente visto quella che è la logica dietro la comunicazione di rete. Che poi, dopo tutto, questo è... andare da un punto A ad un punto B e vice versa. 

See you next time bro!!

