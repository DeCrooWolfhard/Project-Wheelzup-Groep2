# Project-Wheelzup-Groep2
⭐ Verbeterde Prompt: Projectvoorbereiding Wheelzup
Ontwikkel een webgebaseerd aanwezigheids- en statistiekensysteem voor Wheelzup, een sportclub voor jeugd met een beperkt budget. De club is een skielerclub en wil efficiënter werken dan de huidige manuele WhatsApp aanwezigheidsregistratie.

🎯 Doel van het systeem
•	Aanwezigheden registreren via één vaste QR code die aan het bord hangt.
•	Bij het scannen moet de gebruiker zijn naam (en eventueel gezinsleden) kunnen ingeven.
•	Het systeem registreert automatisch een timestamp en slaat deze op in een database.
•	Administrators moeten uitgebreide statistieken kunnen bekijken via een beveiligde backend.


🧩 Functionele vereisten

1. QR code & scanning
•	Eén QR code die altijd geldig blijft.
•	QR code kan 30 minuten voor, tijdens en 30 minuten na de training gescand worden.
•	Scannen kan alleen op de dag van de training.
•	Trainingsmomenten zijn niet altijd vast, dus moeten flexibel ingepland kunnen worden.
•	Vanaf 1 januari moeten admins de vaste datums voor het jaar kunnen instellen.

2. Aanwezigheidsregistratie
•	Gebruikers kunnen aangeven:
o	Wie komt trainen (per persoon of per gezin).
o	Welke activiteit ze volgen: basis, gevorderden, toertocht, hockey, jaarlijkse vergadering, speciale evenementen. Per lid
•	Optie: taalkeuze (NL/FR/EN).

3. Gebruikersrollen
•	Tot 5 administrators met verschillende rollen kunnen inloggen op de backend.
•	Backend moet PC gericht zijn.
•	Loggen wie wanneer de backend opent (audit log).

4. Statistieken (alleen zichtbaar voor admins)
•	Naam + familienaam van aanwezigen.
•	Aantal aanwezigen per training.
•	Gemiddeld aantal aanwezigen per maand.
•	Top 10 aanwezigheden over een zelf te kiezen periode.
•	Aantal leden per activiteit.
•	Statistieken moeten afdrukbaar zijn.
•	Leden en niet leden mogen geen statistieken zien, enkel gegevens ingeven via QR.

5. Toekomstige uitbreidbaarheid
•	Backend moet uitbreidbaar zijn naar een mobiele app met login.
•	Gegevens moeten eenvoudig via smartphone ingegeven kunnen worden.


🛠️ Technische vereisten
•	Backend met login.
•	Database voor:
o	Leden
o	Aanwezigheden
o	Activiteiten
o	Trainingsmomenten
o	Rollen & audit logs
•	Tijdslimiet op QR code validatie.
•	Systeem moet licht en budgetvriendelijk zijn.

