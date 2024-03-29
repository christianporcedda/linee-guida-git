
4. **Sequenza dei comandi git**
================================
      git sequenza-dei-comandi-git

4.1 **Clone**
----------------
         git clone

Per poter iniziare ad operare su un progetto esistente sul repository
aziendale è necessario effettuare una copia locale tramite il comando:
  
**git clone**

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


4.2 **Clone in una directory diversa**
----------------------------------------

Una ulteriore possibilità consiste nel definire un nome diverso alla
directory di destinazione (locale). Questo è possibile eseguendo il
comando

**git@git.intranet.sardegnait.it:user/progetto.git altro_nome_progetto**

**altro_nome_progetto**. Corrisponde al nome della directory che si
vuole creare


4.3 **Creare un Repository su GitHub**
---------------------------------------
Per creare un Repository su GitHub è necessario registrarsi su GitHub (o accedervi),
cliccare il tasto verde in altro a sinistra con scritto **"New"**.

---

<img src="15.png" width="800">

---

Nella pagina che segue assegnate un **nome** al repository, una **descrizione** (se volete)
e scegliete il **livello di visibilità**. Infine cliccate su **"Create repository""**.

---

<img src="16.png" width="800">

---


4.4 **Creare un Repository su GitLab Aziandale**
-------------------------------------------------
Per creare un Repository su GitLab è necessario registrarsi su GitLab (o accedervi) e
cliccare il tasto verde con scritto **"New Project"**. 

---

<img src="17.png" width="800">

---

Nella pagina che segue assegnate un **nome**, una **descrizione** (se volete) e 
scegliete il **livello di visibilità**. Infine cliccate su **"Create project""**.

---

<img src="18.png" width="800">

---


4.5 **Init**
--------------

Attraverso il comando **git init** si potrà tenere traccia di un
progetto locale e trasformare la directory che ospita il nostro codice
in un repository per il versioning.

Dalla directory locale del progetto l’esecuzione del comando git init
creerà una nuova sottodirectory .git che conterrà i file del repository.

Per poter, successivamente, inserire il progetto nel repository
aziendale si dovrà eseguire il comando:

**git remote add origin
git@git.intranet.sardegnait.it:user/progetto.git**

4.6 **Add**
----------

Il tracciamento dei file avviene attraverso il comando **git add**.

Dalla directory di progetto l’esecuzione del comando git add \*
consentirà di aggiungere all’area di stage i file che si intende
monitorare (nel caso git add sia seguito da un \* verranno aggiunti
tutti i file).

4.7 **Commit**
------------

Il comando **git commit** consente di completare il monitoraggio dei
file nel repository locale.

Dopo l’esecuzione del comando git add si procede con il comando **git
commit –m** **‘descrizione operazione’**.

L’opzione –m ‘….’ Consente di inserire un testo descrittivo delle
modifiche eseguite.

4.8 **Push**
---------

Attraverso il comando git push quanto monitorato in locale può essere
riportato sul repository aziendale.

In sintesi, nel caso di progetto locale preesistente (punto 3.3.2), si
riportano i comandi da eseguire per l’aggiornamento del repository
aziendale:


*git init*

*git remote add origin
git@git.intranet.sardegnait.it:scasu/ILA-SUP-02.git*

*git add .*

*git commit –m ‘descrizione operazione’*

*git push -u origin master*

---

[Capitolo Precedente](Capitolo3.md) (3. GIT - Stati e sezioni di progetto)

[Capitolo Successivo](Capitolo5.md) (5. Controllo dello stato dei file)

[Indice](README_INDEX.md)
