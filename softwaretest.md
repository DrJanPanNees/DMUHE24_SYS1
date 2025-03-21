
# 🧪 Øvelser i Softwaretest – uden kode

Denne fil indeholder en række testtyper, som en softwareudvikler bør kende – og øvelser til at forstå og anvende dem. Øvelserne er målrettet 2. semester datamatikerstuderende.

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

- Giv studerende en simpel login-side (eller mock-up).
- Opgave: Udarbejd og udfør 3 manuelle test cases.
- Brug Azure Test Plans eller papirskabelon.

---

### 🔹 Øvelse 2: Exploratory test

**🎯 Læringsmål:** Udvikle evne til at opdage fejl uden en fast plan.  
**🧠 Hvorfor lære dette?** Exploratory testing kan afdække uventede fejl og brugeradfærd.

- Giv adgang til et simpelt demo-websystem.
- Studerende får 15 minutter til at “lege” og finde fejl.
- Dokumentér alt med screenshots og noter.
- Refleksion: Hvad blev opdaget, og hvorfor?

---

### 🔹 Øvelse 3: Use Case-test

**🎯 Læringsmål:** Forstå hvordan brugsscenarier kan bruges til at designe test.  
**🧠 Hvorfor lære dette?** Use cases fokuserer på brugerens behov.

- Giv et use case-diagram (fx "Bestil pizza").
- Studerende skriver en test case til at validere hele use casen.
- Test udføres manuelt eller via prototype (fx Figma).

---

### 🔹 Øvelse 4: Acceptance test

**🎯 Læringsmål:** Forstå forretningskrav og hvordan man bekræfter dem.  
**🧠 Hvorfor lære dette?** Accepterer funktionalitet set fra forretningens/kundens perspektiv.

- Giv en liste med 5 krav (fx “Bruger kan nulstille kodeord”).
- Studerende skriver 5 tilsvarende acceptance tests.
- Brug rollen som "kunde" og vurder testene i grupper.

---

### 🔹 Øvelse 5: UI/UX test

**🎯 Læringsmål:** Forstå hvordan visuel feedback og oplevelse testes.  
**🧠 Hvorfor lære dette?** UI/UX påvirker brugerens tilfredshed direkte.

- Giv en klikbar prototype i Figma.
- Studerende observerer hinanden: Hvad klikker brugeren først på?
- Dokumentér forvirring og UX-fejl.
- Fremlæggelse i grupper.

---

### 🔹 Øvelse 6: Regression test

**🎯 Læringsmål:** Genteste eksisterende funktionalitet efter ændringer.  
**🧠 Hvorfor lære dette?** Tidligere funktioner må ikke gå i stykker efter opdateringer.

- Giv før-/efter-screenshots af et system.
- Studerende sammenligner og dokumenterer ændringer.
- Hvad virker stadig? Hvad er brudt?

---

### 🔹 Øvelse 7: Smoke test

**🎯 Læringsmål:** Forstå idéen med hurtig "sundhedstest".  
**🧠 Hvorfor lære dette?** Hurtig afklaring: virker systemet grundlæggende?

- Giv et system og en liste: "Loader forsiden? Virker login?"
- Studerende checker hvert punkt og markerer status.

---

### 🔹 Øvelse 8: Boundary test

**🎯 Læringsmål:** Identificere og teste grænseværdier.  
**🧠 Hvorfor lære dette?** Grænseværdier er typiske fejlområder i software.

- Fx: Et system tillader alder 18–99 år.
- Test: 17, 18, 99, 100.
- Hvad accepteres og hvad afvises?

---

God fornøjelse med testarbejdet!
