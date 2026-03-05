# 📘 README – WheelzUp Aanwezigheidsregistratie & Statistiekenplatform

## 📌 Overzicht
WheelzUp heeft een digitaal systeem nodig om aanwezigheden van leden te registreren via een vaste QR‑code. Het huidige proces (WhatsApp + Excel) is foutgevoelig, tijdrovend en biedt geen betrouwbare statistieken. Dit project levert een webgebaseerd platform met een eenvoudige QR‑flow voor leden en een beveiligde backend voor bestuurders en trainers.

Het systeem ondersteunt:
- QR‑registratie met automatische tijdsvalidatie  
- Gezinsregistratie en activiteitenkeuze  
- Trainingsbeheer  
- Statistieken en rapportage  
- Beveiligde backend met rollen  
- Uitbreidbaarheid naar mobiele app  


## 🧩 Probleemstelling
De club registreert aanwezigheden manueel, wat leidt tot:
- onnauwkeurige gegevens  
- ontbrekende registraties  
- geen overzicht of statistieken  
- foutieve QR‑scans buiten trainingsuren  
- geen autorisatiesysteem  

Het nieuwe systeem moet betrouwbaar, gebruiksvriendelijk, goedkoop te hosten en uitbreidbaar zijn.


## 👥 Stakeholders & Gebruikersrollen

### Stakeholders
- **Bestuur WheelzUp** – bepaalt vereisten, budget, rapportage.
- **Trainers / leiding** – willen aanwezigheden en statistieken raadplegen.
- **Leden & gezinnen** – registreren aanwezigheid via QR.
- **IT‑beheer / ontwikkelaars** – bouwen en onderhouden het systeem.
- **Toekomstige app‑gebruikers** – uitbreiding naar login/app.

### Gebruikersrollen
- **Lid (geen login)**  
  - QR scannen  
  - Naam/gezinsleden ingeven  
  - Activiteit kiezen  
  - Taal kiezen  

- **Trainer**  
  - Aanwezigheden en statistieken bekijken (beperkte rechten)  

- **Administrator (max. 5)**  
  - Inloggen op beveiligde backend  
  - Trainingen beheren  
  - Activiteiten beheren  
  - Statistieken downloaden  
  - Rollen beheren  
  - Audit logs bekijken  

- **Systeem**  
  - Tijdslotvalidatie  
  - Timestamp opslaan  
  - Geldige/ongeldige scans onderscheiden  


## ⚙️ Functionele eisen (User Stories)

### QR‑registratie & aanwezigheden
- Als lid wil ik een vaste QR‑code kunnen scannen zodat ik mijn aanwezigheid kan registreren.
- Als lid wil ik enkel kunnen registreren binnen 30 minuten voor, tijdens en 30 minuten na de training.
- Als lid wil ik enkel op de dag van de training kunnen registreren.
- Als ouder wil ik meerdere gezinsleden tegelijk kunnen registreren.
- Als lid wil ik een activiteit kunnen kiezen (basis, gevorderd, hockey, toertocht, alternatieve activiteit, speciale activiteit).
- Als lid wil ik een taal kunnen kiezen (NL/FR/EN).
- Als systeem wil ik dubbele namen op dezelfde dag blokkeren.
- Als systeem wil ik automatisch een timestamp opslaan.

### Trainingsbeheer
- Als admin wil ik trainingen flexibel kunnen inplannen.
- Als admin wil ik vaste datums vanaf 1 januari kunnen instellen.
- Als admin wil ik trainingstypes en subactiviteiten kunnen beheren.
- Als admin wil ik trainingen kunnen annuleren met reden.
- Als systeem wil ik trainingen die voorbij zijn automatisch naar geschiedenis verplaatsen.

### Backend & rollen
- Als admin wil ik kunnen inloggen op een beveiligde backend.
- Als admin wil ik rollen kunnen beheren (trainer, hoofdadmin, statistiekbeheerder).
- Als admin wil ik een audit log zien van wie wanneer inlogt.

### Statistieken & rapportage
- Als admin wil ik een lijst van aanwezigen per training zien.
- Als admin wil ik het aantal aanwezigen per training zien.
- Als admin wil ik gemiddelde aanwezigheden per maand/jaar kunnen bekijken.
- Als admin wil ik een top 10 van meest aanwezige leden kunnen zien.
- Als admin wil ik statistieken kunnen filteren op datum, periode, activiteit, subactiviteit.
- Als admin wil ik statistieken kunnen downloaden (PDF/Excel).
- Als admin wil ik geldige en ongeldige scans kunnen bekijken.

### Toekomstige uitbreidbaarheid
- Als admin wil ik dat het systeem uitbreidbaar is naar een mobiele app.
- Als lid wil ik dat gegevens eenvoudig via smartphone ingegeven kunnen worden.
- Als admin wil ik nieuwe activiteiten kunnen toevoegen wanneer nodig.


## ✅ Definition of Done (DoD)
Een feature is *done* wanneer:
- Alle user stories correct werken.
- Validaties functioneren (tijdslimiet, dubbele namen, verplichte velden).
- QR‑flow werkt op smartphone.
- Database correct schrijft en leest.
- Backend beveiligd is met login en rollen.
- Audit logs correct worden opgeslagen.
- Statistieken correct berekend worden.
- UI gebruiksvriendelijk is (desktop + mobiel).
- Unit tests + manuele tests geslaagd zijn.
- Documentatie aanwezig is.
- Stakeholders akkoord zijn.


## 🛡️ Niet‑functionele eisen

### Prestatie
- QR‑registratie binnen 1–2 seconden.
- Statistieken laden binnen 2–3 seconden.

### Beveiliging
- Veilige login (hashing).
- Audit log verplicht.
- Enkel bestuurders toegang tot backend.
- GDPR‑conforme opslag van gegevens.

### Betrouwbaarheid
- 24/7 beschikbaarheid.
- Dagelijkse back‑ups.
- Correcte detectie van foutieve scans.

### Gebruiksvriendelijkheid
- Eenvoudige QR‑flow, ook voor kinderen.
- Overzichtelijke backend voor bestuur/trainers.

### Onderhoudbaarheid
- Modulair, uitbreidbaar systeem.
- Logische database‑structuur.

### Budget
- Licht en goedkoop te hosten.
- Geen dure frameworks of licenties.

## 📦 Scope

### In scope
- QR‑registratie via vaste QR‑code  
- Tijdslimiet op registratie  
- Namen, gezinsleden, activiteiten ingeven  
- Taalkeuze  
- Database voor leden, activiteiten, trainingen, aanwezigheden, rollen, audit logs  
- Backend met login  
- Statistieken + PDF/Excel export  
- Flexibel plannen van trainingen  
- Overzicht per activiteit  
- Aparte tabel voor ongeldige scans  
- Mobielvriendelijke invoer  

### Out of scope
- Volwaardige mobiele app  
- Betaalsystemen of lidgeldbeheer  
- Communicatieplatform (berichten, meldingen)  
- Integratie met externe sportplatformen  
- Automatische detectie zonder QR (NFC, GPS)  
- Hardware (scanners, tablets…)  

