# User Stories voor CodeCampus Dashboard

Na het oplossen van alle bugs kunnen teams kiezen uit onderstaande user stories om nieuwe features toe te voegen. Verdeel het werk eerlijk en kies features die bij jullie vaardigheidsniveau passen.

---

## Must-have Features (Prioriteit 1)

### User Story 1: Zoekfunctionaliteit

**Als gebruiker** wil ik **cursussen kunnen zoeken op titel of trefwoord** zodat ik **snel specifieke cursussen kan vinden zonder door de hele lijst te scrollen**.

**Acceptatiecriteria:**

- Er is een zoekbalk zichtbaar bovenaan het dashboard
- Bij het typen worden resultaten direct gefilterd (zonder pagina te verversen)
- Zoeken werkt op cursustitel en beschrijving
- Als er geen resultaten zijn, wordt een melding getoond
- De zoekfunctie werkt in combinatie met eventuele actieve filters

### User Story 2: Sorteeropties

**Als gebruiker** wil ik **cursussen kunnen sorteren op verschillende criteria** zodat ik **ze kan ordenen op een manier die voor mij relevant is**.

**Acceptatiecriteria:**

- Er is een dropdown menu met sorteeropties
- Cursussen kunnen gesorteerd worden op: populariteit, rating, duur
- De huidige sortering wordt visueel aangegeven
- Sortering werkt in combinatie met eventuele filters of zoekopdrachten

### User Story 3: Cursus details bekijken

**Als gebruiker** wil ik **op een cursus kunnen klikken voor meer informatie** zodat ik **een beter beeld krijg van de inhoud voordat ik de video bekijk**.

**Acceptatiecriteria:**

- Bij klikken op een cursuskaart verschijnt een modal of detailpagina
- De detailweergave toont uitgebreide beschrijving, leerdoelen, en andere relevante info
- Er is een knop om direct naar de video te gaan
- Er is een knop om terug te gaan naar het overzicht

### User Story 4: Filtering op categorieën

**Als gebruiker** wil ik **cursussen kunnen filteren op categorieën** zodat ik **alleen cursussen zie die relevant zijn voor een specifiek onderwerp**.

**Acceptatiecriteria:**

- Er is een sectie/component waar categorieën worden getoond
- Meerdere categorieën kunnen tegelijk geselecteerd worden
- Geselecteerde categorieën worden visueel gemarkeerd
- Bij selectie worden alleen relevante cursussen getoond
- Er is een optie om alle filters te wissen

---

## Should-have Features (Prioriteit 2)

### User Story 5: Gebruikersauthenticatie (Login/Register)

**Als gebruiker** wil ik **een account kunnen aanmaken en inloggen** zodat ik **een persoonlijke ervaring heb en mijn data wordt opgeslagen**.

**Acceptatiecriteria:**

- Register form met validatie (email, password, confirm password, naam)
- Login form met email/password
- Password requirements (minimaal 8 karakters, hoofdletter, cijfer)
- Error handling voor ongeldige login, duplicate email, etc.
- "Remember me" checkbox voor langere sessies
- Logout functionaliteit
- Protected routes voor features zoals cart, profile, reviews
- Session management via localStorage met expiration
- Basic profile info tonen in header wanneer ingelogd

**React concepten:**

- Context API en useContext
- Form handling en controlled components
- Input validatie en error states
- Conditional rendering op basis van auth status
- localStorage voor session persistence

### User Story 6: Favorieten & Wishlist systeem

**Als gebruiker** wil ik **cursussen kunnen markeren als favoriet en toevoegen aan een wishlist** zodat ik **een persoonlijke collectie kan maken van cursussen die me interesseren**.

**Acceptatiecriteria:**

- Elke cursuskaart heeft zowel een "favoriet" als "wishlist" knop
- Aparte pagina's/tabs voor favorieten en wishlist
- Mogelijkheid om items van wishlist naar favorieten te verplaatsen
- Teller badges die aantal items tonen
- Alles wordt opgeslagen in localStorage met complexere data structuur
- Alleen maar te zien als je bent ingelogd

### User Story 7: Review & Rating systeem

**Als gebruiker** wil ik **reviews kunnen lezen en schrijven voor cursussen** zodat ik **geïnformeerde beslissingen kan maken op basis van ervaringen van anderen**.

**Acceptatiecriteria:**

- Sterren rating systeem (1-5 sterren) per cursus
- Mogelijkheid om geschreven reviews toe te voegen
- Reviews tonen met gebruikersnaam, datum, rating en tekst
- Gemiddelde rating berekenen en tonen op cursuskaarten
- Filter cursussen op minimale rating
- Review form met validatie (vereiste velden, karakterlimiet)
- Reviews opslaan in localStorage

### User Story 8: Shopping Cart functionaliteit

**Als gebruiker** wil ik **cursussen kunnen toevoegen aan een winkelwagen** zodat ik **meerdere cursussen tegelijk kan "kopen"**.

