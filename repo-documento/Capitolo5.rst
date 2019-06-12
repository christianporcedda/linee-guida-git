5. **Controllo dello stato dei file**
========================================

Il controllo dello stato dei file avviene attraverso il comando **git
status**. Tale comando permette di verificare la situazione dei file nel
repository locale, evidenziando eventuali aggiornamenti dei file
tracciati o anche la presenza di possibili file “untracked” non ancora
versionati.

-  Nel caso in cui nessuno dei file tracciati abbia subito modifiche
   l’esecuzione del comando git status restituirebbe una situazione del
   tipo:
   

*$ git status*

*# On branch master*

*nothing to commit, working directory clean*


-  Nel caso in cui, invece, al progetto in locale sia stato aggiunto un
   nuovo file (es. analisi.txt) il comando git status restituirebbe una
   situazione del tipo:
   

*$ git status*

*On branch master*

*Untracked files:*

*(use "git add <file>..." to include in what will be committed)*

*analisi.txt*

*nothing added to commit but untracked files present (use "git add" to
track)*

In questa situazione è emersa la presenza di un nuovo file non ancora
tracciato e la necessità di eseguire il comando git add nel caso lo si
voglia ricomprendere tra i file da sottoporre a versionamento.

-  Un ulteriore caso può essere quello in cui un file in precedenza già
   tracciato viene modificato (es. il file documentazione.txt).
   L’esecuzione del comando git status successivamente alla modifica del
   file restituirebbe una situazione del tipo:
   
---
*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*new file: analisi.txt*

*Changes not staged for commit:*

*(use "git add <file>..." to update what will be committed)*

*(use "git checkout -- <file>..." to discard changes in working
directory)*

*modified: documentazione.txt*
---

La situazione rappresentata espone sia il nuovo file aggiunto (vedi
esempio precedente) sia il file documentazione.txt sottoposto a
modifica.

Come si può notare il primo appare nella sezione *Changes to be
committed* e può quindi essere committato attraverso il comando git
commit, mentre il secondo appare nella sezione *Changes not staged for
commit* e per esso sarà necessario eseguire il comando *git add
documentazione.txt* al fine di poter eseguire un successivo *git commit
–m ‘…….’*.

---

[Capitolo Precedente](Capitolo4.md) (4. Sequenza dei comandi GIT)

[Capitolo Successivo](Capitolo6.md) (6. Visualizzare le differenze)

[Indice](README_INDEX.md)
