# Casebeskrivelse: Grise Fodringssystem

## Baggrund

Virksomheden Agrisys ønsker at få udviklet et system til at overvåge fodringen af grise. Agrisys er en førende leverandør af teknologiske løsninger til landbruget, der specialiserer sig i automatiserede fodrings- og overvågningssystemer. De arbejder tæt sammen med landmænd for at optimere dyrevelfærd og produktivitet gennem avanceret dataanalyse og IoT-baserede løsninger. Systemet skal hjælpe med at analysere og visualisere fodringsdata samt give advarsler, hvis en gris ikke har spist nok de sidste 3 dage. Data er tilgængelig i en Excel-fil, som systemet skal kunne importere. Mere information om virksomheden findes på [www.agrisys.dk](https://www.agrisys.dk).

## Systemkrav

### 1. Datahåndtering

- Systemet skal kunne læse og vise data fra en Excel-fil.
- Data skal lagres i en MSSQL-database.

### 2. Brugerroller

- **Superbruger**: Kan oprette dashboards og widgets til at overvåge fodringsmønstre.
- **Bruger**: Kan se dashboards og overvåge grisenes fodringstilstand.

### 3. Dashboards og KPI Widgets

- Dashboards skal visualisere fodringsmønstre og grisenes vægtøgning via **JavaFX-grafer og widgets**.
- Superbrugeren skal kunne tilpasse dashboards med forskellige KPI’er.

### 4. Advarselsfunktion

- Systemet skal registrere og advare, hvis en gris har spist under et minimum de sidste 3 dage.
- Bruger skal kunne se en liste over grise med advarsler.

### 5. Simulering af drift (Bonusopgave)

- Studerende skal udvikle en funktion, der simulerer fodringsforløb for en gris over en periode og genererer data baseret på realistiske fodringsmønstre.

### 6. Eksportfunktion

- Systemet skal kunne eksportere fodringsdata og analyser til CSV-filer.

## Teknologier

- **Programmeringssprog:** Java
- **UI Framework:** JavaFX
- **Database:** MSSQL Server
- **Diagrammer:** UML-diagrammer til systemarkitektur
- **ER-diagram:** Database design
- **Systemudviklingsmetode:** Studerende skal vælge en metode og begrunde valget

## Arbejdsopgaver til jer

1. Importér data fra Excel og vis det i systemet.
2. Design en MSSQL-database til at lagre fodringsdata.
3. Implementér brugerroller og adgangskontrol.
4. Udvikl JavaFX-widgets til dashboard-visualisering.
5. Implementér advarselsfunktion for grise med lav fodring.
6. Implementér CSV-eksportfunktion.
7. Udarbejd UML- og ER-diagrammer for systemet.
8. Skriv en rapport om den valgte systemudviklingsmetode.
9. (Bonus) Implementér en simulering af fodringsdrift.

## Forventet resultat

I skal udvikle en fungerende prototype af systemet med en database og et JavaFX-brugerinterface. Projektet evalueres på kodens kvalitet, systemarkitektur, databaseimplementering og rapportering.

## Leverables

- Kørende JavaFX-applikation med databaseintegration
- UML- og ER-diagrammer
- Systemdokumentation
- Præsentation af løsningen

---

## Systemarkitektur (ASCII Diagram)

```
+-----------------------------+
|     [Excel-fil input]      |
|  Fodringsdata (.xlsx/.csv) |
+-------------+--------------+
              |
              v
+-------------+--------------+
|     [Importmodul]         |
| - Læser Excel-filer       |
| - Validerer data          |
+-------------+--------------+
              |
              v
+-------------+--------------+
|     [Database: MSSQL]     |
| - Gemmer fodringsdata     |
| - Tabeller: Grise, Fodring|
+-------------+--------------+
              |
        +-----+-----+
        |           |
        v           v
+--------+--+   +---+---------+
|  [Bruger-UI] | | [Admin-UI] |
|   (JavaFX)   | | (JavaFX)   |
| - Se grafer  | | - Redigér  |
| - Advarsler  | |   dashboards |
+--------------+ +-------------+
        |           |
        v           v
     +------------------------+
     |  [Dashboardmodul]      |
     | - JavaFX widgets       |
     | - KPI'er & grafer      |
     +------------------------+
              |
              v
     +------------------------+
     | [Advarselsmodul]       |
     | - Tjekker 3 dages data |
     | - Viser alarmer        |
     +------------------------+
              |
              v
     +------------------------+
     |  [CSV Eksportmodul]    |
     | - Genererer rapporter  |
     +------------------------+

        (Bonus)
              |
              v
     +------------------------+
     | [Simuleringsmodul]     |
     | - Genererer testdata   |
     +------------------------+
```

---

## Use-Case Diagram (ASCII)

```
          +-------------------+
          |     Superbruger   |
          +--------+----------+
                   |
          +--------v----------+
          | Opret Dashboard   |
          +-------------------+
                   |
          +--------v----------+
          | Konfigurer Widgets|
          +-------------------+

          +-------------------+
          |      Bruger       |
          +--------+----------+
                   |
          +--------v----------+
          | Se Dashboard      |
          +-------------------+
                   |
          +--------v----------+
          | Modtag Advarsler  |
          +-------------------+

   (Systemfunktioner i brug af begge roller)

          +-------------------+
          | Importér Data     |
          +-------------------+
                   |
          +--------v----------+
          | Eksportér CSV     |
          +-------------------+
                   |
          +--------v----------+
          | Simuler Fodring   |
          +-------------------+
```

---

