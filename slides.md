---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: ./background.webp
# some information about your slides (markdown enabled)
title: PEFC-EUDR-RED Datenbankapplikation
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: fade-out
# enable Comark Syntax: https://comark.dev/syntax/markdown
comark: true
# duration of the presentation
duration: 15min
---

# PEFC-EUDR-RED Datenbankapplikation

Webbasiertes System zur digitalen Verwaltung von PEFC-Teilnehmern, EUDR-Integration und RED-Selbsterklärung

<img src="./w3geo-logo.png" class="abs-br m-8 h-12" style="filter: brightness(3)" />
<img src="./pefc-logo.png" class="abs-bl m-8 h-12" />

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: center
---

# w3geo GmbH

- Seit 2015 als w3geo
- Klassische Software- und Datenbankentwicklung + Geospatial Solutions (Geo-Informatik)
- Wichtigster Anspruch für jedes Projekt: Dem Benutzer eine möglichst perfekte Umsetzung zu bieten
  - UX = User-Experience ganz oben auf der Prioritätenliste.


<!-- AP -->

---
layout: center
---

# Umsetzungskonzept 1 / 4

- Rollenabhängige Benutzeroberfläche im Client, umgesetzt ausschließlich mit Open Source Frameworks (z.B. VUE)
  - Erfahrung aus div. Projekten, Beispiel ISTMobil:
    - *Große Datenbank mit tausenen Kunden, Verkehrsunternehmern, Disponenten, Administratoren usw.*
    - *Die Oberfläche wird rollenabhängig dargestellt*
    - *Für bestimmte Rollen responsive Versionen, z.B. Fahrzeug-Applikation*

<div class="mt-4 flex flex-wrap justify-center gap-4">
  <img src="./istmobil03.jpg" class="h-52" />
  <img src="./istmobil07.jpg" class="h-52" />
</div>

---
layout: center
---

# Umsetzungskonzept 2 / 4

- Responsive Web-Formulare anstatt Excel-Sheets
 - Offline fähig (z.B. im Wald)
 - Erfahrung aus div. Projekten, z.B. GZA, eStrab, sofisch

<div class="mt-4 flex flex-wrap justify-center gap-4">
  <img src="./gza03.jpg" class="h-52" />
  <img src="./sofisch06.jpg" class="h-52" />
</div>


---
layout: center
---

# Umsetzungskonzept 3 / 4

- Relationale Datenbank, geeignet für große Datenmengen und performative Suchen (z.B. PostgreSQL)
- Logging sämtlicher relevanter Ereignisse in Form eines sg. "Activity Trails"
  - bietet auch Verknüpfung zu DB-Entitäten / anderen Ereignissen
- Audit Tools für Auswertungen / Controlling
  - *Beispiel ISTMobil - Fahrzeug-Controlling*

<div class="mt-4 flex flex-wrap justify-center gap-4">
  <img src="./istmobil10.jpg" class="h-52" />
  <img src="./istmobil11.jpg" class="h-52" />
</div>


---
layout: center
---

# Umsetzungskonzept 4 / 4

- Hosting in skalierbarer, performativer Server-Infrastruktur
  - Beispiel ISTMobil:
    - *hochverfügbarer Server 24/7*
    - *DSGVO (Kundendaten)*

<!-- AP -->

---
layout: section
---

# Schlaglichter

<ph-flashlight class="text-7xl text-amber-300 mx-auto mt-2 block" />

<!-- AH -->

---
layout: center
---

# Identity Provider, Authentifizierung

- Bereits Erfahrungen mit USP, eAMA Partner-Login, ID Austria
- Kenntnis auch der zugehörigen Antragsprozesse

<img src="./idp.png" class="mt-4 h-76">

---
layout: center
---

# Verknüpfen von Accounts und Duplikatvermeidung
- Eindeutige Attribute (LFBIS-Nummer) ermöglichen Account-Verknüpfung ohne Zutun des Benutzers
- Mitarbeiterdelegierung zum gemeinsamen Zugriff auf den gleichen Account (USP)
- Gemeinsame Eigenschaften (LFBIS-Nummer, Adresse) ermöglichen **Duplikatvermeidung** in der Datenbank

