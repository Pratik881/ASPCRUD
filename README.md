# CategoryCRUD

## Description
This is an ASP.NET Core MVC web application that uses Entity Framework Core with SQL Server for data access. The application is styled with Bootstrap for a responsive design.



## Prerequisites
Before you begin, ensure you have met the following requirements:
- .NET SDK (6.0 or later)
- SQL Server
- Visual Studio (or any compatible IDE)

## Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Pratik881/CategoryCRUD.git
   ```

2. **Set up the database:**
   - Open `appsettings.Development.json` and update the connection string to match your SQL Server setup
   - Open Package Manager Console and run the following commands:
     ```bash
     dotnet ef migrations add InitialCreate
     dotnet ef database update
     ```

3. **Build and run the application:**
   ```bash
   dotnet build
   dotnet run
   ```

## Project Structure
```
CategoryCRUD/
├── Controllers/
│   └── CategoryController.cs
├── Models/
│   └── Category.cs
├── Data/
│   └── ApplicationDbContext.cs
├── Views/
│   └── Category/
│       ├── Index.cshtml
│       ├── Create.cshtml
│       ├── Edit.cshtml
│       └── Delete.cshtml
└── wwwroot/
    ├── css/
    └── js/
```

## Database Configuration
The application uses SQL Server. Update the connection string in `appsettings.Development.json`:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=(localdb)\\mssqllocaldb;Database=CategoryCRUD;Trusted_Connection=True;MultipleActiveResultSets=true"
  }
}
```

## Usage
1. Launch the application
2. Navigate to the Categories page
3. Use the interface to:
   - View all categories
   - Create new categories
   - Edit existing categories
   - Delete categories

