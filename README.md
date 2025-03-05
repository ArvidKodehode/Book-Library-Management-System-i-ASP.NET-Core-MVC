# Book Library Management System

## 📌 Prosjektoversikt
Dette prosjektet er en **ASP.NET Core MVC-basert** bokbibliotek-administrasjonssystem som lar brukere:
- Legge til, redigere og slette e-bøker
- Forhåndsvise og laste ned bøker
- Vise en liste over tilgjengelige bøker
- Valgfritt: Gi bøker en stjernerangering ⭐⭐⭐⭐⭐

## 📌 Hva vi har gjort
✔ Opprettet ASP.NET Core MVC-struktur
✔ Implementert SQLite som database (EBooksLibrary.db)
✔ Laget `ApplicationDbContext` for databaseforbindelse
✔ Konfigurert Entity Framework Core for migrasjoner
✔ Opprettet grunnleggende Views, Controllers og Models
✔ Installert nødvendige **NuGet-pakker**:
   - `Microsoft.EntityFrameworkCore.Sqlite`
   - `Microsoft.EntityFrameworkCore.Design`

## 📌 Viktige ting å huske
- **Bruk relativ databasebane** (`EBooksLibrary.db`) slik at prosjektet er portabelt
- **Migrations må kjøres** (`Add-Migration` og `Update-Database`) ved endringer i modellen
- **Prosjektet startes via Visual Studio** med `F5`
- **UI kan forbedres** med Bootstrap og CSS

## 📌 Hva som gjenstår
🔹 Legge til bedre styling og UI-forbedringer
🔹 Implementere bok-rangering (stjerner)
🔹 Legge til en tilbakemeldingsseksjon for brukere
🔹 Mulighet for brukerautentisering (valgfritt)

🚀 **Prosjektet er godt i gang – snart ferdig!**
