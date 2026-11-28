# Lashable – Ontwerpplan website (Figma)

> Bron: Instagram-profiel @lashable.nl (screenshot). Instagram en Salonized konden niet automatisch worden uitgelezen (rate limit / geblokkeerd). Prijzen, adressen en Salonized-gegevens moeten dus nog bij de klant worden opgevraagd.

---

## 1. Wat we weten van de klant

| Onderdeel | Gegevens |
|---|---|
| Naam / tagline | **Lashable** – *The perfect lashes and brows* |
| Locaties | **Almere** en **Nieuwegein** |
| Positionering | "Certified", beauty-ondernemer(s), persoonlijk en warm (eigenaren zijn veel in beeld) |
| Behandelingen | Lashlift · Lash extensions · Pink Glow / Microneedling · Henna Brows · Brow Lamination · PMU (wenkbrauwen, lippen, eyeliner) |
| Instagram-highlights | Prijslijst · PMU brows · Pink Glow · Lashes · Brows |
| Boekingen | Salonized |
| Bereik | 742 volgers, 214 berichten → het meeste verkeer komt via Instagram, dus **mobiel eerst** |

**Huisstijl zoals nu zichtbaar:** zwart-wit logo met een getekend oog en wimpers, het woord "Lashable" in een vette schreefloze letter, de tagline in een dunne cursieve schreefletter. De highlight-iconen zijn zacht roze/blush met illustraties in lijnstijl. Op de foto's staan warme, feestelijke scènes van de eigenaren, plus close-ups van wimpers en wenkbrauwen.

---

## 2. Sitemap

```
Home
├── Behandelingen (overzicht)
│   ├── Lashlift
│   ├── Lash extensions
│   ├── Brow lamination
│   ├── Henna brows
│   ├── Pink Glow & Microneedling
│   └── Permanente make-up (PMU, overzicht)
│       ├── PMU wenkbrauwen
│       ├── PMU lippen
│       └── PMU eyeliner
├── Tarieven
├── Impressie
├── Over ons            (aanbevolen)
├── Contact & locaties  (Almere / Nieuwegein)
└── [Boek nu]           → Salonized (widget/overlay, geen eigen pagina)
Footer: privacybeleid, algemene voorwaarden / annuleringsbeleid
```

**Navigatie (desktop):** Logo · Behandelingen (dropdown/mega-menu met foto per behandeling) · Tarieven · Impressie · Over ons · Contact · **[Boek nu]**
**Navigatie (mobiel):** Logo · hamburger + een vaste knop "Boek nu" onderin het scherm (sticky)

---

## 3. Integratie met Salonized

- Een **"Boek nu"-knop** op elke pagina (in de header, na elk prijsblok en sticky op mobiel) opent de Salonized-boekingswidget als overlay. Zo blijft de bezoeker op de site.
- **Twee locaties:** laat de bezoeker eerst een vestiging kiezen. Dat kan in Salonized zelf (als beide vestigingen in één account staan) of met een kleine keuzemodal in het ontwerp: "Waar wil je boeken? Almere / Nieuwegein".
- **Behandelingspagina's:** nagaan of Salonized een directe link naar een specifieke dienst ondersteunt. Zo ja, dan opent "Boek deze behandeling" meteen de juiste dienst. Zo nee, dan opent de algemene widget.
- Reviews van Salonized en/of Google gebruiken als social proof (eerst nagaan wat beschikbaar is).
- In Figma de knop als component met de varianten *primary / secondary / sticky-mobile* en de overlay als aparte frame voor het prototype (een mock van de widget).

---

## 4. Opbouw van het Figma-bestand