**Acceptatiecriteria:**

- "Toevoegen aan cart" knop op elke cursuskaart
- Floating cart icon met badge die aantal items toont
- Cart modal/pagina met overzicht van toegevoegde cursussen
- Mogelijkheid om items uit cart te verwijderen
- Totaalprijs berekening
- "Checkout" proces simuleren (geen echte betaling)
- Cart state behouden tussen sessies
- Toast notifications bij toevoegen/verwijderen

### User Story 9: Geavanceerde filtering & zoeken

**Als gebruiker** wil ik **cursussen filteren op meerdere criteria tegelijk** zodat ik **precies kan vinden wat ik zoek**.

**Acceptatiecriteria:**

- Filter op: categorie, moeilijkheidsgraad, rating, prijs range, duur
- Multiple select voor categorieën
- Slider voor prijs range
- Checkbox filters voor moeilijkheidsgraad (beginner, intermediate, advanced)
- Actieve filters tonen als "tags" die individueel verwijderd kunnen worden
- "Clear all filters" knop
- URL parameters voor deep linking van filter states
- Filter state opslaan per gebruiker in localStorage (voor ingelogde users)
- Guest users krijgen basic filtering, ingelogde users krijgen saved preferences

---

## Could-have Features (Prioriteit 3)

### User Story 10: Gebruikersprofielen & Dashboard

**Als gebruiker** wil ik **een persoonlijk profiel en dashboard** zodat ik **mijn leervoortgang kan bijhouden en beheren**.

**Acceptatiecriteria:**

- Gebruikersprofiel pagina met avatar upload (via file input)
- Dashboard met overzicht van: ingeschreven cursussen, favorieten, wishlist, reviews
- Leervoortgang tracking per cursus (percentage completed)
- Totale leertijd bijhouden
- Persoonlijke statistieken (aantal cursussen, gemiddelde rating gegeven, etc.)
- Profile edit functionaliteit
- Data opslaan in localStorage met complexe user object

### User Story 11: Recently Viewed & Recommendations

**Als gebruiker** wil ik **recent bekeken cursussen zien en aanbevelingen krijgen** zodat ik **gemakkelijk kan terugkeren naar interessante content**.

**Acceptatiecriteria:**

- "Recently viewed" sectie die laatste 5-10 bekeken cursussen toont
- Aanbevelingen gebaseerd op bekeken cursussen (zelfde categorie/instructor)
- "Omdat je X bekeken hebt" sectie
- Slimme algoritme voor aanbevelingen (gebruik localStorage data)
- Mogelijkheid om recent viewed te wissen
- Time-based filtering (laatste week, maand)

### User Story 12: Advanced Search & Autocomplete

**Als gebruiker** wil ik **geavanceerde zoekmogelijkheden met suggesties** zodat ik **efficiënt kan vinden wat ik zoek**.

**Acceptatiecriteria:**

- Autocomplete dropdown met suggesties tijdens typen
- Zoekgeschiedenis opslaan en tonen
- "Did you mean..." functionaliteit voor typos
- Zoeken in titel, beschrijving, instructor naam, en tags
- Search highlights in resultaten
- Voice search functionaliteit (Web Speech API)
- Advanced search modal met filters gecombineerd

---

## Would-like Features (Prioriteit 4)

### User Story 13: Instructor Profiles & Follow System

**Als gebruiker** wil ik **instructors kunnen volgen en hun profielen bekijken** zodat ik **op de hoogte blijf van nieuwe cursussen van mijn favoriete leraren**.

**Acceptatiecriteria:**

- Instructor profiel pagina's met bio, expertise, alle cursussen
- "Follow" knop op instructor profielen
- Notification systeem voor nieuwe cursussen van gevolgde instructors
- Instructor statistics (aantal cursussen, gemiddelde rating, aantal studenten)
- "Following" pagina met overzicht van gevolgde instructors
- Filter cursussen op specific instructor

### User Story 14: Learning Path & Progress Tracking

**Als gebruiker** wil ik **leerpaden kunnen volgen en mijn voortgang bijhouden** zodat ik **gestructureerd kan leren naar een specifiek doel**.

**Acceptatiecriteria:**

- Pre-defined learning paths (bijv. "Web Development Beginner to Pro")
- Visual progress indicators per learning path
- Unlock system: volgende cursus wordt pas beschikbaar na completion
- Certificates of completion voor paths
- Time estimation per path
- Bookmark functionaliteit binnen cursussen
- Note-taking functionaliteit per cursus/module

### User Story 15: Social Features & Study Groups

**Als gebruiker** wil ik **kunnen communiceren met andere studenten** zodat ik **samen kan leren en vragen kan stellen**.

**Acceptatiecriteria:**

- Q&A sectie per cursus waar studenten vragen kunnen stellen
- Upvote/downvote systeem voor vragen en antwoorden
- Study group creation en joining
- Discussion forums per cursus categorie
- Private messaging tussen studenten
- Student leaderboards per cursus
