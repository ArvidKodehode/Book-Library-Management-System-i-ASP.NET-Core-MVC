# Book Library Management System - SQLite Setup

## 📌 Introduction
This project is an ASP.NET Core MVC-based **Book Library Management System**, which allows users to preview, download, add, edit, and delete eBooks. The system is now configured to use **SQLite** as the database backend.

---

## 📌 Project Setup
### 🔹 1. Clone the Repository
```
git clone https://github.com/your-repository.git
cd BookLibraryManagementSystem
```

### 🔹 2. Install Required NuGet Packages
Ensure you have the necessary NuGet packages installed:
```
Install-Package Microsoft.EntityFrameworkCore.Sqlite
Install-Package Microsoft.EntityFrameworkCore.Design
```

---

## 📌 Configurations
### 🔹 3. Update `appsettings.json`
Modify the database connection string in `appsettings.json` to point to the SQLite database:
```json
{
    "ConnectionStrings": {
        "DefaultConnection": "Data Source=C:\\Users\\arvid\\OneDrive\\asp.net\\BookLibraryManagementSystem\\EBooksLibrary.db"
    },
    "Logging": {
        "LogLevel": {
            "Default": "Information",
            "Microsoft.AspNetCore": "Warning"
        }
    },
    "AllowedHosts": "*"
}
```

---

### 🔹 4. Update `Program.cs`
Replace SQL Server configuration with SQLite:
```csharp
using BookLibraryManagementSystem.Data;
using Microsoft.EntityFrameworkCore;

var builder = WebApplication.CreateBuilder(args);

// SQLite Database Connection
var connectionString = builder.Configuration.GetConnectionString("DefaultConnection");
builder.Services.AddDbContext<ApplicationDbContext>(options =>
    options.UseSqlite(connectionString));

builder.Services.AddControllersWithViews();
var app = builder.Build();

if (!app.Environment.IsDevelopment())
{
    app.UseExceptionHandler("/Home/Error");
}

app.UseStaticFiles();
app.UseRouting();
app.UseAuthorization();

app.MapControllerRoute(
    name: "default",
    pattern: "{controller=Home}/{action=Index}/{id?}");

app.Run();
```

---

### 🔹 5. Update Entity Framework Core Database
To create the SQLite database, run the following commands in **Package Manager Console**:
```
Add-Migration InitialCreate
Update-Database
```
This will generate the `EBooksLibrary.db` file in the project directory.

---

### 🔹 6. Run the Project
Start the application in Visual Studio:
```
F5 (Debug Mode)
```
Open your browser and go to:
```
http://localhost:{PORT}/Books
```

---

## 📌 Next Steps
- Implement book rating functionality.
- Improve UI with Bootstrap styling.
- Add authentication & admin panel.

🚀 **The SQLite setup is now complete!**