| Figma-pagina | Inhoud |
|---|---|
| 0 · Cover | Projectnaam, versie, status |
| 1 · Moodboard | Instagram-beelden, referentiesites, stijlrichting |
| 2 · Foundations | Kleuren, typografie, grid, spacing, schaduwen en radius als **variabelen/styles** |
| 3 · Components | Alle bouwstenen met varianten (zie §6) |
| 4 · Wireframes | Lo-fi, grijs, voor akkoord op structuur |
| 5 · Design – Mobiel (390) | Hi-fi, wordt als eerste ontworpen |
| 6 · Design – Desktop (1440) | Hi-fi |
| 7 · Prototype | Klikbare flow: Home → Behandeling → Boek nu (overlay) / Tarieven / Impressie |
| 8 · Handoff | Notities voor development, assets, Salonized-specificaties |

**Grid:** desktop 12 kolommen, max. 1200 px content, gutter 24 · mobiel 4 kolommen, marge 20. Spacingschaal in stappen van 8 (8/16/24/32/48/64/96/128).

---

## 5. Stijlrichting (voorstel)

**Gevoel:** luxe maar toegankelijk, zacht en vrouwelijk, veel witruimte en grote close-up-foto's.

| Token | Voorstel | Gebruik |
|---|---|---|
| Ink | `#141414` | Tekst, logo, primaire knop |
| Ivory | `#FBF8F6` | Achtergrond |
| Blush | `#F4E1DE` | Sectie-achtergronden, kaarten |
| Rose | `#D9A3A9` | Accenten, lijnen, iconen |
| Glow | `#E0408F` | Spaarzaam, alleen voor de Pink Glow-pagina en badges |
| Forest | `#1F3A2E` | **Tertiaire (ondersteunende) kleur**: detailvlakken zoals het PMU-vlak en het boekblok |

*Rolverdeling: primair = blush/rose (merk), secundair = ink (tekst, knoppen), tertiair = forest (detail- en accentvlakken).*
| Grey 600 | `#6B6461` | Secundaire tekst |

