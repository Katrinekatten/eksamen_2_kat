# TEKNISK DOKUMENTATION – Dankort Øremærket Eksamen

## Kort om projektet

Dette projekt er udviklet i forbindelse med 2. semester eksamensprojekt på Multimediedesignuddannelsen ved Erhvervsakademi København.

Projektet tager udgangspunkt i kundecasen fra det digitale bureau 1508 og Dankort Øremærket. Formålet med projektet har været at udvikle en digital løsning målrettet unge mellem 18–28 år, som skal skabe større interesse for og efterspørgsel af Dankort.

Løsningen er udviklet med fokus på:

- Mobile-first design
- Responsivt webdesign
- Bæredygtighed
- UX/UI
- Dynamisk datahåndtering
- Moderne frontend-udvikling

Projektet er udviklet med Astro, HTML, CSS og JavaScript, hvor udvalgt indhold hentes dynamisk fra Supabase.

---

# Links

- Live site:  
[Indsæt Netlify link]

- GitHub Repository:  
https://github.com/DankortOeremaerket-EksamensProjekt/OeremaerketEksamen

- Figma:  
https://www.figma.com/design/iO7EkZnKBT3wp1p5xXSx4s/Tema-10--eksamen?node-id=0-1&p=f&t=lUUtlDHGzCWh8DFS-0

- Trello Board:  
https://trello.com/b/B6ZEmDdB/eksamen

---

# Gruppemedlemmer

- Ida Dam – idda0001@stud.ek.dk
- Katrine Madsen - kama0011@stud.ek.dk 
- Julie Stigsen - just0003@stud.ek.ek  
- Patricia Klindt Brokholm - patr1541@stud.ek.dk 

---

# Teknologier

Projektet er udviklet med:

- Astro
- HTML
- CSS
- JavaScript
- Supabase
- Git & GitHub
- Netlify
- Figma

---

# Projektstruktur

```bash
OEREMAERKETEKSAMEN/
├── public/
│   ├── fonts/
│   │   └── Raleway-VariableFont_wght.ttf
│   ├── video/
│   │   └── hero_index.mp4
│   ├── favicon.svg
│   └── DK_Logo_CMYK.svg
├── src/
│   ├── assets/
│   │   ├── dk_mobil.svg
│   │   ├── jumpdown.svg
│   │   ├── kort.svg
│   │   ├── mobil_step_baggrund.svg
│   │   ├── shield_mobil.svg
│   │   ├── shop_mobil.svg
│   │   ├── sti_mobil.svg
│   │   └── trees_mobil.svg
│   ├── components/
│   │   ├── Banner_read_more.astro
│   │   ├── Buttons_nav.astro
│   │   ├── Card_step.astro
│   │   ├── Donation_taeller.astro
│   │   ├── Footer.astro
│   │   ├── Header.astro
│   │   ├── Hero_video.astro
│   │   ├── Icons.astro
│   │   └── Overskrift_hero_index
│   │
│   ├── css/
│   │   ├── custom.css
│   │   └── general.css
│   │
│   ├── img/
│   │   ├── dankort_i_haand.webp
│   │   ├── girls_piggybacking.webp
│   │   ├── grassy_beach_sunset.webp
│   │   ├── loevfro_naturfond.webp #ER DENNE TAGET AF JESPER?#
│   │   ├── logon.webp
│   │   ├── sandy_beach_coastline.webp
│   │   ├── sandy_beach.webp
│   │   ├── sky_clouds.webp
│   │   ├── small_shop.webp
│   │   ├── surfer_girl.webp
│   │   └── udylf_detaljer.webp
│   │
│   ├── layouts/
│   │   └── Layout.astro
│   │
│   ├── lib/
│   │   └── supabase.js
│   │
│   ├── pages/
        └── productlist/
              └── [slug].astro
        ├── detail.astro
        ├── index.astro
        ├── spec.details.astro
        └── stepbystep.astro

```

---

# Filbeskrivelser

## Components

- **Button_nav.astro**  
  Komponent til intern navigation af undersiderne.

- **Card_step.astro**  
  Komponent med HTML og CSS til visning af indhold.

- **Footer.astro**  
  Footer-komponent som bruges globalt på alle sider.

- **Header.astro**  
  Header og navigation med responsivt design og JavaScript-funktionalitet.

- **Hero_video.astro**  
  Hero-sektion på forsiden.

- **Icons.astro**  
  Info banner med ikoner til forsiden.

- **Donation_taeller.astro**  
  Komponent til forsiden donations tæller.

- **Banner_read_more.astro**  
  Banner der fører videre til Naturfondens hjemmeside.

---

## Layouts

- **Layout.astro**  
  Global layout-fil hvor fonte, metadata og globale styles bliver importeret.

---

## Pages

- **index.astro**  
  Forsiden på hjemmesiden.

