---
# try also 'default' to start simple
theme: default
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

<img src="./assets/w3geo-logo.png" class="abs-br m-8 h-12" style="filter: brightness(3)" />
<img src="./assets/pefc-logo.png" class="abs-bl m-8 h-12" />

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
layout: default
---

# Umsetzungskonzept 1 / 4

- Rollenabhängige Benutzeroberfläche im Client, umgesetzt ausschließlich mit Open Source Frameworks (z.B. VUE)
  - Erfahrung aus div. Projekten, Beispiel ISTMobil:
    - *Große Datenbank mit tausenen Kunden, Verkehrsunternehmern, Disponenten, Administratoren usw.*
    - *Die Oberfläche wird rollenabhängig dargestellt*
    - *Für bestimmte Rollen responsive Versionen, z.B. Fahrzeug-Applikation*

<div class="mt-4 flex flex-wrap justify-center gap-4">
  <img src="./assets/istmobil03.jpg" class="h-52" />
  <img src="./assets/istmobil07.jpg" class="h-52" />
</div>

---
layout: default
---

# Umsetzungskonzept 2 / 4

- Responsive Web-Formulare anstatt Excel-Sheets
 - Offline fähig (z.B. im Wald)
 - Erfahrung aus div. Projekten, z.B. GZA, eStrab, sofisch

<div class="mt-4 flex flex-wrap justify-center gap-4">
  <img src="./assets/gza03.jpg" class="h-52" />
  <img src="./assets/sofisch06.jpg" class="h-52" />
</div>


---
layout: default
---

# Umsetzungskonzept 3 / 4

- Relationale Datenbank, geeignet für große Datenmengen und performative Suchen (z.B. PostgreSQL)
- Logging sämtlicher relevanter Ereignisse in Form eines sg. "Activity Trails"
  - bietet auch Verknüpfung zu DB-Entitäten / anderen Ereignissen
- Audit Tools für Auswertungen / Controlling
  - *Beispiel ISTMobil - Fahrzeug-Controlling*

<div class="mt-4 flex flex-wrap justify-center gap-4">
  <img src="./assets/istmobil10.jpg" class="h-52" />
  <img src="./assets/istmobil11.jpg" class="h-52" />
</div>


---
layout: default
---

# Umsetzungskonzept 4 / 4

- Hosting in skalierbarer, performativer Server-Infrastruktur
  - ISO 27001 zertifiziertes Rechenzentrum 
  - Serverstandort EU 
  - Continuous Integration und Deployment (CI/CD) 

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

# Web-Formulare

- Gut strukturierte Web-Formulare (Material Design)
- Voll Responsiv, Basiseigenschaften für Barrierefreiheit
- Zwischenspeicherung des aktuellen Standes
- Prüfung auf Vollständigkeit / Plausibilität bei Einreichung (Vorteil zu externen Dateien)
- **Offline Fähigkeit**
- Fallback: "Analoge" Formulare als Upload

<div class="mt-4 flex flex-wrap justify-center gap-4">
  <img src="./assets/audit1.webp" class="h-52" />
  <img src="./assets/audit2.webp" class="h-52" />
</div>

---
layout: center
---

# Identity Provider, Authentifizierung

- Bereits Erfahrungen mit USP, eAMA Partner-Login, ID Austria
- Kenntnis der zugehörigen Antragsformalitäten
- Berücksichtigung der unterschiedlichen Charakteristika

<img src="./assets/idp.png" class="mt-4 h-76">

---
layout: center
---

# Verknüpfen von Accounts und Duplikatvermeidung
- Eindeutige Attribute (LFBIS-Nummer) erleichtern Account-Verknüpfung
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
layout: two-cols
---

# EUDR – EU Entwaldungsverordnung

::left::

- Bereits Erfahrung mit EUDR durch Entwicklung des **BMLUK EUDR-Meldung**-Tools
- Kenntnis der Prozesse rund um EUDR-Sorgfaltserklärungen und Referenznummern
- Technisches Know-how zur Anbindung an die **TRACES**-Datenbank

::right::

<div class="pl-8">

