# flow of initialisation project 

- gh auth status 
- mkdir blog-des-laureats
- cd blog-des-laureats
- New-Item -ItemType File -Name ".gitignore"( insted of linux command touch .gitignore)
- git init
- git checkout -b sprint1
- mkdir -p tutoriels/realisation-projet/initialisation/publication-github
- New-Item -ItemType File -Name "publication-github.command.md"
- git add .gitignore tutoriels/realisation-projet/initialisation/publication-github/publication-github.command.md
- git commit -m "feat: initialisation du projet et journal des commandes"

# verifiyng 
-  git branch --show-current
-  git log --oneline
-   git remote -v

# creating main branch (last livrable station)
-  git switch -c main
- git push -u origin main