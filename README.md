# tliu-lc.github.io — Site vitrine LIU Consulting

Site vitrine du cabinet de conseil **LIU Consulting** (Tim LIU), hébergé sur GitHub Pages.

**URL live** : https://tliu-lc.github.io

---

## Architecture des 3 sites

```
tliu-lc.github.io                   ← Ce repo — site cabinet LIU Consulting
    ↓ lien "En savoir plus"
tliu-lc.github.io/retail-dashboard/ ← Repo retail-dashboard — vitrine offre tableau de bord
    ↓ lien "Ouvrir la démo"
demo-frontend-bl6u7ximoa-ew.a.run.app ← App démo live (Cloud Run / GCP delor-demo)
                                         Login : demo / demo2024
```

---

## Structure du repo

```
/
├── index.html        ← Site complet (page unique, tout inline)
├── tim.png           ← Photo de profil Tim LIU (fond navy #0c1a35)
├── dashboard.png     ← Screenshot dashboard (non utilisé en héro, conservé)
└── README.md
```

Tout le site est dans **un seul fichier `index.html`** — HTML + CSS + JS inline. Pas de build, pas de node_modules, pas de dépendances locales.

---

## Design

**Inspiré de BCG.com** — style grand cabinet de conseil.

| Élément | Valeur |
|---|---|
| Fond principal | `#ffffff` blanc |
| Navy (hero, nav CTA, stack) | `#0c1a35` |
| Or (accent, hover, labels) | `#b08d57` |
| Typographie titres | Playfair Display (Google Fonts) |
| Typographie corps | Inter 400 (Google Fonts) |
| Fond sections alternées | `#f5f4f1` (crème chaud) |

**Sections dans l'ordre :**
1. Nav blanche fixe
2. Hero sombre (headline + SVG data abstrait + strip 4 principes)
3. Expertise — chips filtres + grille de cards (featured navy + 4 régulières)
4. Stack technique — section navy, 8 technologies en grille 4×2
5. Approche — 3 étapes numérotées 01/02/03
6. Offres — 2 grandes cartes (Abonnement 2 500€/mois + Mission 45 000€ HT) + 2 petites "bientôt"
7. À propos — photo Tim + bio + coordonnées
8. Témoignage — citation client
9. Contact — section navy
10. Footer

---

## Contenu et coordonnées

- **Nom** : Tim LIU — LIU Consulting
- **SIRET** : 91929307600023
- **Email** : tim.liu.liuconsulting@gmail.com
- **Téléphone** : 06 03 65 53 98
- **LinkedIn** : linkedin.com/in/tim-liu-liuconsulting

**Offres affichées :**
- Abonnement tout inclus : 2 500 €/mois HT
- Forfait mission : 45 000 € HT + maintenance optionnelle 8 000 € HT/an
- Automatisation des reportings : bientôt
- Audit & diagnostic data : bientôt

---

## Modifier le site

Tout se fait dans `index.html`. Pas de toolchain.

**Modifier un texte** → éditer directement dans `index.html`

**Remplacer la photo** → remplacer `tim.png` (format carré ou portrait recommandé, fond navy `#0c1a35`)

**Ajouter une offre** → dupliquer un bloc `.card` dans la section `#expertise` ou un bloc `.osm` dans `#offres`

**Déploiement** → `git push origin main` — GitHub Actions publie automatiquement (workflow `.github/workflows/pages.yml` dans ce repo, si configuré, sinon GitHub Pages legacy sur `main / /`)

---

## GitHub Pages — configuration

- **Source** : branche `main`, dossier `/` (racine)
- **Type** : Legacy (Deploy from a branch) ou GitHub Actions selon configuration
- Le repo `tliu-lc.github.io` est le repo spécial GitHub Pages user — `index.html` à la racine = site principal

---

## Liens utiles

- Site cabinet (ce repo) : https://tliu-lc.github.io
- Vitrine dashboard : https://tliu-lc.github.io/retail-dashboard/
- Repo vitrine dashboard : https://github.com/tliu-lc/retail-dashboard
- App démo : https://demo-frontend-bl6u7ximoa-ew.a.run.app
- Projet GCP : `delor-demo` (europe-west1)
