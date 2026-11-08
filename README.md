<div align="center">

# 🛢️ Petroleum Refining Console

**Simulateur expert · Raffinerie 200 kbpd · Topping + FCC + Reformage + HDT**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/fr/docs/Web/JavaScript)
[![Canvas](https://img.shields.io/badge/Canvas_API-0055A4?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/API/Canvas_API)

[![License: MIT](https://img.shields.io/badge/License-MIT-1B7F4B?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-3.0.0-0055A4?style=for-the-badge)](https://github.com/gunout/Petroleum-Refining-Console/releases)
[![Maintenance](https://img.shields.io/badge/maintained-yes-1B7F4B?style=for-the-badge)](https://github.com/gunout/Petroleum-Refining-Console/graphs/commit-activity)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-EF4135?style=for-the-badge)](https://github.com/gunout/Petroleum-Refining-Console/pulls)

[![Arab Light](https://img.shields.io/badge/Arab_Light-API_33-8B5E34?style=flat-square)](#)
[![Capacity](https://img.shields.io/badge/Capacity-200_kbpd-0055A4?style=flat-square)](#)
[![Sulfur](https://img.shields.io/badge/Sulfur-1.8%25-D97706?style=flat-square)](#)
[![Margin](https://img.shields.io/badge/Margin-9.4_$/bbl-1B7F4B?style=flat-square)](#)
[![EN228](https://img.shields.io/badge/EN_228-✓-1B7F4B?style=flat-square)](#)
[![EN590](https://img.shields.io/badge/EN_590-✓-1B7F4B?style=flat-square)](#)
[![Jet A-1](https://img.shields.io/badge/Jet_A-1-✓-1B7F4B?style=flat-square)](#)

[![Made in France](https://img.shields.io/badge/Made_in-France-0055A4?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAzIDIiPjxyZWN0IHdpZHRoPSIzIiBoZWlnaHQ9IjIiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iMiIgaGVpZ2h0PSIyIiBmaWxsPSIjMDA1NUE0Ii8+PHJlY3QgeD0iMiIgd2lkdGg9IjEiIGhlaWdodD0iMiIgZmlsbD0iI0VGNDEzNSIvPjwvc3ZnPg==)](https://www.gouvernement.fr)
[![Zero Dependencies](https://img.shields.io/badge/Dependencies-0-1B7F4B?style=for-the-badge)](#)

</div>

---

## 📖 Sommaire

- [Description](#-description)
- [Fonctionnalités](#-fonctionnalités)
- [Coupes pétrolières](#-coupes-pétrolières)
- [Formules & Équations](#-formules--équations)
- [Unités industrielles](#-unités-industrielles)
- [Installation](#-installation)
- [Utilisation](#-utilisation)
- [Normes carburants](#-normes-carburants)
- [Sécurité HAZOP](#-sécurité-hazop)
- [Économie](#-économie)
- [Stack technique](#-stack-technique)
- [Structure du projet](#-structure-du-projet)
- [Contribuer](#-contribuer)
- [Avertissement](#-avertissement)
- [Licence](#-licence)

---

## 🎯 Description

**Petroleum Refining Console** est un simulateur expert mono-fichier couvrant l'ensemble d'une **raffinerie de 200 kbpd** : distillation atmosphérique (topping), distillation sous vide, FCC, reformage catalytique, hydrodésulfuration et alkylation.

De la **courbe TBP** du brut Arab Light jusqu'au **crack spread 3-2-1**, l'application intègre toutes les équations de référence du raffinage moderne.

> ⚡ **Ouvrez `index.html` → ça fonctionne.** Aucune installation, aucun build, aucune dépendance externe. Offline-first.

---

## ✨ Fonctionnalités

| Section | Description |
|---------|-------------|
| 📊 Vue d'ensemble | Brent, API, marge, PFD, débouchés |
| 📈 Courbe TBP | 4 points de coupe ajustables en temps réel |
| 🏭 Distillation | Colonne 40 plateaux animée, profil T vertical |
| 🌡️ Thermodynamique | Gravité API, équation d'Antoine (7 composés) |
| ⚗️ FCC / Reformage | Conversion, RON, HDT (S ≤ 10 ppm) |
| 💰 Économie | Crack spread, marge brute/nette, point mort |
| ⚠️ Sécurité | HAZOP 6 nœuds + simulateur fuite H₂S |
| 📋 Normes | EN 228 · EN 590 · Jet A-1 (DEF STAN 91-91) |
| 📚 Documentation | Équations, conversions, références |

**Extras** : export JSON (`Ctrl+E`), impression (`Ctrl+P`), palette tricolore, responsive, WCAG AA.

---

## 📊 Coupes pétrolières

**Brut Arab Light** · API 33 · SG 0,860 · S 1,8 %

| Coupe | TBP (°C) | Rendement | SG |
|-------|----------|-----------|-----|
| 🟦 GPL (C₁–C₄) | < 30 | 2,5 % | 0,55 |
| 🟨 Essence | 30–180 | 22,0 % | 0,74 |
| 🟩 Kérosène | 180–230 | 9,5 % | 0,80 |
| 🟧 Gasoil | 230–350 | 19,0 % | 0,85 |
| 🟫 Fioul | 350–500 | 22,0 % | 0,92 |
| 🟥 Résidus | > 500 | 25,0 % | 1,02 |

**Bilan** : distillats 50,5 % · essence+GPL 24,5 % · résidu sous vide 25,0 %

---

## 🔬 Formules & Équations

**Thermodynamique**

- Gravité API : `API = 141,5/SG − 131,5`
- Équation d'Antoine : `log₁₀ P° = A − B/(C + T)` (P en bar, T en K)
- bbl/tonne : `1000 / (ρ · 0,158987)`

**Conversion FCC** (4-lump)

- `X = 100 · [1 − exp(−k·(C/O)·τ)]`
- `k = A · exp(−Ea/RT)` avec `Ea ≈ 200 kJ/mol`

**Hydrodésulfuration (HDS)**

- `r_HDS = k · [S] · P_H₂^1,5`
- `k = A · exp(−Ea/RT)` avec `Ea ≈ 100 kJ/mol`

**Reformage catalytique**

- Naphtènes → aromatiques + 3 H₂ (déshydrogénation)
- Isomérisation · déshydrocyclisation

**Économie**

- Crack spread 3-2-1 : `(2·P_ess + 1·P_gaz − 3·P_Brent) / 3`
- Marge nette = crack spread − OPEX (4,2 $/bbl)

**Courbe TBP** (brut moyen)

- `T(W) = 30 + 4,5·W + 0,017·W²` (W en % pds distillé)

---

## 🏭 Unités industrielles

| Unité | Rôle | Conditions typiques |
|-------|------|---------------------|
| 🏭 CDU (Topping) | Distillation atmosphérique | 380 °C · 1–2 bar |
| 🔥 VDU (Vacuum) | Distillation sous vide | 400 °C · 10–30 mmHg |
| ⚗️ FCC | Craquage catalytique | 525 °C · zéolithe Y |
| 🔄 Reformage | Octane + H₂ | 500 °C · 15 bar · Pt-Re/Al₂O₃ |
| 🧪 HDT | Désulfuration | 350 °C · 30 bar · CoMo/Al₂O₃ |
| ⚗️ Alkylation | Isooctane | 10 °C · H₂SO₄ ou HF |

---

## 🚀 Installation

```bash
git clone https://github.com/gunout/Petroleum-Refining-Console.git
cd Petroleum-Refining-Console

# Ouvrir dans le navigateur
open index.html      # macOS
start index.html    # Windows
xdg-open index.html # Linux
```

Ou serveur local : `python -m http.server 8000` → http://localhost:8000

---

## 📖 Utilisation

### Raccourcis clavier

| Raccourci | Action |
|-----------|--------|
| `Ctrl + E` | Export JSON |
| `Ctrl + P` | Impression |
| `Esc` | Fermer la modale |

### Navigation

9 sections navigables via la barre latérale (overview, TBP, distillation, thermo, refining, economy, safety, specs, docs).

---

## 📋 Normes carburants

### EN 228 · Essence SP95 / SP98

| Paramètre | SP95 | SP98 |
|-----------|------|------|
| RON | ≥ 95 | ≥ 98 |
| MON | ≥ 85 | ≥ 88 |
| Soufre | ≤ 10 ppm | ≤ 10 ppm |
| Benzène | ≤ 1 % | ≤ 1 % |
| Aromatiques | ≤ 35 % | ≤ 35 % |
| Oléfines | ≤ 18 % | ≤ 18 % |
| Éthanol | ≤ 10 % v | ≤ 10 % v |
| P vapeur (été) | 45–60 kPa | 45–60 kPa |

### EN 590 · Gasoil B7/B10

| Paramètre | Valeur |
|-----------|--------|
| Indice cétane | ≥ 51 |
| Densité 15 °C | 820–845 kg/m³ |
| Soufre | ≤ 10 ppm |
| Point éclair | ≥ 55 °C |
| Viscosité 40 °C | 2,0–4,5 mm²/s |
| Distillation 95 % | ≤ 360 °C |
| EMAG (FAME) | ≤ 7 % v |

### DEF STAN 91-91 · Jet A-1

| Paramètre | Valeur |
|-----------|--------|
| Densité 15 °C | 775–840 kg/m³ |
| Point éclair | ≥ 38 °C |
| Point de congélation | ≤ −47 °C |
| Soufre total | ≤ 0,30 % |
| Point de fumée | ≥ 25 mm |

---

## ⚠️ Sécurité HAZOP

### Inflammabilité par coupe

| Coupe | Flash pt | LIE | Zone ATEX |
|-------|----------|-----|-----------|
| GPL / essence | −43 °C | 1,4 % | 🔴 Zone 0 |
| Kérosène | 38 °C | 0,7 % | 🟠 Zone 1 |
| Gasoil | 55 °C | 0,6 % | 🟡 Zone 2 |
| Fioul lourd | 70 °C | 0,5 % | 🟡 Zone 2 |
| Résidus | > 100 °C | N.A. | ⚪ Hors ATEX |
| **H₂S (HDS)** | −82 °C | 4,3 % | 🔴 Toxique |

### 6 nœuds HAZOP analysés

1. **Four topping** — T° haute → craquage thermique, cokage
2. **Colonne atm.** — P haute → PSV, rejet vapeurs
3. **Riser FCC** — T° haute → désactivation zéolithe
4. **HDT réacteur** — fuite H₂S → toxicité mortelle
5. **Soufflante H₂** — arrêt → emballement réacteur
6. **Torchère** — débit excessif → retombées liquides

### Simulateur fuite H₂S

| Concentration | Statut | Action |
|---------------|--------|--------|
| < 5 ppm | ✅ Nominal | Aucune |
| 5–50 ppm | ⚠️ Alerte TLV | Masque ADF obligatoire |
| 50–300 ppm | 🚨 Évacuation | Sortie immédiate |
| > 300 ppm | 💀 Mortel | ARI obligatoire |

---

## 💰 Économie

### Crack spread 3-2-1

- Essence 95 : 98,0 $/bbl
- Gasoil EN 590 : 102,0 $/bbl
- Brent : 82,5 $/bbl
- **Crack spread** ≈ **9,4 $/bbl**
- OPEX raffinage : 4,2 $/bbl
- **Marge nette** ≈ **5,2 $/bbl**

### CAPEX (200 kbpd · Europe)

| Unité | CAPEX |
|-------|-------|
| Topping (CDU) | 450 M€ |
| Vacuum (VDU) | 180 M€ |
| FCC + Alky | 1,8 Md€ |
| Reformage + HDT | 950 M€ |
| Utilities & stockage | 1,2 Md€ |
| **TOTAL** | **~4,6 Md€** |

### Cibles marge

- **Point mort** : 3 $/bbl
- **Cible rentable** : 5–10 $/bbl
- **Exceptionnel** : > 15 $/bbl (crise géopolitique)

---

## 🛠️ Stack technique

| Technologie | Usage |
|-------------|-------|
| ![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white&style=flat-square) | Structure sémantique |
| ![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white&style=flat-square) | Design system (variables CSS) |
| ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=flat-square) | Logique & calculs (ES2020+) |
| ![Canvas](https://img.shields.io/badge/Canvas_API-0055A4?style=flat-square) | Graphiques 2D |

**✅ 0 npm · 0 build · 0 CDN · 0 framework · offline-first**

Palette tricolore française (`#0055A4` / `#FFFFFF` / `#EF4135`) · Responsive · WCAG AA · navigation clavier.

---

## 📁 Structure du projet

```
Petroleum-Refining-Console/
├── index.html          # Application mono-fichier (~60 KB)
├── README.md           # Ce fichier
├── LICENSE             # MIT
└── docs/
    ├── screenshot-overview.png
    ├── screenshot-tbp.png
    └── FORMULAS.md
```

---

## 📊 Statistiques

![LOC](https://img.shields.io/badge/LOC-~2300-0055A4?style=flat-square)
![Size](https://img.shields.io/badge/Size-~60_KB-6B4FBB?style=flat-square)
![Dependencies](https://img.shields.io/badge/Dependencies-0-1B7F4B?style=flat-square)
![Load](https://img.shields.io/badge/Load-<100_ms-1B7F4B?style=flat-square)
![Browsers](https://img.shields.io/badge/Browsers-Chrome_|_Firefox_|_Safari_|_Edge-0055A4?style=flat-square)

---

## 🤝 Contribuer

```bash
git checkout -b feature/ma-fonctionnalite
git commit -m "feat: ajout fonctionnalité X"
git push origin feature/ma-fonctionnalite
```

Conventions : [Conventional Commits](https://www.conventionalcommits.org/) · 2 espaces · camelCase.

[![Open Issue](https://img.shields.io/badge/Open_Issue-EF4135?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gunout/Petroleum-Refining-Console/issues/new)

---

## ⚠️ Avertissement

> **Simulateur pédagogique.** Modèles cinétiques (FCC 4-lump, HDS simplifié) et thermodynamiques (Antoine composés purs) simplifiés.  
> Usage industriel : **Aspen HYSYS**, **Aspen Plus**, **PRO/II**, **Spiral Suite**, **PIMS**.

---

## 📄 Licence MIT

Copyright (c) 2024 Petroleum Refining Console

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

---

<div align="center">

[![Star](https://img.shields.io/badge/⭐_Star_this_repo-yellow?style=for-the-badge&logo=github)](https://github.com/gunout/Petroleum-Refining-Console)

[⬆ Retour en haut](#-petroleum-refining-console)

</div>
