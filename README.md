
# DotNet Crud Web Api Example

 A RESTful Web API using ASP.NET Core in .NET 8.0 alongside Entity Framework Core. 
 
 This project demonstrates a simple CRUD (Create, Read, Update, Delete) operation on movies, utilizing a SQLite database to persist data.

## Prerequisites

Before you begin, ensure you have the following installed:
- .NET 8.0 SDK
- Entity Framework Core CLI

You can install the EF Core CLI tool globally using:

```bash
dotnet tool install --global dotnet-ef
```

## Getting Started

To get a local copy up and running follow these simple steps:

1. **Clone the repository**

   ```bash
   git clone https:/github.com/Scribbio/DotNet-8-Crud-Web-API-Example.git
   ```

2. **Navigate to the project directory**

   ```bash
   cd DotNetCrudWebApi
   ```

3. **Install necessary packages**

   Make sure all the required NuGet packages are restored:

   ```bash
   dotnet restore
   ```

4. **Run Migrations**

   Apply the database migrations to set up your database schema:

   ```bash
   dotnet ef database update
   ```

   If your EF Core context and migrations are in a different project, specify the projects as follows:

   ```bash
   dotnet ef database update --project YourEFCoreProject --startup-project YourStartupProject
   ```

## Usage

Start the API locally by running:

```bash
dotnet run
```

Your API will be available at `http://localhost:5000` by default.

### API Endpoints

The following endpoints are available:

- `GET /api/Movies`: Retrieves a list of all movies.
- `GET /api/Movies/{id}`: Retrieves a specific movie by its ID.
- `POST /api/Movies`: Adds a new movie.
- `PUT /api/Movies/{id}`: Updates an existing movie.
- `DELETE /api/Movies/{id}`: Deletes a specific movie.

## License

Distributed under the MIT License. See `LICENSE` for more information.