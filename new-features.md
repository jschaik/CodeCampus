# User Stories voor CodeCampus Dashboard

Na het oplossen van alle bugs kunnen teams kiezen uit onderstaande user stories om nieuwe features toe te voegen. Verdeel het werk eerlijk en kies features die bij jullie vaardigheidsniveau passen.

---

## Must-have Features (Prioriteit 1)

### User Story 1: Zoekfunctionaliteit

**Als gebruiker** wil ik **cursussen kunnen zoeken op titel of trefwoord** zodat ik **snel specifieke cursussen kan vinden zonder door de hele lijst te scrollen**.

**Acceptatiecriteria:**

- Er is een zoekbalk zichtbaar bovenaan het dashboard
- Bij het typen worden resultaten direct gefilterd (zonder pagina te verversen)
- Zoeken werkt op cursustitel
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
- De detailweergave toont: titel, beschrijving, instructor, duur, rating, aantal views, prijs
- Er is een knop om direct naar de video te gaan
- Er is een knop om terug te gaan naar het overzicht

### User Story 4: Filtering op categorieën

**Als gebruiker** wil ik **cursussen kunnen filteren op categorieën** zodat ik **alleen cursussen zie die relevant zijn voor een specifiek onderwerp**.

**Acceptatiecriteria:**

- Er is een sectie waar categorieën worden getoond (gebruik de 'category' veld uit coursesData)
- Meerdere categorieën kunnen tegelijk geselecteerd worden
- Geselecteerde categorieën worden visueel gemarkeerd
- Bij selectie worden alleen relevante cursussen getoond
- Er is een optie om alle filters te wissen

### User Story 5: Dark Mode Toggle

**Als gebruiker** wil ik **kunnen schakelen tussen light en dark mode** zodat ik **de app kan gebruiken op een manier die prettig is voor mijn ogen**.

**Acceptatiecriteria:**

- Toggle knop/switch in de header (zon/maan icoontje)
- Bij klikken wisselt de app tussen light en dark theme
- Dark mode gebruikt donkere achtergrondkleuren en lichte tekst
- Voorkeur wordt opgeslagen in localStorage
- Bij herladen van de pagina blijft de gekozen mode actief
- Smooth transition tussen de modes (CSS transition)

### User Story 6: Cursus Progress Indicator

**Als gebruiker** wil ik **een visuele voortgangsbalk zien bij elke cursus** zodat ik **in één oogopslag kan zien hoeveel van de cursus ik al heb gekeken**.

**Acceptatiecriteria:**

- Elke cursuskaart toont een progress bar onderaan
- Progress bar toont percentage (0-100%)
- Knop "Markeer als bekeken" of slider om voortgang aan te passen
- Voortgang wordt opgeslagen per cursus in localStorage
- Visuele feedback: progress bar heeft kleur (bijv. groen voor >75%, oranje voor 25-75%, grijs voor <25%)
- Filter optie: "In Progress" cursussen tonen

### User Story 7: View Counter & "Trending Now"

**Als gebruiker** wil ik **zien welke cursussen populair zijn** zodat ik **weet wat andere gebruikers interessant vinden**.

**Acceptatiecriteria:**

- Bij openen van cursus details wordt view counter verhoogd
- View count wordt getoond op cursuskaart (bijv. "👁️ 234 views")
- "Trending Now" sectie toont top 3-5 meest bekeken cursussen van afgelopen week
- Views worden opgeslagen in localStorage met timestamp
- Badge "🔥 Trending" voor cursussen met >X views deze week

### User Story 8: Cursus Notities

**Als gebruiker** wil ik **notities kunnen toevoegen bij cursussen** zodat ik **belangrijke informatie kan onthouden**.

**Acceptatiecriteria:**

- "Notitie toevoegen" knop bij cursus details
- Textarea waar gebruiker notitie kan typen
- "Opslaan" knop om notitie toe te voegen
- Notities worden opgeslagen per cursus in localStorage
- Lijst met alle notities tonen onder de cursus
- Elke notitie heeft timestamp
- Badge op cursuskaart als er notities zijn (bijv. "📝 3")

---

## Should-have Features (Prioriteit 2)

### User Story 9: Gebruikersauthenticatie (Login/Register)

**Als gebruiker** wil ik **een account kunnen aanmaken en inloggen** zodat ik **een persoonlijke ervaring heb en mijn data wordt opgeslagen**.

**Acceptatiecriteria:**

- Register pagina met form (email, wachtwoord, wachtwoord bevestigen, naam)
- Login pagina met form (email, wachtwoord)
- Basis validatie:
  - Email moet geldig formaat hebben
  - Wachtwoord minimaal 6 karakters
  - Wachtwoorden moeten matchen bij registratie
- Error messages tonen bij ongeldige invoer
- Bij succesvolle registratie wordt gebruiker automatisch ingelogd
- Bij succesvolle login wordt gebruiker doorgestuurd naar dashboard
- Logout functionaliteit (knop in header)
- Gebruikersnaam tonen in header wanneer ingelogd
- Gebruikersdata opslaan in localStorage (email, naam, id)
- Ingelogde status blijft bewaard na page refresh

### User Story 10: Favorieten & Wishlist systeem

**Als gebruiker** wil ik **cursussen kunnen markeren als favoriet en toevoegen aan een wishlist** zodat ik **een persoonlijke collectie kan maken van cursussen die me interesseren**.

