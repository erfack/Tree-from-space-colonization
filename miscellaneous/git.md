# Utilizzo di Git e buone prassi
### Questo file descrive come utilizzare Git esponendo i comandi base di Git e le buone prassi, per comandi avanzati vedere [git_commands.txt](../master/miscellaneous/git_commands.txt). <br />
## Comandi base 
#### 1. Copia repo in locale:
    git clone https://github.com/erfack/Tree-from-space-colonization.git LOCAL_FOLDER
#### 2. Aggiornare la repo in locale:
    git pull 
#### 3. Aggiungere un file alla repo locale:
    git add NOME_FILE
    
  #### In alternativa, per effettuare l'add di tutti i file:
    
    git add .
#### 4. Effettuare un commit:
    git commit NOME_FILE -m "Titolo" -m "Primo messaggio" -m "Secondo messaggio" ... -m "n-esimo messaggio"
  L'opzione -m permette di inserire una descrizione del commit che si sta effettuando. Buona prassi è quello di scrivere un titolo breve (ad esempio: *add class NOME_FILE*, *fix NOME_FILE*, *modify document NOME_FILE*, ecc...) che non superi i 50 caratteri. <br /> I messaggi successivi fungono da descrittori del commit (ad esempio: *Aggiunta la classe C*, *Modifica della 4a sezione*, *Fix del bug nella funziona delta*) suddivisi in paragrafi di non più di 72 caratteri ciascuno.
#### 5. Effettuare l'upload:
    git push
#### 6. Vedere gli ultimi k commits:
    git log -n k
## Esempio di utilizzo
Trovandosi nella cartella *LOCAL_FOLDER* e volendo effettuare il commit del file *FILE.f*  

    git add FILE.f
    git commit FILE.f -m "add FILE.f" -m "qualche descrizione"
    git pull
    git push

Il terzo passo previene il conflitto in caso si stia modificando un file non aggiornato nella propria repo locale.
## Altro
1. Prima di mettersi a lavoro è consigliato di leggere gli ultimi 10 (o più) log (vedi punto 6 di Comandi Base)

2. Non effettuare il refactoring di file o cartelle. Potrebbe causare un branch non desiderato del progetto. (Specialmente se qualcuno sta lavorando su essi)

3. Effettuare un commit ogni 15 minuti di lavoro così da poter tenere traccia dei cambiamenti e poter tornare indietro in un qualsiasi punto se necessario.
