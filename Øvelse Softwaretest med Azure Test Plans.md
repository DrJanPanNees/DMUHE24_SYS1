
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
2. Gå til dit projekt > klik på **Test Plans**
3. Klik på **New Test Plan**, navngiv den fx “Login Test”
4. Klik på **+ New Suite** > vælg *Static suite* > navngiv den “Gyldigt login”
5. Klik på **+ New Test Case** og tilføj trin:
   - Gå til login-side
   - Indtast gyldigt brugernavn og kodeord
   - Klik login
   - Tjek om dashboard vises
6. Gem og kør testen med **Run for web application**
7. Marker hvert trin som "Passed"/"Failed", og gem.

---

### 🔹 Øvelse 2: Exploratory test

**🎯 Læringsmål:** Udvikle evne til at opdage fejl uden en fast plan.  
**🧠 Hvorfor lære dette?** Exploratory testing kan afdække uventede fejl og brugeradfærd.

**Sådan gør du i Azure DevOps:**

1. Gå til **Test Plans**
2. Klik på **Exploratory testing** i menuen
3. Vælg det system eller prototype I tester
4. Klik rundt uden en plan – noter hvad du gør og hvad der sker
5. Brug **Session Notes** til at dokumentere fejl, forbedringer og observationer
6. Upload evt. screenshots

---

### 🔹 Øvelse 3: Use Case-test

**🎯 Læringsmål:** Forstå hvordan brugsscenarier kan bruges til at designe test.  
**🧠 Hvorfor lære dette?** Use cases fokuserer på brugerens behov.

**Sådan gør du:**

1. Få udleveret et use case-diagram (fx “Bruger bestiller pizza”)
2. Opret en testplan i Azure DevOps
3. Opret en suite pr. use case
4. Opret test cases, hvor hvert trin svarer til en del af use casen
5. Udfør testene og noter om det reelt fungerer

---

### 🔹 Øvelse 4: Acceptance test

**🎯 Læringsmål:** Forstå forretningskrav og hvordan man bekræfter dem.  
**🧠 Hvorfor lære dette?** Tester funktionalitet set fra forretningens/kundens perspektiv.

**Sådan gør du:**

1. Du får 5 forretningskrav (fx “Bruger kan ændre kodeord”)
2. Opret en testplan: “Acceptance Test”
3. For hvert krav: Opret en testsuite og tilføj test cases
4. Brug **Test Case**-feltet til at dokumentere forventede resultater
5. Udfør testen og vurder om kravene er opfyldt

---

### 🔹 Øvelse 5: UI/UX test

**🎯 Læringsmål:** Test af brugergrænseflade og oplevelse.  
**🧠 Hvorfor lære dette?** UI/UX påvirker direkte brugerens oplevelse.

**Sådan gør du:**

1. Brug en klikbar prototype (Figma, Adobe XD, e.l.)
2. Sid to og to – én er "bruger", én observerer
3. "Bruger" prøver at løse opgave (fx “Find kontaktoplysninger”)
4. “Observatør” dokumenterer, hvor der opstår forvirring
5. Sammen skriv forslag til forbedringer

---

### 🔹 Øvelse 6: Regression test

**🎯 Læringsmål:** Genteste eksisterende funktionalitet efter ændringer.  
**🧠 Hvorfor lære dette?** Sikrer at ny kode ikke ødelægger noget.

**Sådan gør du:**

1. Få adgang til to versioner af en applikation (før og efter opdatering)
2. Lav en liste over funktioner der skal retestes
3. Brug **Test Plans** og lav en testplan kaldet "Regression Test"
4. Udfør testene og marker hvad stadig virker – og hvad der er brudt

---

### 🔹 Øvelse 7: Smoke test

**🎯 Læringsmål:** Forstå idéen med hurtig "sundhedstest".  
**🧠 Hvorfor lære dette?** Afklarer om systemet overhovedet er testklart.

**Sådan gør du:**

1. Lav en kort liste: "Forside loader", "Login virker", "Menu fungerer"
2. I Azure DevOps, opret én suite kaldet “Smoke Test”
3. Opret en test case pr. punkt
4. Udfør testen efter ny version er deployeret
5. Marker hurtigt systemets tilstand

---

### 🔹 Øvelse 8: Boundary test

**🎯 Læringsmål:** Identificere og teste grænseværdier.  
**🧠 Hvorfor lære dette?** Grænseværdier er hyppige fejlområder.

**Sådan gør du:**

1. Scenarie: System accepterer alder mellem 18–99
2. Lav 4 test cases:
   - Alder = 17 (skal afvises)
   - Alder = 18 (skal accepteres)
   - Alder = 99 (skal accepteres)
   - Alder = 100 (skal afvises)
3. Brug testplanen “Boundary Test” og dokumentér resultat

---

God fornøjelse!
