# HCBD — Prompt Claude Design
## Hugo Charlet Bureau de Design · Site one-page

---

## 1. DIRECTION ARTISTIQUE

### Palette HEX

| Rôle | Valeur | Usage |
|---|---|---|
| Background principal | `#F5F0EA` | Fond général (lin chaud) |
| Background secondaire | `#EDE7DC` | Sections alternées, cards |
| Texte principal | `#1A1714` | Corps, titres |
| Texte secondaire | `#6B5F54` | Légendes, sous-titres, métadonnées |
| Accent terracotta | `#B85C38` | CTA, soulignements, hover, détails |
| Accent rouille clair | `#D4795A` | Dégradé accent, hover secondaire |
| Blanc cassé | `#FAF7F3` | Backgrounds de cards flottantes |
| Séparateur | `#D6CEC4` | Lignes, bordures subtiles |

### Typographie

- **Logo** : Hanken Grotesk 800 · 22px (HCBD) + 500 · 15px (contract furniture design)
- **Titres de sections (H2)** : Hanken Grotesk 700 · uppercase · letter-spacing: 0.08em
- **Titres secondaires (H3)** : Hanken Grotesk 600
- **Corps de texte** : Hanken Grotesk 400 · 16–17px · line-height 1.7
- **Annotations, étiquettes, numéros, détails techniques** : IBM Plex Mono italic · 12–13px · couleur `#6B5F54`
- **Citations / "En résumé"** : IBM Plex Mono italic · 15px · couleur accent terracotta

### Ambiance générale

Craft & technique. Ambiance studio de design industriel européen : sobre, structuré, avec une chaleur artisanale dans les matières (lin, béton clair). Pas de froideur corporate, pas d'exubérance créative. Le site respire la compétence tranquille. Les accents terracotta et les annotations mono italic rappellent les cahiers de design et les fichiers techniques. Texture de fond très subtile (grain papier 3–4% d'opacité).

---

## 2. STRUCTURE SECTION PAR SECTION

### NAV — Navigation sticky

- Fond : `#F5F0EA` avec `backdrop-filter: blur(12px)` au scroll
- Gauche : Logo texte **HCBD** (Hanken 800) + *contract furniture design* (Hanken 500) sur deux lignes
- Centre : Liens de navigation · `WHO WE ARE · EXPERTISE · SERVICES · PROJECTS · CONTACT`
  - Style : Hanken 500 · 13px · uppercase · letter-spacing 0.1em
  - Hover : soulignement terracotta animé (width 0→100%, transition 200ms)
- Droite : Numéro de téléphone cliquable `tel:` · IBM Plex Mono italic · couleur accent
- Séparateur bas : ligne `1px solid #D6CEC4` qui apparaît au scroll (pas visible en top)

---

### SECTION 01 — HERO

**Concept** : Grid de projets pro en hero — impact visuel immédiat.

- Fond : `#F5F0EA`
- Layout : Grille asymétrique 3 colonnes × 2 rangées, hauteur 100vh
  - Cellule large gauche (col 1–2, row 1) : `pro-project-helena-ambiance-1` (vue plongée dossier rouge) — image pleine, aucune légende
  - Cellule haute droite (col 3, row 1) : `pro-project-helena-packshot-2` (face légèrement angled)
  - Cellule basse droite (col 3, row 2) : `pro-project-porada-amarantha-1`
  - Petite cellule bas gauche (col 1, row 2) : `pro-project-fiam-vertigo-1`
  - Cellule centrale bas (col 2, row 2) : **Bloc texte hero**
- **Bloc texte hero** (dans la grille) :
  - Annotation IBM Plex Mono italic · terracotta : *— Bordeaux, Europe*
  - Titre Hanken 700 · grand : **"Design on demand. Zero royalties."**
  - Sous-titre Hanken 400 · 16px · `#6B5F54` : *3D modeling · Visualization · Contract furniture*
- Images : `object-fit: cover`, légère transition `scale(1.02)` au hover (300ms ease), pas de légende visible
- Numérotation IBM Plex Mono des cellules en overlay discret : `01 / 02 / 03...` · 11px · `#6B5F54` coin bas gauche de chaque image

