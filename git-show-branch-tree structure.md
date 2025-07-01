# Git Workflow med --no-ff (Bevar Gren-Struktur)

## Formål
Brug `--no-ff` ved merge for at sikre, at alle merges genererer en separat commit, så gren-strukturen bevares i din Git-historik. Dette giver et mere overskueligt grafisk træ i f.eks. Git Graph eller SourceTree.

---

## Standard Workflow med --no-ff

### 1. Skift til `dev` Branch og Hent Seneste Version
```bash
git checkout dev
git pull origin dev
```

### 2. Opret Ny Branch til Funktionalitet
```bash
git checkout -b feature-navn
```
Erstat `feature-navn` med noget sigende, fx `feature-login`.

### 3. Lav Ændringer, Tilføj og Commit
```bash
git add .
git commit -m "Beskrivelse af ændringer"
```

### 4. Skift Tilbage til `dev` og Merge med --no-ff
```bash
git checkout dev
git pull origin dev
```
Merge med synlig merge-commit:
```bash
git merge --no-ff feature-navn -m "Merge feature-navn"
```

### 5. Push til GitHub
```bash
git push origin dev
```

### 6. (Valgfrit) Slet Lokal Branch
```bash
git branch -d feature-navn
```

---

## Eksempel med Login Funktion
```bash
git checkout dev
git pull origin dev
git checkout -b feature-login
# Lav ændringer
git add .
git commit -m "Tilføjer login funktion"
git checkout dev
git pull origin dev
git merge --no-ff feature-login -m "Merge login funktion"
git push origin dev
git branch -d feature-login
```

---

## Fejl og Løsning
Hvis du får fejl som:
```
merge: feature-login - not something we can merge
```
Sikre følgende:
- Du står på `dev` eller en anden base-branch
- Branch'en `feature-login` findes lokalt
- Brug korrekt stavemåde

Tjek branches:
```bash
git branch
```
Hvis branch mangler:
```bash
git checkout -b feature-login
```

---

**Bemærk:** Dette workflow sikrer tydelig gren-struktur i grafiske værktøjer som Git Graph, VS Code eller SourceTree.
