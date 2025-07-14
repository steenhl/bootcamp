# Git Intro Opgave

## 1. Opret Projektmappe i VS Code
- Opret en mappe, som skal være dit projekt
- Inde i mappen:
    - Opret en `index.html` fil
    - Opret en `readme.md` fil

---

## 2. Initialiser Git i Projektet
Åbn terminalen i VS Code og kør:
```bash
git init
```

### Skift standard branch til `dev`
```bash
git branch -m dev
```

---

## 3. Første Commit
Tilføj alle filer og lav første commit, samt en beskrivelse `Initial commit`
```bash
git add .
git commit -m "Initial commit"
```

---

## 4. Opret Repository på GitHub
- Gå til: [https://github.com](https://github.com)
- Klik på **New** (øverst til venstre ved "Top Repositories")
- Opret et repository med samme navn som din mappe

Når du har oprettet repository, kopier linket, fx:
```bash
https://github.com/brugernavn/projektnavn.git
```

---

## 5. Tilknyt Lokalt Repository til GitHub
Kør følgende i terminalen:
```bash
git remote add origin https://github.com/brugernavn/projektnavn.git
git push -u origin dev
```

---

## 6. Bekræft at Det Virker
- Gå til dit repository på GitHub
- Opdater siden
- Dine filer fra `dev` branch bør være synlige

---

## 7. Git Workflow i Hverdagen
Når du laver ændringer:
```bash
git add .
git commit -m "Beskrivelse af ændringer"
git push origin dev
```

---

## 8. Opret Lokale Branches
Det er god praksis at arbejde i separate branches for ny funktionalitet.

### Opret Ny Lokal Branch
```bash
git checkout -b nyBranch
```

### Lav Ændringer og Commit
```bash
git add .
git commit -m "Beskrivelse af ændringer"
```

### Skift Tilbage til `dev`
```bash
git checkout dev
```

### Merge Din Nye Branch Ind i `dev`
```bash
git merge nyBranch
```

### Push `dev` Til GitHub
```bash
git push origin dev
```

### Valgfrit: Slet Lokal Branch Efter Merge
```bash
git branch -d nyBranch
```

---

## 9. Komplet Eksempel på Workflow
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

**Tip:** Mange af disse trin kan også udføres via VS Code's grafiske Source Control menu.