---

### SECTION 02 — WHO ARE WE?

- Fond : `#EDE7DC`
- Layout : Split 50/50
  - Gauche : `profile-img-in-office` (16:9, crop pour remplir) avec un cadre légèrement offsetté (2px border `#D6CEC4`)
  - Droite : Contenu texte
    - Annotation IBM Plex Mono italic · terracotta · small : *— Who are we?*
    - Titre H2 : **"HCBD"**
    - Corps : texte fourni (HMBD is a design agency...)
    - Détail IBM Plex Mono · bas : *Est. 2026 · Bordeaux*
- Texture grain subtile sur fond

---

### SECTION 03 — EXPERTISE

- Fond : `#FAF7F3`
- Layout : 2 colonnes
  - Colonne gauche : Texte expertise (With 10 years of experience...)
    - Annotation IBM Plex Mono italic · `— Expertise`
    - Titre H2
    - Corps Hanken 400
    - Liste de logiciels en IBM Plex Mono : `Rhino · Keyshot · Blender · V-Ray · AI tools`
  - Colonne droite : **Scroll horizontal de captures CAD**
    - Rail scrollable (overflow-x: auto, snap) contenant 5–6 images `cad-modeling-skill-*`
    - Chaque image : fond `#1A1714` (screenshots Rhino sont naturellement sombres), label IBM Plex Mono italic en bas : *— Rhinoceros 3D · Surface modeling*
    - Indicateur de scroll discret : `→` animé

---

### SECTION 04 — IN SUMMARY (Services)

- Fond : `#F5F0EA`
- Layout : 6 points en grille 2×3, chaque item dans un bloc card `#FAF7F3`
- Chaque card :
  - Numéro IBM Plex Mono terracotta : `01`
  - Titre Hanken 600 : intitulé du service
  - Corps Hanken 400 : description courte
  - Bordure bas `2px solid #D6CEC4` qui vire terracotta au hover
