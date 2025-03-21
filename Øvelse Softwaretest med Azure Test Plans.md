# 🧪 Øvelser i Softwaretest – uden kode (Guidet version)

Denne fil indeholder en række testtyper, som en softwareudvikler bør kende – og øvelser til at forstå og anvende dem. Øvelserne er målrettet 2. semester datamatikerstuderende og gennemføres i Azure DevOps.

## 🧱 Produktbeskrivelse

I dette forløb tager vi udgangspunkt i et fiktivt produkt: **PizzaPortalen** – en webapplikation hvor brugere kan:
- Oprette en brugerprofil
- Logge ind og ud
- Bestille pizza
- Se deres ordrestatus
- Opdatere deres oplysninger

Formålet er at lære at designe og udføre forskellige testtyper, som bruges i softwareudvikling, uden at skulle skrive kode. I vil simulere test af dele af PizzaPortalen baseret på krav og scenarier.

---

## 🔍 Oversigt over testtyper

| Testtype             | Formål                                                                 |
|----------------------|------------------------------------------------------------------------|
| **Manuel test**       | Gennemgang af funktionalitet vha. testcases udført manuelt             |
| **Exploratory test**  | Fri test uden faste scripts for at finde skjulte fejl og mangler       |
| **Use case-test**     | Validering af om et specifikt bruger-scenarie fungerer som forventet   |
| **Acceptance test**   | Validering af funktionalitet ift. krav fra kunde/forretning            |
| **UI/UX test**        | Test af brugergrænseflade og brugeroplevelse                           |
| **Regression test**   | Kontrol af at eksisterende funktioner stadig virker efter ændringer    |
| **Smoke test**        | Hurtig test af om systemet overhovedet virker ved opstart              |
| **Boundary test**     | Test af grænseværdier for input og funktionalitet                      |

---

## 🧪 Øvelser til testtyperne

*(Alle øvelser er relateret til PizzaPortalen med fokus på forskellige aspekter af test.)*

### 🔹 Øvelse 1: Manuel test

**🎯 Læringsmål:** Forstå opbygning og udførelse af en test case.  
**🧠 Hvorfor lære dette?** Testplaner strukturerer testarbejde og sikrer, at funktionalitet bliver dokumenteret og verificeret.

**📦 Metadata:**
- Fokus: Strukturering og eksekvering af tests
- Relevans: Grundlæggende testdisciplin
- Forventet udbytte: Forståelse for trinvise test cases og deres betydning

**Sådan gør du i Azure DevOps:**

