```markdown
# Rendu : MaRtInRxU

- Dépôt : tp-git-
- Site GitHub Pages : https://martinrxu.github.io/tp-git-/

## Ex2
git log --oneline : 
ba0a6a4 (HEAD -> main, origin/main) ex2: corrige une faute
7ba321b ex2: ajoute trois lignes
4d870dc ex2: crée les notes
7371db8 ex1: initialise le dépôt

## Ex3
- config.local est-il encore dans l'historique ? Pourquoi ?
oui, config.local est encore dans l'historique, le commit de correction arrête le suivi du fichier à partir de ce moment là, mais n'efface pas le commit précédent

## Ex4
- git status après avoir retiré brouillon.txt du staging :
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   RENDU.md
	modified:   brouillon.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	.DS_Store
	node_modules/

no changes added to commit (use "git add" and/or "git commit -a")
- Différence entre annuler une modification et retirer du staging ?
git restore brouillon.txt annule les modifications non commitées du fichier 
git restore --staged brouillon.txt retire le fichier du staging mais conserve les modifications dans le fichier

## Ex6
- À quoi servent <<<<<<<, ======= et >>>>>>> ?
ce sont des marqueurs temporaires qui indiquent qu'il y a un conflit entre les deux branches (main et version-en)
<<<<<<< indique le début de la version actuelle de main 
======= sépare les deux versions
>>>>>>> marque la fin de la verison provenant de version-en 

## Ex7
- git stash list (avant récupération) :
stash@{0}: On main: travail en cours
- Pourquoi annuler un commit plutôt que l'effacer de l'historique ?
git revert conserve les commits existabnts et ajoute une trace de l'annulation, c'est plus sûr lorsque l'historique a déjà été partagé avec d'autres personnes

## Ex8
- git pull = git fetch + quoi ?
git pull = git fetch + changements récupérés par git merge 

## Ex10
git log --oneline --graph --all :* 5d3a922 (HEAD -> main, origin/main, origin/HEAD) ex9: relance le déploiement
* 5bd3144 ex9: ajoute la page d'accueil
* 5918173 ex8: modification depuis GitHub
*   30814a9 Merge pull request #1 from MaRtInRxU/feature-contact
|\  
| * 2caa37a (origin/feature-contact, feature-contact) ex8 : ajoute la page contact
|/  
* b1a9170 ex7: ajoute la ligne en cours
* d46659e Revert "ex7: ajoute une ligne par erreur"
* bc843de ex7: ajoute une ligne par erreur
*   9c9bf6a ex6: résout le conflit du titre
|\  
| * 67fe5da (origin/version-en) ex6: titre en anglais
* |   863c7d2 ex6: fusionne version-fr
|\ \  
| |/  
|/|   
| * be0e2c6 (origin/version-fr) ex6: titre en français
|/  
*   a4bb8ca ex5: fusionne feature menu
|\  
| * 65ef87e (origin/feature-menu) ex5: ajoute un dessert
| * 296dba2 ex5: crée le menu
|/  
* 24878c9 ex4: supprime a-supprimer.txt
* 048b29c ex4: renomme ancien.txt
* 0914c91 ex4: ajoute trois fichiers
* 3ec36e0 ex3: arrête de suivre config.local
* 9423499 ex3: ajoute config.local (erreur)
* 2a8f984 ex3: ajoute .gitignore
* ba0a6a4 ex2: corrige une faute
* 7ba321b ex2: ajoute trois lignes
* 4d870dc ex2: crée les notes
* 7371db8 ex1: initialise le dépôt
```