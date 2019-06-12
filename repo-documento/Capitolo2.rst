2. **Abilitazione e accesso GIT tramite account aziendale**
==============================================================

Git è un sistema di gestione delle versioni che consente a una o più
persone di contribuire alla creazione e aggiornamento dei diversi file
di un progetto.

All’indirizzo https://git.intranet.sardegnait.it/ è disponibile il git
aziendale, basato sulla piattaforma open source **GitLab**
https://docs.gitlab.com/ . Per accedere al Git aziendale tramite è
necessario avere una email aziendale e una apposita password che verrà
inviata all’indirizzo di posta elettronica personale aziendale.

Nel caso l’account non sia stato ancora creato, è necessario chiedere
l’abilitazione all’Area Sistemi dell’azienda o al proprio Responsabile.

Una volta scaricato **Git** da https://git-scm.com/ e ricevuta l’email
di corretta attivazione dell’account aziendale, si può procedere con il
primo accesso che può avvenire tramite browser o tramite riga di
comando.

2.1 **Accesso tramite browser**
-----------------------------------

1. Accedere a https://git.intranet.sardegnait.it/
<img src="13.png" width="600">

2. Nel campo “username or email” inserire la propria email personale

3. Nel campo “password” inserire la password ricevuta per email

4. Completata la fase di login, modificare la password avendo cura di
   segnare quella nuova in un posto sicuro e riservato
NB. Se durante gli accessi successivi si dovesse smarrire o dimenticare
la password è possibile seguire il percorso “Forgot your password?” per
recuperarla. Verrà inviato un link all’indirizzo email aziendale
autorizzato e utilizzato come username.

5. Completato l’accesso a Git:

   a. se l’account non è stato autorizzato a progetti già esistenti,
      sarà possibile creare un nuovo progetto o un nuovo gruppo

   b. se è necessario accedere a progetti già esistenti chiedere
      l’abilitazione al proprio Responsabile

   c. se l’account è autorizzato a progetti già esistenti, sarà
      possibile accedere alla lista progetti oppure crearne nuovi

2.2 **Accesso tramite linea di comando**
------------------------------------------

Oltre l’accesso tramite browser, Git può essere utilizzato da linea di
comando per trasferire i file dal repository aziendale al proprio
computer e viceversa.

Tale accesso da linea di comando può avvenire:

-  Tramite email/password

-  Tramite chiave ssh

L’accesso tramite chiave ssh consente di evitare l’inserimento di
email/password ad ogni comando, ma richiede come ulteriore passo la
generazione (nel GIT locale) una chiave ssh che, dopo esser stata
salvata sul GIT aziendale, consenta al repository aziendale di
riconoscere ed accettare files o aggiornamenti di versione eseguiti con
l’account in uso.

---

[Capitolo Precedente](Capitolo1.md) (1. Installazione GIT)

[Capitolo Successivo](Capitolo3.md) (3. GIT - Stati e sezioni di progetto)

[Indice](README_INDEX.md)