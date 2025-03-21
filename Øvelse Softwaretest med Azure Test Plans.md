# 🧪 Øvelser i Softwaretest – uden kode (Guidet version)

Denne fil indeholder en række testtyper, som en softwareudvikler bør kende – og øvelser til at forstå og anvende dem. Øvelserne er målrettet 2. semester datamatikerstuderende og gennemføres i Azure DevOps.

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

### 🔹 Øvelse 1: Manuel test

**🎯 Læringsmål:** Forstå opbygning og udførelse af en test case.  
**🧠 Hvorfor lære dette?** Testplaner strukturerer testarbejde og sikrer, at funktionalitet bliver dokumenteret og verificeret.

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

### 🔹 Øvelse 4: Acceptance test

**🎯 Læringsmål:** Forstå forretningskrav og hvordan man bekræfter dem.  
**🧠 Hvorfor lære dette?** Tester funktionalitet set fra forretningens/kundens perspektiv.

**Sådan gør du i Azure DevOps:**

1. Få en liste med funktionelle krav (fx "Bruger skal kunne ændre kodeord")
2. Gå til **Test Plans** og klik på **New Test Plan**, navngiv den fx "Acceptance Test"
3. Klik på **+ New Suite** for hvert krav og navngiv efter funktion (fx "Ændre kodeord")
4. Tilføj **New Test Case** for hvert krav:
   - Beskriv trin og forventet resultat
5. Udfør testene med **Run for web application**
6. Marker hvert trin og vurder om kravet er opfyldt
7. Del dine resultater med en "kunde" (klassekammerat i rollen)

---

### 🔹 Øvelse 5: UI/UX test

**🎯 Læringsmål:** Test af brugergrænseflade og oplevelse.  
**🧠 Hvorfor lære dette?** UI/UX påvirker direkte brugerens oplevelse.

**Sådan gør du:**

1. Brug en klikbar prototype i fx Figma eller Adobe XD
2. Arbejd to og to – én tester, én observerer
3. Testeren får en opgave (fx "Find kontaktoplysninger")
4. Observatøren noterer:
   - Hvor brugeren klikker først
   - Eventuel forvirring eller fejlplaceringer
5. Sammenlign notater og skriv 3 forbedringsforslag

---

### 🔹 Øvelse 6: Regression test

**🎯 Læringsmål:** Genteste eksisterende funktionalitet efter ændringer.  
**🧠 Hvorfor lære dette?** Sikrer at ny kode ikke ødelægger eksisterende funktionalitet.

**Sådan gør du i Azure DevOps:**

1. Få adgang til to versioner af samme app (før og efter ændring)
2. Lav en liste over funktioner der bør virke
3. Opret **New Test Plan** kaldet "Regression Test"
4. Lav én suite med flere test cases der dækker de eksisterende funktioner
5. Udfør testen i den nye version
6. Noter: Hvad virker stadig, og hvad er gået i stykker?

---

### 🔹 Øvelse 7: Smoke test

**🎯 Læringsmål:** Forstå idéen med hurtig "sundhedstest".  
**🧠 Hvorfor lære dette?** Afklarer hurtigt om systemet er testklart efter deployment.

**Sådan gør du i Azure DevOps:**

1. Lav en kort tjekliste: "Loader forsiden?", "Virker login?", "Vises navigationen?"
2. Opret en **Test Plan** kaldet "Smoke Test"
3. Opret en enkel **Static suite** og test cases ud fra listen
4. Udfør testen efter ny deployment
5. Dokumenter status: Passed/Failed og noter evt. kritiske fejl

---

### 🔹 Øvelse 8: Boundary test

**🎯 Læringsmål:** Identificere og teste grænseværdier.  
**🧠 Hvorfor lære dette?** Grænseværdier er hyppige fejlområder i software.

**Sådan gør du:**

1. Eksempel: Et felt tillader alder 18–99
2. Opret en testplan og suite kaldet "Boundary Test"
3. Tilføj 4 test cases:
   - Indtast alder 17 → forvent "Afvises"
   - Indtast alder 18 → forvent "Accepteres"
   - Indtast alder 99 → forvent "Accepteres"
   - Indtast alder 100 → forvent "Afvises"
4. Udfør og dokumenter resultatet i Azure DevOps

---

Nu er alle øvelser samlet med trin-for-trin-instruktioner.

