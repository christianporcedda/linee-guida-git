**Sequenza dei comandi git**
============================

4.1 **Clone**
----------------
         :name: clone

Per poter iniziare ad operare su un progetto esistente sul repository
aziendale è necessario effettuare una copia locale tramite il comando:
  
**git clone [url]**

L’esecuzione del comando git clone consente di scaricare le versioni 
di ciascun file associato al progetto.
Il comando va eseguito nella Powershell, che va cercata tra le app di Windows.

Il comando

**git clone** **git@git.intranet.sardegnait.it:user/progetto.git**

**git**. Corrisponde al proprio user Git. Il proprio utente è riportato
nella sezione profilo di solito corrisponde a @ncognome

<img src="14.png" width="600">

**use**\ r. Corrisponde allo user del creatore del progetto

**progetto** Corrisponde al nome del progetto

NB. La stringa git@git.intranet.sardegnait.it:user/progetto.git è
recuperabile anche dalla pagina del progetto su
`https://git.intranet.sardegnait.it <https://git.intranet.sardegnait.it/>`__

Questo comando, eseguito in ambiente locale, creerà una directory
“progetto” in cui verranno scaricati dal repository aziendale tutti i
dati di progetto ed un file **.git** attraverso il quale si effettuerà
il controllo dell’ultima versione scaricata.


