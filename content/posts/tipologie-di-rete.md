+++
title = 'Tipi di rete'
date = 2024-05-02T17:23:19+02:00
draft = false
tags = ['network', 'tipi']
categories = ['Network']
+++


Ciao bro!! Per complicarci ulteriormente l'esistenza queste reti possono essere coinfigurate in vari modi. Per questo motivo abbiamo diverse topologie e diversi tipi di rete. 

Fra i tipi di rete ci sono due, diciamo così, macro categorie:

1. Terminologie comuni
1. Terminologie di riferimento

### Fra le terminologie comuni abbiamo:

1. **La WAN: Wide Area Network**, conosciuta come "L'INTERNET". Non è nient'altro che un insieme di reti LAN collegate fra loro. Spesso possiamo vedere delle grandi aziende avere un sistema di Intranet, che sarebbe un "INTERNET" interno accessibile solo dai computer e dalla rete aziendali.

2. **La LAN: Local Area Network**, praticamente la rete di casa tua o del tuo ufficio.

3. **La WLAN,** essenzialmente come sopra ma attraverso la wireless

4. **la VPN: Virtual Private Network**, esattamente quella che branchi di youtuber sponsirizzano, sono, in parole povere, diverse reti collegate ad una LAN. Ma anche qui la faccenda è un attimino più complessa di quello che sembra, perché ne esistono bene tre diversi tipi! Sì o mio dio! TRE, DIVERSI, TIPI: 

1. **Site-To-Site VPN:** in questo caso sia il client che il server sono dei dispositivi di rete, come ad esempio un router e un firewall. Viene utilizzate per unire diverse reti aziendali attraverso Internet, questo consente ai dispositivi sparsi in diversi luoghi di comunicare via Internet come se stessero tutti nello stesso luogo... 

2. **Remote Access VPN:** poniamo caso la vostra azienda ha una sua intranet localizzata su un server aziendale, installato proprio li, nell'ufficio accanto al tuo. Poniamo caso sempre che in questa intranet c'è tutto il meglio del porno reperibile in rete (quell'altra retew ;) ), facciamo che tu sei a casa che lavori da remoto e nella tua pausa pranzo vorresti usufruire di quel bellissimo materiale... ma è nell'intranet... come puoi fare?!?!?!! Installando un software, ad esempio OpenVPN che ti consente di connetterti alla rete interna aziendale e comportarti come se ti trovassi fisicamente li. Ovviamente anche qui abbiamo delle particolarità che devono necessariamente rovinarci la vita, come ad esempio la split-tunnel VPN: in pratica quando ci connettiamo con il Remote Access VPN, non è altro che una connessione Tunnel Criptata fra noi, che siamo il client e loro che sono il server... in una split-tunnell VPN abbiamo una connessione tunnel criptata magari specifica per una certa rete (ad esempio che so... 10.10.10.10/24) in questo modo la connessione a questa specifica rete è criptata ma alle altre reti siamo in braccio a Dio, questo significa che tutto il resto non è criptato. 

3. **SSL VPN:** è essenzialmente una VPN realizzata all'interno del nostro browser, generalmente questi "programmi" trasmettono applicazioni o intere sessioni desktop al browser. 

### Fra le stronzissime terminologie di riferimento, abbiamo... rullo di tamburi....

1. **La GAN: Global Area Network**, una struttura megalattica mondiale come Internet ad esempio è una GAN. MA NON SOLOOO!! Anche diverse compagne internazionali utilizzano reti isolate che si estondono attraverso l'utilizzo di più WAN collegando così computer in tutto il mondo. Utilizzano strutture in fibra di vetro ad altro raggio e le interconnettono fra di loro attraverso cavi internazionali sotto marini o trasmissioni satellitari. (ROBA DA SPIONAGGIO INTERGALATTICO)

2. **La MAN:** Metropolitan Area Network, se la GAN collega diverse MAN la MAN collega diverse LAN in prossimità geografica. Vi prego non odiatemi.... Questo avviene tramite vengono utilizzati router e reti a fibra di vetro ad alte prestazioni, questo consente una velocità di scambio di informazioni notvalmente superiore a quella di Internet (che poi non si sa perché ma dovrebbe essere internet anche questa), la velocità di trasmissione può essere paragonata a quella di una LAN. Le città collegate come MAN possono essere integrate in realtà sopra-regionali nelle WAN e internazionalmente come GAN. 

3. **La PAN o WPAN:** Personal Area Network, essenzialmente i dispositivi moderni come smartphone, tablet e computer possono essere collegati tra di loro creando così una rete ad hoc che consente lo scambio di dati. Può avvenire via cavo PAN o via wireless WPAN. In questo caso però ovviamente la fregatura sta nel fatto che una PAN creata via wireless è chiamata Piconet. Si estendono, poverine, per poche metri e non sono adatte a collegare dispositivi in diverse stanze separate o diversi uffici... che poi anche qui perché? Se è possibile connetterle via Wireless.

See you next time bro!!!

