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

## Oprettelse af lokale branch
Det er en god praksis at oprette en lokal branch for hver ny funtionalitet. Når man er færdig tilføjes ændringerne til den lokale dev
## Git Branch Oprettelse og Merge - Hurtig Opsummering

### Opret Ny Lokal Branch
```bash
git checkout -b nyBranch
```

### Lav Ændringer og Commit
```bash
git add .
git commit -m "Beskrivelse af ændringer"
```

### Skift Tilbage til `dev` Branch
```bash
git checkout dev
```
Hvis `dev` ikke findes endnu:
```bash
git checkout -b dev
```

### Merge Ny Branch Ind i `dev`
```bash
git merge nyBranch
```

### Push `dev` Til GitHub
```bash
git push origin dev
```

### (Valgfrit) Slet Lokal Branch Efter Merge
```bash
git branch -d nyBranch
```

---

### Komplet Workflow Eksempel
```bash
git checkout -b feature-login
# Lav ændringer
git add .
git commit -m "Tilføjer login funktion"
git checkout dev
git merge feature-login
git push origin dev
git branch -d feature-login
```

---

**Bemærk:** Du kan også udføre mange af disse trin via VS Code's Source Control interface, hvis du foretrækker grafisk overblik.