1. Log ind på [https://dev.azure.com](https://dev.azure.com)
2. Gå til dit projekt og vælg **Test Plans** i venstremenuen
3. Klik på **New Test Plan**, navngiv planen (f.eks. “Login Test”) og klik **Create**
4. Klik **+ New Suite** > vælg *Static suite* > navngiv suiten “Gyldigt login”
5. Klik **+ New Test Case** og opret trin såsom:
   - Gå til login-side
   - Indtast gyldigt brugernavn og kodeord
   - Klik på login-knappen
   - Tjek om dashboard vises
6. Klik på **Run for web application** for at udføre testen
7. Marker hvert trin som "Passed" eller "Failed", og gem testen

---

### 🔹 Øvelse 2: Exploratory test

**🎯 Læringsmål:** Udvikle evne til at opdage fejl uden en fast plan.  
**🧠 Hvorfor lære dette?** Exploratory testing kan afdække uventede fejl og brugeradfærd.

**📦 Metadata:**
- Fokus: Intuitiv test og observation
- Relevans: Hurtig fejlfinding
- Forventet udbytte: Forståelse af uforudsete problemer og adfærd

**Sådan gør du i Azure DevOps:**

1. Gå til **Test Plans** > klik på **Runs** > vælg **Exploratory Testing**
2. Start en ny session og vælg det relevante system eller webapp
3. Brug applikationen frit i 15-20 minutter – klik rundt og prøv forskellige funktioner
4. Undervejs: Notér hvad du gør og hvilke problemer du finder
5. Brug **Session notes** til at dokumentere observationer
6. Tilføj screenshots og kommentarer

---

### 🔹 Øvelse 3: Use Case-test

**🎯 Læringsmål:** Forstå hvordan brugsscenarier kan bruges til at designe test.  
**🧠 Hvorfor lære dette?** Use cases fokuserer på brugerens behov.

**📦 Metadata:**
- Fokus: Fra use case til testcase
- Relevans: Kobling mellem analyse og test
- Forventet udbytte: Evne til at teste ud fra brugsscenarier

**Sådan gør du i Azure DevOps:**

1. Find et use case-diagram, fx fra et tidligere projekt eller fra pensum (eksempel: “Bruger bestiller pizza”).
2. Log ind på [https://dev.azure.com](https://dev.azure.com)
3. Gå til **Test Plans** i venstremenuen og klik på **New Test Plan**
4. Navngiv testplanen (fx "Pizza-bestilling Use Case") og klik **Create**
5. Klik **+ New Suite** > vælg *Static suite* > navngiv suiten efter din use case (fx "Bestil pizza")
6. Inde i suiten, klik **+ New Test Case** for hvert trin i use casen:
   - Eksempel:
     - Åbn pizzamenu
     - Vælg pizza
     - Læg i kurv
     - Gå til betaling
     - Gennemfør bestilling
7. Klik **Run for web application** for at udføre testen
8. Marker hvert trin som "Passed" eller "Failed"
9. Gem og reflekter: Virkede det som forventet? Notér evt. problemer eller forbedringsforslag

---

### 🔹 Øvelse 5: UI/UX test

**🎯 Læringsmål:** Forstå hvordan man evaluerer en brugergrænseflade og brugeroplevelse.  
**🧠 Hvorfor lære dette?** En god UI/UX er afgørende for brugerens tilfredshed og systemets brugbarhed.

**📦 Metadata:**
- Fokus: Visuelt design og navigation
- Relevans: Brugbarhedstest uden kode
- Forventet udbytte: Viden om brugeradfærd og forbedringsforslag til design

**Sådan gør du:**

1. Brug en klikbar prototype af PizzaPortalen i fx Figma eller Adobe XD (du kan også bruge screenshots af webappen)
2. Arbejd sammen to og to:
   - A er testbruger, B er observatør
3. A får følgende opgave: “Find og bestil en pepperoni-pizza”
4. B observerer og noterer:
   - Hvor A klikker først
   - Forvirring, fejlplacering, uventede reaktioner
5. Efter testen udveksler I roller
6. Sammenlign jeres oplevelser og skriv 3 forbedringsforslag
7. **Brug ikke Azure Test Plans** i denne øvelse – dokumentér i en delt note eller .md-fil

---

### 🔹 Øvelse 6: Regression test

**🎯 Læringsmål:** Forstå hvordan man gentester eksisterende funktionalitet efter ændringer.  
**🧠 Hvorfor lære dette?** Regressionstest sikrer, at nye ændringer ikke bryder noget eksisterende.

**📦 Metadata:**
- Fokus: Genbrug og validering af tidligere funktionalitet
- Relevans: Centrale tests før releases
- Forventet udbytte: Praktisk erfaring med tests før/efter ændringer

**Sådan gør du i Azure DevOps:**

1. Få udleveret:
   - En video eller demo-link til version 1 (før ændringer)
   - En version 2 med ny funktionalitet (fx tilføjet “valgfri toppings”)
2. Opret en **New Test Plan** kaldet "Regression Test - PizzaPortalen"
3. Klik på **+ New Suite** og navngiv den “Tidligere funktioner”
4. Klik **+ New Test Case** for funktioner som:
   - Opret bruger
   - Bestil pizza
   - Se ordrehistorik
5. Udfør testene på den nye version (version 2)
   - Klik på testcasen > vælg **Run for web application**
   - Marker hvert trin og kommentér evt. forskelle
6. Vurder: Virker funktionaliteten stadig som i version 1?
7. Dokumentér alt i testplanen og del konklusioner med holdet

---

### 🔹 Øvelse 7: Smoke test

**🎯 Læringsmål:** Forstå hvordan man hurtigt kan teste om systemet overhovedet fungerer.  
**🧠 Hvorfor lære dette?** Smoke tests afslører kritiske fejl før mere detaljeret test påbegyndes.

**📦 Metadata:**
- Fokus: Overfladisk og bred funktionstest
- Relevans: Første test ved ny version/deployment
- Forventet udbytte: Evne til hurtigt at validere systemets grundlæggende sundhed

**Sådan gør du i Azure DevOps:**

1. Tjek at du har adgang til den nyeste version af PizzaPortalen (eller en demo)
2. Lav en tjekliste med kritiske funktioner, fx:
   - Loader forsiden?
   - Kan man logge ind?
   - Kan man se pizzamenuen?
3. Opret en **Test Plan** kaldet “Smoke Test – PizzaPortalen”
4. Klik **+ New Suite** > vælg *Static suite* og navngiv den “Basistest”
5. Klik **+ New Test Case** og opret testcases ud fra din tjekliste
6. Kør testene og noter:
   - Hvad virker?
   - Er der kritiske fejl?
   - Er noget utilgængeligt?

---

### 🔹 Øvelse 8: Boundary test

**🎯 Læringsmål:** Forstå hvordan man identificerer og tester grænseværdier.  
**🧠 Hvorfor lære dette?** Grænseværdier er typiske fejlområder, især i formularer og inputfelter.

**📦 Metadata:**
- Fokus: Input-validering og robusthed
- Relevans: Undgår fejl og sikrer kvalitet ved yderpunkter
- Forventet udbytte: Erfaring med grænsesøgning i testdesign

**Sådan gør du i Azure DevOps:**

1. Forestil dig at PizzaPortalen kræver alder 18–99 ved registrering
2. Opret en **Test Plan** kaldet “Boundary Test – Brugeroprettelse”
3. Klik **+ New Suite** > vælg *Static suite* > navngiv den “Alder”
4. Opret følgende test cases:
   - Indtast alder 17 → forvent “Afvises”
   - Indtast alder 18 → forvent “Accepteres”
   - Indtast alder 99 → forvent “Accepteres”
   - Indtast alder 100 → forvent “Afvises”
5. Klik på hver test case > **Run for web application** og test resultaterne
6. Vurder: Giver systemet tydelig feedback? Kan man snyde valideringen?
7. Dokumentér konklusioner og forslag til forbedring

---

Nu er alle øvelser samlet med trin-for-trin-instruktioner.

---

🚧 **Opdatering i gang:** Øvelse 5–8 er under revidering for at inkludere:
- Anvendelse (eller fravalg) af Azure Test Plans i UI/UX test
- Data og detaljeret vejledning for regression tests (før/efter-versioner, opbygning af suite, kørselsvejledning)
- Afklaring omkring anvendelighed af statiske suites i Smoke tests
- Udvidet metadata og trin i Boundary tests

Sig til, så færdiggør jeg det hele i næste skridt.