**Acceptatiecriteria:**

- Elke cursuskaart heeft een "favoriet" (hartje) én "wishlist" knop
- Deze knoppen zijn alleen zichtbaar wanneer ingelogd
- Aparte pagina's of tabs voor "Mijn Favorieten" en "Mijn Wishlist"
- Mogelijkheid om item van wishlist naar favorieten te verplaatsen (of andersom)
- Badge in navigatie toont aantal items
- Data wordt per gebruiker opgeslagen in localStorage
- Bij logout blijven favorieten/wishlist bewaard voor die gebruiker
- Bij nieuwe login worden eigen favorieten/wishlist weer geladen

### User Story 11: Review & Rating systeem

**Als gebruiker** wil ik **reviews kunnen lezen en schrijven voor cursussen** zodat ik **geïnformeerde beslissingen kan maken op basis van ervaringen van anderen**.

**Acceptatiecriteria:**

- Sterren rating systeem (1-5 sterren) per cursus
- Mogelijkheid om geschreven reviews toe te voegen
- Reviews tonen met gebruikersnaam, datum, rating en tekst
- Filter cursussen op minimale rating
- Review form met validatie (vereiste velden, karakterlimiet)
- Elke gebruiker kan maar 1 review per cursus schrijven
- Edit/delete eigen review
- Reviews opslaan in localStorage

### User Story 12: Shopping Cart functionaliteit

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

---

## Could-have Features (Prioriteit 3)

### User Story 13: "Quick Start" Cursus Suggestie

**Als nieuwe gebruiker** wil ik **een "Begin hier" suggestie zien** zodat ik **weet waar ik moet starten**.

**Acceptatiecriteria:**

- Banner/card bovenaan dashboard met "Aanbevolen voor jou" cursus
- Logica: toon random beginner cursus met hoogste rating
- "Start deze cursus" call-to-action knop
- Optie om suggestie te dismissen
- Na dismiss wordt een nieuwe suggestie getoond
- Dismissed cursussen worden onthouden (localStorage)

### User Story 14: Completion Badges / Achievements

**Als gebruiker** wil ik **badges verdienen** zodat ik **gemotiveerd blijf om cursussen af te maken**.

**Acceptatiecriteria:**

- Badges verdienen bij mijlpalen:
  - "First Step" - eerste cursus bekeken
  - "Knowledge Seeker" - 5 cursussen bekeken
  - "Expert" - 10 cursussen bekeken
  - "Category Master" - alle cursussen in 1 categorie bekeken
- Badge collectie pagina of sectie
- Notification/toast wanneer badge wordt verdiend
- Badges opslaan in localStorage
- Visuele badges (emoji's of icons zijn genoeg)

### User Story 15: Gebruikersprofielen & Dashboard

**Als gebruiker** wil ik **een persoonlijk profiel en dashboard** zodat ik **mijn leervoortgang kan bijhouden en beheren**.

**Acceptatiecriteria:**

- Gebruikersprofiel pagina met avatar upload (via file input)
- Dashboard met overzicht van: ingeschreven cursussen, favorieten, wishlist, reviews
- Leervoortgang tracking per cursus (percentage completed)
- Totale leertijd bijhouden
- Persoonlijke statistieken (aantal cursussen, gemiddelde rating gegeven, etc.)
- Profile edit functionaliteit
- Data opslaan in localStorage met complexe user object

### User Story 16: Recently Viewed & Recommendations

**Als gebruiker** wil ik **recent bekeken cursussen zien en aanbevelingen krijgen** zodat ik **gemakkelijk kan terugkeren naar interessante content**.

**Acceptatiecriteria:**

- "Recently viewed" sectie die laatste 5-10 bekeken cursussen toont
- Aanbevelingen gebaseerd op bekeken cursussen (zelfde categorie/instructor)
- "Omdat je X bekeken hebt" sectie
- Slimme algoritme voor aanbevelingen (gebruik localStorage data)
- Mogelijkheid om recent viewed te wissen
- Time-based filtering (laatste week, maand)

### User Story 17: Advanced Search & Autocomplete

**Als gebruiker** wil ik **geavanceerde zoekmogelijkheden met suggesties** zodat ik **efficiënt kan vinden wat ik zoek**.

**Acceptatiecriteria:**

- Autocomplete dropdown met suggesties tijdens typen
- Zoekgeschiedenis opslaan en tonen
- "Did you mean..." functionaliteit voor typos
- Zoeken in titel, beschrijving, instructor naam, en tags
- Search highlights in resultaten
- Voice search functionaliteit (Web Speech API)
- Advanced search modal met filters gecombineerd

### User Story 18: Protected Routes & Navigation Guards

**Als systeem** wil ik **bepaalde pagina's alleen toegankelijk maken voor ingelogde gebruikers** zodat **niet-ingelogde gebruikers geen toegang hebben tot persoonlijke features**.

**Acceptatiecriteria:**

- Routes zoals /profile, /favorites, /wishlist, /cart zijn protected
- Bij poging om protected route te bezoeken zonder login: redirect naar /login
- Na succesvolle login: redirect naar de pagina waar gebruiker naartoe wilde
- Toast/melding: "Je moet ingelogd zijn om deze pagina te bekijken"
- Navigatie items voor protected pages alleen tonen wanneer ingelogd

---