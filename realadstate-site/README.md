# Real Adstate — Website

Statische website voor [realadstate.nl](https://realadstate.nl) — gehost op Vercel, beheerd via GitHub.

## 📁 Structuur

```
realadstate-site/
├── index.html                        # Homepage
├── vercel.json                       # Routing & caching config
├── assets/
│   └── css/
│       └── global.css               # Gedeelde CSS-variabelen + fonts
├── pages/
│   ├── makelaardiensten.html        # /makelaars/diensten
│   ├── vastgoedontwikkelaars.html   # /vastgoedontwikkelaars
│   ├── cases.html                   # /cases
│   └── case-template.html          # /cases/[naam] (handmatig dupliceren)
└── embeds/
    ├── quiz.html                    # Kantoor-check quiz (standalone)
    └── explainer.html              # 30-sec animated explainer
```

## 🚀 Deployment

Deze repo is gekoppeld aan Vercel. Elke push naar `main` deployt automatisch.

**Live URL:** https://realadstate.nl  
**Preview URL:** https://realadstate.vercel.app

## ✏️ Een pagina aanpassen

1. Open het HTML-bestand in een teksteditor (VS Code aanbevolen)
2. Pas de tekst, kleuren of structuur aan
3. Commit en push naar `main`:
   ```bash
   git add .
   git commit -m "Aanpassing: [omschrijving]"
   git push
   ```
4. Vercel deployt automatisch — live binnen ~30 seconden

## ➕ Nieuwe case toevoegen

1. Dupliceer `pages/case-template.html`
2. Hernoem naar `pages/cases/[projectnaam].html`
3. Vul alle `[[ INVULLEN ]]` plekken in
4. Voeg een kaart toe aan `pages/cases.html` (kopieer een bestaand `.case-card` blok)
5. Push naar `main`

## 🎨 Kleuren & stijl

| Token | Waarde | Gebruik |
|---|---|---|
| `--navy` | `#0F2043` | Achtergronden, tekst |
| `--green` | `#69C28E` | Accenten, CTA's |
| `--green2` | `#4aab76` | Hover states |
| `--muted` | `#6B7A99` | Subtekst |
| `--border` | `#E2E8F0` | Borders |

Lettertypen: **DM Serif Display** (koppen) · **DM Sans** (body) · **Space Mono** (labels)

## 🔌 Embeds

De quiz en explainer in `/embeds/` zijn zelfstandige HTML-bestanden.  
Ze worden inline opgenomen in pagina's via een `<iframe>` of direct als HTML-blok.

## 📞 Contact

Ruben — ruben@realadstate.nl
