# PROTOCOLE SESSION — IA Idle Tycoon
> SlowAI Studio 🐢 — À lire avant chaque session et après chaque livraison

---

## 1. DÉMARRAGE DE SESSION

Écris dans le chat Claude (Project "IA Idle Tycoon") :

```
Session V1.X — [objectif du jour]
```

Claude va automatiquement :
1. Lire `ia-idle-tycoon-v1.X.html` depuis Google Drive
2. Confirmer la version lue + résumer l'état du jeu en 3 lignes
3. Coder selon ton objectif

---

## 2. CHECKLIST DE FIN DE SESSION

### ① Télécharger le fichier livré
- Télécharge le `.html` livré par Claude
- Renomme-le : `ia-idle-tycoon-v1.X.html`

---

### ② Google Drive
Chemin : `Idle Tycoon IA Claude/01_Code/HTML_Prototypes/`

- [ ] Upload du nouveau `.html` dans `01_Code/HTML_Prototypes/`
- [ ] Vérifier que `05_Admin/CHANGELOG_global.txt` est à jour (Claude le fait normalement)
- [ ] Mettre à jour `05_Admin/IA_Idle_Tycoon_Suivi_Projet.xlsx` (backlog, statut tâches)

---

### ③ GitHub
Repo : `IA-IDLE-TYCOON-CLAUDE` — branche `main`

**Avec GitHub Desktop :**
1. Copie le fichier `.html` dans le dossier local du repo → `01_Code/HTML_Prototypes/`
2. Ouvre GitHub Desktop — le fichier apparaît dans "Changes"
3. Message de commit : `v1.X — [résumé en une ligne]`
   - Exemple : `v1.9 — tables de config data-driven + structure projet`
4. Clique **Commit to main**
5. Clique **Push origin**

**Avec le terminal :**
```bash
cp ~/Downloads/ia-idle-tycoon-v1.X.html ./01_Code/HTML_Prototypes/
git add .
git commit -m "v1.X — [résumé en une ligne]"
git push origin main
```

---

### ④ Mettre à jour le prompt système Claude

Dans Claude.ai → Project "IA Idle Tycoon" → icône **crayon** (Instructions du projet)

Trouve le bloc `## ÉTAT DU DÉVELOPPEMENT` et mets à jour ces 3 lignes :

```
- Version courante : V1.X
- Dernière version livrée : ia-idle-tycoon-v1.X.html
- Prochaine version : V1.X+1
```

---

### ⑤ Vérification finale

- [ ] Fichier HTML lisible dans le navigateur ?
- [ ] Drive à jour ?
- [ ] GitHub à jour (commit + push) ?
- [ ] Instructions du Project Claude mises à jour ?
- [ ] CHANGELOG rempli ?

---

## 3. REPRISE APRÈS UNE LONGUE PAUSE

1. Lis ce fichier
2. Ouvre le Project Claude "IA Idle Tycoon"
3. Vérifie les instructions du projet (bloc `ÉTAT DU DÉVELOPPEMENT`)
4. Écris : `Session V1.X — reprise projet`
5. Claude relit tout depuis Drive et te résume l'état en 3 lignes

---

## 4. STRUCTURE DU REPO GITHUB

```
IA-IDLE-TYCOON-CLAUDE/
├── 01_Code/
│   └── HTML_Prototypes/
│       ├── ia-idle-tycoon-v1.8.4.html
│       ├── ia-idle-tycoon-v1.9.html
│       └── ...
├── .gitignore
├── CHANGELOG_global.txt
├── IA_Idle_Tycoon_Suivi_Projet.xlsx
└── README.md
```

---

## 5. STRUCTURE GOOGLE DRIVE

```
Idle Tycoon IA Claude/
├── 01_Code/
│   └── HTML_Prototypes/     ← fichiers .html versionnés
├── 02_GDD/                  ← Game Design Document
├── 03_Assets/
├── 04_Marketing/
└── 05_Admin/
    ├── CHANGELOG_global.txt
    └── IA_Idle_Tycoon_Suivi_Projet.xlsx
```

> `.gitignore` et `README.md` → GitHub uniquement, pas sur Drive.

---

*Dernière mise à jour : mai 2026*