- **detail.astro**  
  Side med fokus på områder Dankorts donationer har støttet til.

- **spec.details.astro**  
  Informationsside om de specifikke områder.

- **stepbystep.astro**  
  Statisk side med fokus på at give overblik over hvordan målgruppen kan få et Dankort.

---

# Navngivning

Vi har navngivet filer, variabler og funktioner ud fra deres funktionalitet for at skabe et mere overskueligt og vedligeholdelsesvenligt projekt.

## Eksempel på variabler

```javascript
const scrollToSteps = document.getElementById("jump_down_button");
const stepsSection = document.getElementById("steps");
```

## Eksempel på funktioner

```javascript
if (burger && menu) {
    burger.addEventListener("click", () => {
      burger.classList.toggle("active");
      menu.classList.toggle("active");
    });
  }
```

Vi har benyttet camelCase i JavaScript for at skabe ensartethed og bedre læsbarhed i koden.

---

# Data og JSON-struktur

Projektet henter dynamisk indhold fra Supabase i JSON-format.

## Eksempel på datastruktur

```javascript
{
  "id": 1,
  "navn": "Storebælt Klint",
  "undertitel": "Forenet med naturen",
  "beskrivelse": "Hver gang du bruger dit Dankort, donerer vi 1 øre til Den Danske Naturfond...",
  "billede_url": "https://xxxx.supabase.co/storage/v1/object/public/billeder/storebaelt1.webp",
  "billede_url_2": "https://xxxx.supabase.co/storage/v1/object/public/billeder/storebaelt2.webp",
  "billede_url_3": "https://xxxx.supabase.co/storage/v1/object/public/billeder/storebaelt3.webp",
  "pin_x": 65.05,
  "pin_y": 74.32,
  "slug": "storebaelt_klint"
}
```

## Felter vi bruger

```javascript
navn        // Navn på naturområdet — vises som overskrift
undertitel  // Kort undertitel — vises på card og detaljeside
beskrivelse // Længere beskrivelse af naturområdet
billede_url  // URL til primært billede
billede_url_2 // URL til sekundært billede
billede_url_3 // URL til tertiært billede
pin_x       // Kortets X-koordinat i procent (bruges til placering af pin på Danmarkskortet)
pin_y       // Kortets Y-koordinat i procent (bruges til placering af pin på Danmarkskortet)
slug        // URL-venligt navn til dynamisk routing fx /productlist/storebaelt_klint
```

---

# Git og branches

Vi har anvendt GitHub som versionsstyring og dokumentation af udviklingsprocessen.

Ved at arbejde med branches kunne flere gruppemedlemmer udvikle funktioner samtidig uden konflikter i koden.

## Eksempler på branches

- index-rettelser
- indsaet-banner
- heroindex-kat
- buttons_mobile_fiks
- buttons_links

## Workflow

1. Oprette en branch til en feature eller opgave
2. Udvikle og teste funktionalitet
3. Committe ændringer
4. Pushe til GitHub
5. Merge til main når funktionaliteten virker stabilt

---

# Bæredygtighed

Vi har blandt andet arbejdet med:

- Mobile-first udvikling
- Lav page weight
- Komprimerede billeder
- Brug af `.svg` og `.webp`
- Genbrugelige komponenter
- Begrænset brug af tunge animationer og video
- Responsivt design for optimal performance

---

# Design og UX

Projektet er udviklet med fokus på:

- Brugervenlig navigation
- Moderne UI-design
- Responsivt layout
- Accessibility
- Visuel identitet der matcher Dankort Øremærkets brand

Der er arbejdet ud fra Double Diamond-processen med research, idéudvikling, prototyping og test.

---

# AI og udvikling

Generativ AI er blevet anvendt som støtteværktøj til blandt andet:

- Strukturering af dokumentation
- Kodehjælp
- Idéudvikling

Brugen af AI er dokumenteret i overensstemmelse med eksamenskravene.

---
---

# Mulige forbedringer

Hvis projektet skulle videreudvikles, kunne vi tilføje:

- Error handling og 404-side
- Flere animationer og microinteractions
- Udvidet accessibility
- Brugerlogin
- Samarbejdspartnere
- Darkmode

---

# Vores "nice to have"

Vi havde originalt et ønske om at skabe et Achievement system, for at gøre brugeres bidrag til Den Danske Naturfond tydeligere og mere håndholdt. Inspireret af PureGym.
Dette kunne vi desværre ikke udfører, da dette ville kræve brugerlogin.

# Eksamensinformation

Projektet er udarbejdet som en del af:

- 2. semester eksamen
- Multimediedesignuddannelsen
- Erhvervsakademi København
- F2026

Projektet er udviklet i teams og tager udgangspunkt i kundecasen fra 1508 og Dankort Øremærket.