```mermaid {theme: 'neutral', scale: 0.6}
flowchart TB
    subgraph std ["Standard-Prozess"]
        direction TB
        A["App erstellt Sorgfaltserklärung"] --> B["Nutzer bestätigt ✓"]
        B --> C(["PEFC: bevollmächtigter Vertreter aller Mitglieder"])
    end
    subgraph alt ["Alternativ"]
        direction TB
        D["Nutzer gibt bestehende Referenznummer ein"]
        D --> E["App verifiziert Nummer über TRACES  ✓"]
    end
    subgraph coc ["Chain of Custody"]
        F["CoC-Unternehmen fügt Lieferanten hinzu"]
    end
    std --> DB[(Referenznummer in Datenbank)]
    alt --> DB
    DB -->|"Detailabfragen"| TR[(TRACES-Datenbank)]
    DB -->|"Lieferantenzuordnung"| coc

    classDef green fill:#15803d,color:white,stroke:#15803d
    classDef pill fill:#16a34a,color:white,stroke:#16a34a
    classDef blue fill:#1d4ed8,color:white,stroke:#1d4ed8
    classDef db fill:#1e3a5f,color:white,stroke:#1e3a5f
    classDef orange fill:#c2410c,color:white,stroke:#c2410c

    class A,B green
    class C pill
    class D,E blue
    class DB,TR db
    class F orange
```

</div>

<!-- AH -->

---
layout: center
---

optional:

# Altdaten-Übernahme
- Erfordert Export/Kopie der Bestandsdatenbank
- Nur zu empfehlen für bereits strukturierte Daten
- Erspart Nutzerfrust bei Launch der neuen Applikation

<div class="flex items-start justify-center mt-8">
  <div class="flex flex-col items-center w-32">
    <div class="w-12 h-12 rounded-full bg-green-700 text-white flex items-center justify-center font-bold text-xl">1</div>
    <div class="mt-2 text-center text-sm leading-tight text-slate-700">Alt-App<br>Login</div>
  </div>
  <div class="mt-6 h-0.5 w-10 bg-green-300 shrink-0"></div>
  <div class="flex flex-col items-center w-32">
    <div class="w-12 h-12 rounded-full bg-green-700 text-white flex items-center justify-center font-bold text-xl">2</div>
    <div class="mt-2 text-center text-sm leading-tight text-slate-700">Daten<br>sichten</div>
  </div>
  <div class="mt-6 h-0.5 w-10 bg-green-300 shrink-0"></div>
  <div class="flex flex-col items-center w-32">
    <div class="w-12 h-12 rounded-full bg-green-700 text-white flex items-center justify-center font-bold text-xl">3</div>
    <div class="mt-2 text-center text-sm leading-tight text-slate-700">Verifizieren<br>&amp; Anpassen</div>
  </div>
  <div class="mt-6 h-0.5 w-10 bg-green-300 shrink-0"></div>
  <div class="flex flex-col items-center w-32">
    <div class="w-12 h-12 rounded-full bg-green-800 text-white flex items-center justify-center font-bold text-xl">✓</div>
    <div class="mt-2 text-center text-sm leading-tight text-slate-700">Daten<br>übernommen</div>
  </div>
</div>



<!-- AH -->

---
layout: center
---

# Räumliche Information

- Räumliche Daten sind "einfach da":
  - **Adressen** von Unternehmen und Benutzern (amtliches Adressregister)
  - **Bezirke**, in denen ein Forstbetrieb Waldflächen bewirtschaftet
- Mögliche Ausbaustufe: Erfassung von Waldflächen mit höherer Genauigkeit (Grundstück)
- **Potenzial der räumlichen Daten:**
  - Duplikatvermeidung bei Besitzerwechsel — gleiche Adresse signalisiert möglichen Zusammenhang
  - Karte der zertifizierten Mitglieder nach Bezirk / Dichte-Auswertung
  - Regionale Filterung &amp; Auswertungen für Controlling und Reporting

<!-- AH -->

---
layout: center
---

# Danke für die Aufmerksamkeit

<ph-handshake-thin class="text-7xl text-amber-400 mx-auto mt-4 block" />

<PoweredBySlidev class="abs-br m-8" />