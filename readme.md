# Git intro opgave

## Opret en mappe som du bruger som project til VC code
- Opret en index.html fil 
- Opret en readme.md fil
## Tilføj git
- Opret en git fil
    - git init
- Skift master til dev
    - git branch -m dev
## Tilføj dine tilføjelser  
- Git Add
    - git add .
- Git commit
    - git commit -m "Besked"
## Tilknyt dit lokale repository
- Opret et repository på gitHub
    - https://github.com/
    - Øverst til venstre vil der ud for Top repositoris være et knap "New" som oprette et nyt repository
    - Når du har oprettet dit gitHub repository vil der være to branches, en __main__ og en __dev__ branche 

- I VS code's terminal tilføj dit gitHub repository
    - git remote add origin https://github.com/brugernavn/projektnavn.git
- Git push til dev på GitHub 
    - git push -u origin dev
## Bekræft at det virker
- Gå ind på GitHub
- Opdater siden
- Dine filer burde nu være der
## Git Flow
- Tilføj til dit projekt fx. et nyt stykke kode
    - `git add .` 
    - `git commit -m "besked"`
    - `git push -u origin dev`