- Fade-in scroll-triggered décalé (`animation-delay` par card, 100ms d'écart)
- Bloc citation en bas de section : IBM Plex Mono italic · terracotta · centré :
  *"Whether you have small modeling projects or require complete furniture modeling, we are here to help."*

---

### SECTION 05 — OUR METHOD

- Fond : `#EDE7DC`
- Layout : Full-width avec étapes numérotées en timeline horizontale (desktop) / verticale (mobile)
  - Chaque étape : numéro IBM Plex Mono `01 →`, titre Hanken 600, description Hanken 400
  - Étapes : Écoute → Visite atelier → Conception → Plans & fichiers 3D → Modifications
- Arrière-plan : photo `profile-img-in-factory` en position right, grande, opacity 15% (texture ambiance)

---

### SECTION 06 — PROJECTS · PRO

- Fond : `#1A1714` (section sombre pour contraste maximum avec les packshots Helena)
- Annotation IBM Plex Mono italic · blanc 50% : *— Professional projects*
- Titre H2 : **"PRODUCTION"** · Hanken 700 · blanc
- Sous-titre : *Furniture currently in production* · Hanken 400 · `#6B5F54`
- **Rail scroll horizontal** :
  - Helena série : `helena-ambiance-1`, `helena-packshot-1`, `helena-packshot-2`, `helena-packshot-3`, `helena-in-factory-1`
  - Séparateur vertical discret
  - Porada : `porada-amarantha-1`, `porada-amphora-1`, `porada-amphora-2`
  - Séparateur
  - Autres : `fiam-vertigo-1`, `produzioneprivata-bachetta-1`
- Images : hauteur fixe 70vh, largeur auto, `object-fit: cover`, sans légende sauf label IBM Plex Mono italic discret en bas : *— Helena · CMcadeiras* / *— Porada · Amarantha*
- Au clic : l'image passe en `position: fixed` plein écran avec fond noir, fermeture par clic ou `Esc`

---

### SECTION 07 — PROJECTS · 3D SKILLS

- Fond : `#F5F0EA`
- Annotation IBM Plex Mono italic · terracotta : *— 3D & Rendering skills*
- Titre H2 : **"3D"**
- **Deux rails scroll horizontal distincts** :
  1. **CAD Modeling** · fond sombre par cellule (screenshots Rhino) · label IBM Plex Mono : *Surface modeling · Rhinoceros 3D*
  2. **Rendering** · images claires/rendus · label IBM Plex Mono : *Photorealistic rendering · Blender / AI*
- Chaque rail : `scroll-snap-type: x mandatory`, indicateur `→` animé à droite

---

### SECTION 08 — WHY CHOOSE US?

- Fond : `#EDE7DC`
- Layout : liste de 9 arguments en grille 3×3, sans cards — juste typographie
  - Numéro IBM Plex Mono terracotta : `—01`
  - Titre Hanken 600
  - Ligne séparatrice `1px #D6CEC4`
- Photo `profile-kneeling-behind-pixa-chair` en fond partiel droit, opacity 8%, `object-fit: cover`

---

### SECTION 09 — CONTACT (Footer intégré)

- Fond : `#1A1714`
- Layout : 4 colonnes
  1. **Logo** : HCBD blanc + *contract furniture design* · Réseaux : Instagram `@hugocharletb` · lien vers portfolio PDF
  2. **Adresse** : IBM Plex Mono · 8 rue du commandant arnould · 33000 Bordeaux
  3. **Formulaire** : Nom / Email / Message / Bouton `SEND` · bouton : fond terracotta, texte blanc, border-radius 0 (carré), hover fond rouille clair
  4. **Contact direct** : Téléphone en IBM Plex Mono italic · Mention *— Remote across Europe*
- Ligne de copyright bas : IBM Plex Mono · 11px · `#6B5F54` · *© 2026 HCBD · Hugo Charlet Bureau de Design*

---

## 3. INTERACTIONS & ANIMATIONS

| Élément | Interaction |
|---|---|
| Nav links | Soulignement terracotta width 0→100% · 200ms ease |
| Images hero | `scale(1.02)` au hover · 300ms ease |
| Cards services | Bordure bas vire terracotta au hover |
| Scroll sections | `fade-in + translateY(20px → 0)` · staggered 100ms delay par élément |
| Rails horizontaux | `scroll-snap`, curseur `grab` / `grabbing` |
| Bouton SEND | Fond terracotta → rouille clair · transition 200ms |
| Image pro au clic | Expand plein écran `position:fixed` fond `#1A1714` · fade-in 300ms |
| Nav au scroll | Backdrop-blur + séparateur bas apparaît |

---

## 4. STYLE PHOTO UNIFIÉ (pour préparation des visuels)

**Ambiance** : Fond neutre clair (lin, béton clair, blanc cassé `#F5F0EA`)  
**Éclairage** : Naturel latéral diffus, pas de flash, légèrement sous-exposé  
**Composition** : Centré, épuré, beaucoup d'air autour du sujet  
**Mood** : Studio de design européen — sérieux, artisanal, premium sans ostentation  
**Traitement** : Légère désaturation globale, tons chauds dans les ombres  
**À éviter** : Surexposition, tons froids/bleutés, arrière-plans chargés, effet HDR

---

## 5. À ÉVITER ABSOLUMENT

- ❌ Violet / bleu Klein / dégradés flashy — hors positionnement
- ❌ Polices Inter, Roboto, ou system-ui
- ❌ Cards avec `border-radius` élevé (> 4px) — trop soft / SaaS
- ❌ Icônes génériques (emoji, FontAwesome flat)
- ❌ Sections trop texte-denses sans respiration
- ❌ Animations de parallaxe agressive
- ❌ Layout 100% symétrique / corporate
- ❌ Fond blanc pur (`#FFFFFF`) — toujours utiliser les tons lin
- ❌ CTA en forme de bouton pill (trop moderne / startup)
- ❌ Lightbox modale — les images s'affichent dans la section ou en plein écran natif
- ❌ Tout ce qui ressemble à un site d'agence digitale générique