**Typografie**
- **Gekozen: [Ysabeau](https://fonts.google.com/specimen/Ysabeau)**, één familie (Google Fonts, OFL).
  - Koppen: *Ysabeau* Bold, in lijn met het vette woordmerk van het logo; krappe letterafstand (−1 tot −3%).
  - Tekst, knoppen en prijzen: *Ysabeau Office*, de variant met rechte cijfers (die staan netjes onder elkaar in de prijslijst).
- Waarom: een schreefloze letter op een Garamond-skelet. Fijne, taps toelopende lijnen (net als een wimper) en een verfijnd karakter, zonder in de "zachte serif = premium"-valkuil te stappen. Weinig gebruikt (Google Fonts populariteit #1178), dus niet de standaardlook van gegenereerde sites.
- Afgevallen: Cormorant Garamond + Manrope (de AI-standaardcombinatie), Funnel Display (te technisch), Bricolage Grotesque (veel gebruikt), Hanken Grotesk Light (te neutraal). Het vergelijkingsbord staat op de Figma-pagina *2 · Foundations*.
- Regels: geen cursieve accentwoorden in koppen, geen kleine labels in hoofdletters met extra letterafstand, maximaal vijf zichtbare groottes per pagina.
- Schaal: Display 72/76 · H1 60/64 · H2 44/48 · H3 28/34 · body 17/27 · groot 19/30 · klein 15/22 (mobiel: H1 44, H2 32, H3 24).

**Beeld:** afgeronde of boogvormige fotokaders (een verwijzing naar de ooglijn), fijne lijnillustraties van een oog, wimpers en wenkbrauw (in de stijl van de highlight-iconen) als iconen per behandeling.

> Er komen 2 style tiles voor de klant (bijv. *"Soft Blush"* en *"Black Luxe"*). Na de keuze werken we die uit tot een hi-fi ontwerp.

---

## 6. Componenten

- **Header / navigatie** – desktop, mobiel, mega-menu Behandelingen
- **Button** – primary (zwart), secondary (outline), tekstlink, sticky "Boek nu" (mobiel)
- **Behandelingskaart** – foto, naam, korte beschrijving, "vanaf €…", duur → klikbaar naar de detailpagina
- **Prijsrij** – behandeling · duur · prijs · (optioneel) boekknop; variant met subregels (bijv. refill 2/3/4 weken)
- **USP-strip** – Certified · 2 locaties · persoonlijke aandacht · natuurlijk resultaat
- **Stappenblok** – "Zo verloopt je behandeling" (1-2-3-4)
- **Voor/na-slider**
- **FAQ-accordion**
- **Reviewkaart / carrousel**
- **Locatiekaart** – adres, openingstijden, kaart, knop "Boek in Almere / Nieuwegein"
- **Galerij-tegel + lightbox**, filterchips
- **Instagram-feedblok**
- **CTA-banner** – "Klaar voor perfecte lashes & brows?" + Boek nu
- **Footer**

Alles opbouwen met **Auto Layout** en variabelen, zodat responsive varianten en hergebruik in alle templates eenvoudig zijn.

---

## 7. Pagina's in detail

### 7.1 Home – zwaartepunt op de behandelingen
1. **Hero**: grote close-up (wimpers/wenkbrauwen), H1 *"The perfect lashes and brows"*, subregel "in Almere & Nieuwegein", knoppen [Boek nu] en [Bekijk behandelingen]
2. **Boekbalk**: studio (Almere/Nieuwegein) + behandeling + [Bekijk beschikbare tijden] → opent Salonized met die keuze
3. **USP-strip**
4. **Behandelingen – slider** (zoals La Diva): kop + intro + pijlknoppen links, rechts een horizontaal scrollende rij van 6 kaarten (foto, categorie, naam, korte tekst, duur/prijs) die over de rand doorloopt. Mobiel: swipe met stippen. **Dit is het belangrijkste blok van de pagina**: elke kaart linkt naar de detailpagina; "Bekijk alle behandelingen" gaat naar het overzicht (daar wel een grid)
5. **Uitgelicht – PMU**: foto + tekst op een vlak in bosgroen (`#1F3A2E`, tertiaire kleur)
6. **De gezichten achter Lashable**: de twee eigenaren met portret, naam en studio
7. **Review**: één grote review naast een grote foto (in plaats van een rij kaarten)
8. **Locaties**: twee kaarten
9. **Instagram**: strook met 6 posts + [Volg @lashable.nl]
10. **Boekblok** (bosgroen) met dezelfde keuzevelden als de boekbalk. Het blok ligt op de naad tussen een wit vlak (boven, met ruime marge na de Instagram-foto's) en een lichtroze vlak (onder) + footer

*Overgenomen uit de La Diva-referentie: boekbalk, kleurvlakken, eigenaren, grote review, Instagram-strook, boekblok onderaan. Bewust niet overgenomen: scriptaccenten, labels boven koppen, carrousels voor behandelingen, perslogo's, blog.*

### 7.2 Behandelingen (overzicht)
Intro, daarna per categorie (**Lashes · Brows · Skin · Permanente make-up**) de behandelingskaarten. Filterchips bovenaan om snel naar een categorie te springen.

### 7.3 Behandelingspagina (één template voor alle 9 pagina's)
1. Breadcrumb (Behandelingen › Lashes › Lashlift)
2. **Hero**: titel, één zin over het resultaat, kerngegevens in chips (**duur · houdbaarheid · vanaf-prijs**), [Boek deze behandeling]
3. **Wat is het?** Uitleg in tekst met een beeld ernaast
4. **Voor wie is het geschikt?**
5. **Het resultaat**: voor/na-slider en galerij
6. **Zo verloopt je afspraak**: stappenblok
7. **Prijs-box**: varianten (bijv. lash extensions: classic / volume / refill), met een boekknop per variant
8. **Nazorg**: tips
9. **Contra-indicaties / goed om te weten**, vooral bij PMU en microneedling
10. **FAQ**
11. **Bekijk ook**: 2 à 3 gerelateerde behandelingen (cross-sell, bijv. lashlift ↔ brow lamination)
12. CTA-banner

*Variaties binnen het template:* de PMU-overzichtspagina gebruikt de kaarten voor wenkbrauwen, lippen en eyeliner in plaats van één behandeling. Bij PMU komen er extra blokken bij voor het **intakegesprek** en de **touch-up na 6–8 weken**. De Pink Glow-pagina krijgt het Glow-accent.

### 7.4 Tarieven
- Intro + noot "prijzen gelden voor beide locaties" (bevestigen bij de klant)
- **Ankernavigatie** per categorie (sticky op mobiel)
- Per categorie de prijsrijen met duur en prijs, refills en touch-ups als subregels
- Blok met kortingen of pakketten (indien van toepassing)
- **Annuleringsbeleid / aanbetaling** (vaak van belang bij PMU)
- Boekknop per categorie + CTA onderaan
- Elke behandelingsnaam linkt naar de bijbehorende detailpagina

### 7.5 Impressie
- Masonry-galerij met **filterchips** (Alles · Lashes · Brows · PMU · Pink Glow · Salon)
- Lightbox met bijschrift en de link "Bekijk deze behandeling"
- Optioneel een paar korte video's/reels
- Instagram-blok "Volg @lashable.nl" + CTA

### 7.6 Over ons / Contact & locaties (ondersteunend)
- Het verhaal, de eigenaren, certificaten en salonfoto's
- Twee locatiekaarten met kaart, adres, openingstijden en een eigen boekknop per locatie, plus WhatsApp en Instagram

---

## 8. SEO en conversie (meenemen in het ontwerp)
- Eén pagina per behandeling, met lokale zoektermen in H1/H2 en meta (bijv. *"Lashlift in Almere en Nieuwegein"*, *"PMU wenkbrauwen Almere"*). Later kunnen er eventueel aparte locatiepagina's bij.
- Op elke pagina binnen één scroll een boekknop. Op mobiel blijft de sticky "Boek nu"-knop altijd zichtbaar.
- Vertrouwen opbouwen met reviews, certificaten, echte voor/na-foto's en de gezichten van de eigenaren.
- Ruimte voor een LocalBusiness/BeautySalon-schema en Google-reviews (voor development).

---

## 9. Op te vragen bij de klant
- [ ] Actuele **prijslijst** (uit de highlight "Prijslijst") inclusief duur, refills en touch-ups
- [ ] **Adressen en openingstijden** van Almere en Nieuwegein; gelden dezelfde behandelingen en prijzen op beide locaties?
- [ ] **Salonized**: toegang of de widgetcode, één account of twee, en of directe links per dienst mogelijk zijn
- [ ] Foto's in hoge resolutie: behandelingen, salon, eigenaren, en voor/na-foto's **met toestemming van de klanten**
- [ ] Teksten: uitleg en nazorg per behandeling, contra-indicaties, annuleringsbeleid
- [ ] Certificaten en opleidingen
- [ ] Reviews (Google of Salonized)
- [ ] Logobestanden in vector (SVG/AI); wil de klant het logo houden of mag het worden verfijnd?
- [ ] Domein lashable.nl: is dit al in bezit?

---

## 10. Planning (fases)

| Fase | Oplevering | Akkoord klant |
|---|---|---|
| 1. Intake & content | Ingevulde checklist (§9), sitemap definitief | ✔ |
| 2. Wireframes | Lo-fi Home, Behandelingspagina, Tarieven, Impressie (mobiel + desktop) | ✔ |
| 3. Style tiles | 2 stijlrichtingen, keuze door de klant | ✔ |
| 4. Hi-fi design | Componenten + alle templates, eerst mobiel, dan desktop | – |
| 5. Prototype & presentatie | Klikbare flow incl. Salonized-overlay | ✔ (feedbackronde 1) |
| 6. Verwerking & handoff | Feedback verwerkt (2 rondes), handoff-pagina voor development | ✔ |

**Te ontwerpen schermen:** Home, Behandelingen-overzicht, Behandelingspagina (template + PMU-variant), Tarieven, Impressie, Over ons, Contact, boekingsoverlay. Elk scherm mobiel en desktop, dus ±16 frames.
