6. **Visualizzare le differenze**
===============================

Git status consente di individuare i file che hanno subito delle
modifiche ma non consente di capire quali cambiamenti siano stati
apportati agli stessi file.

Tale esigenza è soddisfatta dal comando **git diff** che può essere
eseguito con o senza il suffisso **--cached**.

**git diff** permette di visualizzare le eventuali modifiche non ancora
ricomprese nello stage.

**git diff --cached** permette di visualizzare le eventuali modifiche
ricomprese nello stage.

6.1 **Branch**
------------

Con il termine branch si fa riferimento a una linea di sviluppo
collegata ma indipendente dalla linea di sviluppo principale vale a dire
il branch master. Attraverso il comando git branch è possibile creare
delle “diramazioni” nelle quali è possibile effettuare modifiche ed
aggiornamenti di file senza che le stesse modifiche interferiscano con i
file o il codice ricompreso nel branch master.

I branch (e quindi i file ad esso collegati) possono poi essere in
qualche modo ricondotti al master attraverso una apposita procedura di
merging.
I comandi principali sono git branch per la creazione della
diramazione e git checkout per il posizionamento sulla stessa.
Ad esempio:

---------------------------------------
*$ git branch area_svi (creazione diramazione)*

*$ git checkout area_svi (posizionamento nel ramo creato)*

*$ vim test.txt (creazione di un nuovo file)*

*$ git commit -a -m 'nuovo doc' (add e commit relativo al nuovo file
creato nel nuova branch area_svi)*
-----------------------------------------

Il file creato, attraverso il commit, viene “attribuito” al branch e
non risulta facente parte dei file attribuiti al master o radice
principale memorizzata nel repository locale. In tal modo è possibile
isolare eventuali sviluppi che non si desidera immediatamente
attribuire al master.
Nel caso, infine, si voglia ricomprendere quanto realizzato nel branch
all’interno del master:
  
--------------------------------------------
*$ git checkout master*

*$ git merge* *area_svi*
----------------------------------------------

6.2 **Controllo dello stato dei Branch**
---------------------------------------

Si fa presente che il generico comando **git branch** consente di
ottenere la lista dei rami correnti, es:

---------------------------------------------
*$ git branch*

*area_svi*

*\* master*

*area_svi_2*
---------------------------------------------------

L’asterisco indica in quale branch siamo posizionati.

Un ulteriore controllo può riguardare la verifica di quali branch siano
stati fusi nel ramo master principale. Attraverso il comando **git
branch –merged**, es:

-----------------------------------------
*$ git branch --merged*

*area_svi*

*\* master*
-----------------------------------------------------

Al contrario il comando **git branch –no-merged** permette di
visualizzare i branch non ancora fusi nel master principale, es:

--------------------------------------------------------------
*$ git branch –no-merged*

*area_svi_2*
--------------------------------------------------------------

6.3 **Inserire immagini**
-----------------------------
Per inserire delle immagini nel proprio repository su GitLab è necessario andare nel repository del
progetto nel quale si vogliono inserire le immagini e cliccare sul **+** affianco al nome del repository. 
A questo punto bisogna cliccare su **Upload file** e trascinare i file (in questo caso le immagini) uno
alla volta nel riquadro che appare, oppure si può scegliere il file cliccando su **click to upload**,
infine cliccate sul bottone verde **Upload file**. Ripetere queste operazioni tante volte quanti sono i
file da inserire.

---

<img src="19.png" width="800">

---


6.4 **Come inserire immagini nei .MD**
---------------------------------------
Per inserire le immagini nei file .MD è necessario seguire la seguente sintassi:
**< img src="nome_immagine.estensione" width="800" >**  (senza spazi dopo < e prima di >)

es. < img src="gita_2012.png" width="600" >

6.5 **Rimuovere un file**
-----------------------

Nel caso in cui si intenda escludere uno specifico file da un successivo
commit (rimozione dall’area di stage) il comando da utilizzare
corrisponde a **git reset HEAD <file>**.

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*modified: analisi.txt*

*modified: documentazione.txt*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Nell’esempio si mostra la rimozione del file analisi.txt dalla lista dei
file da committare:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
*$*\ **git reset HEAD analisi.txt**

*Unstaged changes after reset:*

*M analisi.txt*

*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*modified: documentazione.txt*

*Changes not staged for commit:*

*(use "git add <file>..." to update what will be committed)*

*(use "git checkout -- <file>..." to discard changes in working
directory)*

*modified: analisi.txt*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

6.6 **Annullare una modifica**
----------------------------

Il precedente esempio ci permette di introdurre una ulteriore funzione
di modifica, vale a dire il comando **git checkout -- <file>**.
Attraverso il git status (esempio 3.8) è emerso che il file
*analisi.txt* risulta modificato e non ricompreso nell’area di stage.
Il sistema ci informa, inoltre, che è possibile annullare le modifiche
  apportate al file analisi.txt attraverso il comando git checkout --
  <file> rimuovendole dunque dalla directory di lavoro

Nello specifo l’esecuzione del comando porterebbe a\ *:*

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
*$ git checkout – analisi.txt*

*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*modified: documentazione.txt*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

6.7 **Fork: lavorare con diversi utenti**
-------------------------------------------

Per poter effettuare degli interventi sul repository di un altro utente, è consigliabile operare su un “fork”.

Il fork è una copia di un progetto, che viene salvata sul proprio
account, e consente quindi di effettuare su questa copia le modifiche e
quando tali modifiche sono completate, è possibile inviare al
proprietario del progetto originale una richiesta di merge.

---

[Capitolo Precedente](Capitolo5.md) (5. Controllo dello stato dei file)

[Capitolo Successivo](Capitolo7.md) (7. Documentazione tecnica)

[Indice](README_INDEX.md)
