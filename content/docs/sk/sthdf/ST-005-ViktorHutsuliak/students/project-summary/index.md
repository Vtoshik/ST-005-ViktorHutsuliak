---
# 🧩 Versioning – systém dopĺňa automaticky
fm_version: "1.0.1"

# Dátum buildu – generuje skript
fm_build: "2026-10-05T15:36:21.335042+00:00"

# Poznámka k verzii – voliteľné
fm_version_comment: ""


# 🆔 IDENTITY --------------------------------------------------------

# ID generuje CLI / skript

# Unikátne UUID – generuje skript
guid: "d33450de-793f-4fbc-83b2-ce9e8c30ed08"


# 🧭 CONTEXT ---------------------------------------------------------

# DAO / doména (knife, sdlc, q12, 7ds...) dopĺňa skript
dao: "sthdf"

# Názov zápisu – dopĺňa používateľ
title: "Project Summary"

# Krátky popis – dopĺňa používateľ (voliteľné)
description: "Zhrnutie projektu ST-005 Viktora Hutsuliaka"


# 👥 AUTHORSHIP ------------------------------------------------------

# Hlavný autor – z globálneho configu
author: "Viktor Hutsuliak"

# Zoznam autorov – generuje skript
authors:
  - "Viktor Hutsuliak"


# 🗂 CLASSIFICATION ---------------------------------------------------

# Nadradená kategória – môže doplniť používateľ
category: "sthdf"

# Typ dokumentu (guide, case, tutorial...) – používateľ (voliteľné)
type: ""

# Priorita (low/medium/high) – voliteľné
priority: ""

# Tagy – odporúča sa 2–6 tagov.
# Typy tagov:
#   - rámce: knife, 7ds, sdlc, q12
#   - účel: tutorial, guide, pattern, case-study
#   - téma: git, backup, ai, communication
#   - úroveň: beginner, intermediate, advanced
tags: ["sthdf", "deliverables", "student"]


# 🌍 LOCALIZATION -----------------------------------------------------

# Jazyk dokumentu – doplní skript podľa štruktúry
locale: "sk"


# 🕒 LIFECYCLE --------------------------------------------------------

# Dátum vytvorenia – generuje skript
created: "2026-10-05 17:36"

# Dátum poslednej úpravy – dopĺňa človek
modified: "2026-10-20 15:10"

# Stav dokumentu – default "backlog"
status: "in-progress"

# Viditeľnosť – default "public"
privacy: "public"


# ⚖ INTELLECTUAL PROPERTY -------------------------------------------

# Držiteľ práv k obsahu – dopĺňa skript
rights_holder_content: "Viktor Hutsuliak"

# Systémový vlastník práv
rights_holder_system: "CAA / KNIFE / LetItGrow"

# Licencia
license: "CC-BY-NC-SA-4.0"

# Disclaimer
disclaimer: "Use at your own risk. Methods provided as-is; participation is voluntary and context-aware."

# Copyright
copyright: "© 2026 Viktor Hutsuliak"


# 🔗 ORIGIN / PROVENANCE ---------------------------------------------

# Repozitár pôvodu
origin_repo: ""

# URL pôvodného repozitára
origin_repo_url: ""

# Commit pôvodu
origin_commit: ""

# Branch pôvodu
origin_branch: ""

# Systém pôvodu (CAA/KNIFE/STHDF…)
origin_system: "CAA"

# Pôvodný autor
origin_author: "Roman Kazicka"

# Importovaný zdroj
origin_imported_from: ""

# Dátum importu
origin_import_date: ""


# 🧱 RESERVED ---------------------------------------------------------

fm_reserved1: ""
fm_reserved2: ""
---

<!-- SDLC_INSTANCE_ID: ST-005-ViktorHutsuliak -->

# 📝 Project Summary

