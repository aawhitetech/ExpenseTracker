# Expense Tracker App Setup Guide

This guide provides step-by-step instructions to set up and run the Expense Tracker App using C# .NET 7 MVC and Microsoft SQL Server.
Prerequisites

Before you begin, ensure you have the following:

- [Visual Studio / VSCode](https://visualstudio.microsoft.com/downloads/)
- [Microsoft SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads) - See also [Running MSSQL with Docker](docs/SETUP_DB.md)
- [.NET 7 SDK](https://dotnet.microsoft.com/download/dotnet/7.0)

## Setup Steps

1. Clone the Repository:
Open your terminal or command prompt. Run the following command to clone the repository:

    `git clone https://github.com/aawhitetech/expense-tracker.git`

2. Navigate to the project directory:

    `cd expense-tracker`

3. Open the Solution in Visual Studio:

    Launch Visual Studio.
    Open the solution file ExpenseTrackerApp.sln.

4. Configure Database Connection:

    Open the appsettings.json file in the ExpenseTrackerApp project.
    Replace the placeholder in "DefaultConnection" with your SQL Server connection string.

5. Build and Run the Application:

    Build the solution by clicking on the Build button in Visual Studio.
    Start the application by pressing F5 or clicking the Start button.
    
    Alternatively, you can use the cli commands:

    `dotnet build`

    `dotnet run`

6. The app should open in your default web browser at http://localhost:port.

7. Register and Log In:

    Register a new account or log in using existing credentials.

8. Adding Expenses:

    Log your expenses by navigating to the Expenses section and adding new transactions.
    Categorize expenses and provide details like amount, description, and date.

9. Setting Budgets:

    Navigate to the Budgets section and set budgets for different expense categories.

10. Visualize Spending Patterns:

    Explore the provided charts and graphs to visualize your spending patterns.