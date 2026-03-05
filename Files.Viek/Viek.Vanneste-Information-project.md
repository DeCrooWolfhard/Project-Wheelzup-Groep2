# 📌 WheelzUp – Aanwezigheidsregistratie & Statistiekenplatform

## 1. Doel van het project
Dit project ontwikkelt een digitaal systeem waarmee WheelzUp aanwezigheden automatisch kan registreren via QR-codes. Het bestuur krijgt toegang tot uitgebreide statistieken en rapportages.  
Het systeem moet **makkelijk uitbreidbaar**, **gebruiksvriendelijk** en **foutbestendig** zijn.

---

## 2. Huidige situatie & problemen
- Aanwezigheden worden nu via WhatsApp doorgegeven → onoverzichtelijk.
- Bestuur wil weten:
  - Wie aanwezig is.
  - Hoeveel leden per training aanwezig zijn.
  - Gemiddeld aantal aanwezigen per maand/jaar.
- Excel is te omslachtig en moet telkens manueel worden overlopen.
- De QR-code is momenteel hard coded en verwijst naar een eenvoudige webpagina.
- Er is geen controle op het tijdstip van scannen → scans buiten trainingsuren zijn foutief.

---

## 3. Gewenste oplossing

### 3.1 QR-code systeem
- Een vaste QR-code hangt op het bord.
- QR-code bevat een link naar een webformulier (geen login nodig).
- Formulier bevat:
  - Voornaam
  - Familienaam
  - Automatische datum + tijd
  - Optioneel: aantal personen (met dynamische velden)
  - Optioneel: gezinssnelkeuze met vinkjes

#### 3.1.1 Tijdslotvalidatie
- Scans **binnen trainingsuren** → geldige aanwezigheid.
- Scans **buiten trainingsuren** → opgeslagen in een **aparte tabel**:
  - Bestuur kan zien wanneer iemand foutief of te vroeg/laat heeft gescand.
  - Deze scans tellen **niet** mee voor statistieken.

#### 3.1.2 Agenda-integratie
- Trainingsuren worden beheerd in een backend-agenda.
- QR-code is enkel “actief” tijdens geplande trainingen.
- Voorkomt foutieve registraties.

---

## 4. Functionaliteiten voor leden (frontend)
- QR scannen → formulier invullen → klaar.
- Geen login nodig.
- Mogelijkheid om meerdere personen tegelijk te registreren:
  - Vraag: “Met hoeveel personen ben je aanwezig?”
  - Dynamisch aantal velden.
  - Validatie: geen dubbele namen op dezelfde dag.
- Optie om een gezin aan te maken:
  - Lijst met gezinsleden + vinkjes.
  - Snel meerdere personen aanduiden.

---

## 5. Functionaliteiten voor bestuur (backend)

### 5.1 Trainingsbeheer
- Trainingen toevoegen, wijzigen en verwijderen.
- Ondersteunde trainingstypes:
  - Basis training
  - Gevorderde training
  - Hockey training
  - Toertocht
  - Alternatieve activiteit
- Per training:
  - Datum + tijd
  - Subactiviteiten
- Verlopen trainingen → automatisch naar **geschiedenis**.
- Trainingen kunnen geannuleerd worden met een reden.

### 5.2 Statistieken & rapportage
Bestuur (max. 5 personen) kan:

#### 5.2.1 Aanwezigheidsstatistieken
- Aantal aanwezigen per training (per datum).
- Gemiddeld aantal aanwezigen per maand / jaar.
- Top 10 meest aanwezige leden.
- Minst aanwezige leden.
- Filters:
  - Datum
  - Periode
  - Trainingstype
  - Subactiviteit

#### 5.2.2 Downloads
- Statistieken kunnen worden gedownload (PDF/Excel).

#### 5.2.3 Extra tabellen
- **Geldige scans** (binnen trainingsuren).
- **Ongeldige scans** (buiten trainingsuren).

---

## 6. Gegevens die worden opgeslagen
- Voornaam
- Familienaam
- Datum + tijd van scan
- Trainingstype
- Subactiviteit
- Aantal personen (indien van toepassing)
- Gezin (optioneel)
- Geldige of ongeldige scan

---

## 7. Webplatform
- Taal: **Nederlands**
- Gericht op **PC-gebruik**
- Enkel toegankelijk voor bestuur (5 personen)
- Pagina’s:
  - Dashboard
  - Statistieken
  - Trainingen beheren
  - Geschiedenis
  - Ongeldige scans
  - Leden/subactiviteiten overzicht

---

## 8. Extra wensen
- Systeem moet makkelijk uitbreidbaar zijn.
- Automatische verwerking van QR-scans.
- Mogelijkheid om subactiviteiten per training te registreren.
- Mogelijkheid om gezinnen te beheren.
- Validatie tegen dubbele namen op dezelfde dag.

---

## 9. Trainingsmomenten (voorbeeld)
- Zondag 10:00 – 12:00  
  (Moet configureerbaar zijn in backend)

---

## 10. Nieuwe toevoeging
- Scans buiten trainingsuren worden opgeslagen in een aparte tabel.
- QR-code is momenteel hard coded en verwijst naar een webformulier.
- Dit formulier moet worden geïntegreerd in het nieuwe systeem.