## 🔖 Identifikácia
## 1️⃣ Názov projektu
*(Jasný, výstižný, inšpiratívny – ako by sa mal objaviť na plagáte.)*
- **Názov projektu:** HackLock
- **Stručný popis:** Edukačný zámok s klávesnicou postavený na ESP32, na ktorom si študenti prakticky vyskúšajú útok cez časový postranný kanál (timing side channel). Firmvér existuje v dvoch verziách, zámerne slabej a zabezpečenej, takže únik sa dá zmerať a potom na reálnom hardvéri aj odstrániť.

## 2️⃣ Členovia tímu

| ST ID | Meno | Rola v tíme | Kompetencie |
|-------|------|-------------|-------------|
| ST001 |      | Project Lead | koordinácia |
| ST002 |      | Developer | implementácia |
| ST003 |      | Designer | UI/UX |

## 3️⃣ Motivácia tímu
- Prečo ste si vybrali tento projekt?
- Aký osobný alebo profesný zmysel má pre vás riešenie tejto témy?
- Prečo je projekt dôležitý
- Aký problém rieši

## 4️⃣ Cieľ a pridaná hodnota projektu
- Finálny cieľ: urobiť neviditeľný typ chyby, rozdiel pár mikrosekúnd v odozve, viditeľným a merateľným, a potom ukázať, že oprava funguje.
- Úspech spoznáme podľa toho, že pomocou meracieho nástroja vieme na slabom firmvéri uhádnuť PIN znak po znaku a na zabezpečenom firmvéri už nie.

## 5️⃣ Popis riešenia
HackLock je malá krabička s klávesnicou. Používateľ zadá PIN a ak je správny, servo otvorí veko a LED sa rozsvieti nazeleno. Zaujímavé je, ako firmvér PIN kontroluje:

- Slabý (učebný) firmvér porovnáva zadaný PIN s tajným znak po znaku a zareaguje hneď pri prvom nesprávnom znaku. Čas odozvy tak závisí od počtu správnych znakov na začiatku, čo je klasický timing side channel.
- Zabezpečený firmvér porovnáva celý PIN v konštantnom čase, takže čas odozvy už nič neprezrádza.

Pomocný nástroj na notebooku meria čas odozvy zariadenia cez sériovú linku, aby sa obe verzie firmvéru dali porovnať na rovnakom hardvéri.

Hardvér: ESP32, klávesnica, servo, LED. Poznámka k rozsahu: HackLock je učebná pomôcka. Ukazuje známu triedu zraniteľností na vlastnom zariadení a je určená na výuku a samoštúdium.

## 6️⃣ Projektový plán
- Odhadovaný čas na prácu: _x hodín / týždeň_
- Predpokladaný stav v čase prezentácie: _MVP / prototyp / dokumentácia / funkčný produkt_
- Hlavné míľniky:
  - [ ] Príprava
  - [ ] Implementácia
  - [ ] Testovanie
  - [ ] Prezentácia

### 📅 Míľniky a výstupy
- **Do januára dodáme:**
  - [ ] prototyp
  - [ ] prezentáciu
  - [ ] dokumentáciu

## 7️⃣ Zákazník a hodnoty
- Používateľmi sú študenti a učitelia, ktorí sa učia o bezpečnosti zariadení a postranných kanáloch.
- Prinesie im to možnosť vidieť, zmerať a opraviť zraniteľnosť na fyzickom zariadení, nie len čítať o nej v teórii.

## 8️⃣ Očakávané výstupy
- Dokumentácia: README, popis firmvéru a meracieho nástroja, KNIFE článok.
- Artefakty: fyzický zámok HackLock, dve verzie firmvéru (slabá a zabezpečená), nástroj na meranie odozvy.

## 📚 Kontext
- KNIFE príspevky, literatúra, inšpirácie

## 🧭 Riziká a závislosti
- Riziká projektu
- Na čom závisí

## 9️⃣ Reflexia a ďalšie kroky
Čo očakávate, že sa naučíte?
Ako by sa projekt mohol rozvíjať ďalej?

---

## Navigácia
- [↩️ Späť](../index.md)
