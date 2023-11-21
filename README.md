# ASP.NET-WebAPI-with-Azure-SQL-Database
# ASP.NET Web API with Azure SQL Database

This repository contains a sample ASP.NET Web API project that connects to an Azure SQL Database to perform CRUD operations on a "Customers" table. The API allows you to retrieve a list of customers, get a customer by ID, create a new customer, and delete a customer.

## Prerequisites

Before getting started, ensure that you have the following prerequisites:

1. **Azure SQL Database:** Set up an Azure SQL Database in the Azure portal. Make note of the connection string.

2. **Azure Data Studio:** Use Azure Data Studio to manage and interact with your Azure SQL Database.

3. **Visual Studio:** This project was developed using Visual Studio. Ensure you have it installed on your machine.

4. **Git:** Install Git on your machine to clone this repository.

## Steps to Set Up the Project

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd <repository-directory>
```

### Step 2: Open Project in Visual Studio

Open the project in Visual Studio by double-clicking the `.csproj` file or using the command:

```bash
start <your-project-name>.csproj
```

### Step 3: Set Database Connection String

In the `appsettings.json` file, replace the `<your-connection-string>` placeholder with the connection string for your Azure SQL Database.

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "<your-connection-string>"
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

### Step 4: Run the Application

Run the application by pressing `F5` or using the Visual Studio toolbar.

The API will be hosted at `https://localhost:5001` by default.

## API Endpoints

### Get Customers

```http
GET https://localhost:5001/api/customers
```

Retrieves a list of all customers.

### Get Customer by ID

```http
GET https://localhost:5001/api/customers/GetCustomerById?id={id}
```

Retrieves a customer by their ID.

### Create Customer

```http
POST https://localhost:5001/api/customers
```

Creates a new customer. Send a JSON payload in the request body.

### Delete Customer

```http
DELETE https://localhost:5001/api/customers/{id}
```

Deletes a customer by their ID.

## Conclusion

Congratulations! You have successfully set up an ASP.NET Web API connected to an Azure SQL Database using Visual Studio. The provided steps assume the usage of Visual Studio for development.