<div class="mt-4 text-sm" style="display:grid; grid-template-columns:2fr 1fr 1fr 2fr; gap:8px;">
  <div style="grid-column:1/4" class="bg-green-100 text-green-700 font-bold text-xs text-center rounded py-1 tracking-wide">UNTERNEHMENSBEZOGEN</div>
  <div style="grid-column:4/5" class="bg-blue-100 text-blue-700 font-bold text-xs text-center rounded py-1 tracking-wide">PERSONENBEZOGEN</div>

  <div style="grid-column:1/2" class="bg-green-50 border border-green-300 rounded-lg p-3 flex flex-col gap-2">
    <div class="font-bold text-green-700 text-base text-center">eAMA Partner-Login</div>
  </div>
  <div style="grid-column:2/4" class="bg-green-50 border border-green-300 rounded-lg p-3 flex flex-col gap-2">
    <div class="font-bold text-green-700 text-base text-center">Unternehmensserviceportal</div>
    <div class="bg-green-700 text-white text-xs rounded-full text-center py-1 px-2">Mitarbeiterdelegierung</div>
  </div>
  <div style="grid-column:4/5" class="bg-blue-50 border border-blue-300 rounded-lg p-3">
    <div class="font-bold text-blue-700 text-base text-center">ID Austria</div>
  </div>

  <div style="grid-column:1/3" class="bg-green-100 text-green-800 text-xs rounded text-center py-1 px-2">Land- und forstwirtschaftliche Betriebe mit LFBIS Nummer</div>
  <div style="grid-column:3/4" class="bg-slate-100 text-slate-500 text-xs rounded text-center py-1 px-2 border border-slate-200">Andere Betriebe (CoC)</div>
  <div style="grid-column:4" class="bg-blue-100 text-blue-700 text-xs rounded text-center py-1 px-2 border border-blue-200">Natürliche Personen</div>

  <div style="grid-column:1/5" class="bg-slate-50 border border-slate-200 rounded-lg py-2 px-4 text-center text-xs">
    <span class="text-slate-500">Adressen aus dem amtlichen Adressregister</span>
  </div>
</div>



<!-- AH -->

---
layout: center
---

# Altdaten-Übernahme Var. 1
## via Alt-Login

<!-- AH -->

---
layout: two-cols
---

# EUDR

- Bereits Erfahrung mit EUDR durch Entwicklung des **BMLUK EUDR-Meldung**-Tools
- Kenntnis der Prozesse rund um EUDR-Sorgfaltserklärungen und Referenznummern
- Technisches Know-how zur Anbindung an die **TRACES**-Datenbank

::right::

```mermaid {theme: 'neutral', scale: 0.65}
flowchart TD
    subgraph std ["Standard-Prozess"]
        direction TB
        A["App erstellt Sorgfaltserklärung (Entwurf)"] --> B["Nutzer bestätigt ✓"]
        B --> C(["PEFC: bevollmächtigter Vertreter aller Mitglieder"])
    end
    subgraph alt ["Alternativ"]
        direction TB
        D["Nutzer gibt bestehende Referenznummer ein"]
    end
    C --> DB[(Referenznummer in Datenbank)]
    D --> DB
    DB -->|"Detailabfragen"| TR[(TRACES-Datenbank)]

    classDef green fill:#15803d,color:white,stroke:#15803d
    classDef pill fill:#16a34a,color:white,stroke:#16a34a
    classDef blue fill:#1d4ed8,color:white,stroke:#1d4ed8
    classDef db fill:#1e3a5f,color:white,stroke:#1e3a5f

    class A,B green
    class C pill
    class D blue
    class DB,TR db
```

<!-- AH -->

---
layout: section
---

# Web-Formulare
## Offline-Geschichte

<!-- AP -->

---
layout: section
---

# Duplikatvermeidung und mehr
## Räumliche Information / Zukunftsinfos

<!-- AH -->

---
layout: center
---

# Altdaten-Übernahme Var. 2

<!-- AH -->


