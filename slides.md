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


---
layout: center
---

# Authentifizierung

<!-- AH -->

---
layout: center
---

# Altdaten-Übernahme Var. 1
## via Alt-Login

<!-- AH -->

---
layout: center
---

# EUDR

- Bereits Erfahrung mit EUDR durch Entwicklung des **BMLUK EUDR-Meldung**-Tools
- Kenntnis der Prozesse rund um EUDR-Sorgfaltserklärungen und Referenznummern
- Technisches Know-how zur Anbindung an die **TRACES**-Datenbank

<img src="./eudr-flow.svg" class="mt-4 mx-auto h-72" />

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


