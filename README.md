WELCOME TO AGRI-ENERGY CONNECT PLATFORM WEB APPLICATION:
---------------------------------------------------------
INTRODUCTION:
--------------
The Agri-Energy Connect Platform is a web app developed using ASP. NET Core MVC with Visual Studio 2022 that enables 
its users to connect agricultural producers (Farmers) with employees or potential energy sector stakeholders. 
It offers secure login, registration and data management on behalf of farmers and products using SQLite, MVC architecture, 
Razor Pages, entity models and role based access.This README gives an in-depth explanation of how the application works, 
how it is built, and commands for running and testing the application on your own system.

BODY:
-----
Project Overview:
------------------
Technologies And Tools Used in this Project:
--------------------------------------------
-ASP.NET Core MVC (.NET 8.0)
-Entity Framework Core
-SQLite Database
-Razor Pages
-Identity Authentication (Login/Register)
-Bootstrap (for styling)
-Visual Studio 2022

Application Features:
---------------------
Secure user registration and login:
-----------------------------------
-Role-based access (Farmers & Employees)
-CRUD (Create, Read, Update, Delete) operations for:
-Farmers
-Products
-Informational pages:
-Home
-About Us
-Contact Us
-Local SQLite database
-Responsive UI design with Bootstrap
-Form validation
-Data persistence

Application Pages Breakdown:
----------------------------
1. Home Page:
-------------
-Displays an introduction to the Agri-Energy Connect Platform.
-Simple navigation bar to access other pages.
-Located in Views/Home/Index.cshtml.

2. About Us Page:
-----------------
-Describes the purpose and goals of the platform.
-Located in Views/Home/AboutUs.cshtml.

3. Contact Us Page:
-------------------
-Contains a form or information for users to reach the developers/admins.
-Located in Views/Home/ContactUs.cshtml.

4. Login & Register Pages:
--------------------------
-Handles user authentication with ASP.NET Identity.
-Located in Areas/Identity/Pages/Account.

5. Farmer Page:
---------------
-Allows users to add new farmers with fields like:
-Name
-Location
-Contact Info
-List of all farmers and actions for editing or viewing details.
-CRUD functions handled in FarmersController.cs.
-Views located in Views/Farmers.

6. Product Page:
----------------
-Allows users to add new products with fields like:
-Name
-Category
-Quantity
-Similar structure and behavior to the Farmer page.
-CRUD functions handled in ProductsController.cs.
-Views located in Views/Products.

🛠️ How the Application Works:
------------------------------
1. The application runs in the ASP.NET Core MVC framework.
2.Authentication is done through ASP.NET Identity and the database is SQLite.
3. When logged in, authenticated users may visit the Farmer and Product Management pages.
4.Data stored using EF Core and the local SQLite database.
5.Each controller runs logic for pages, but views use Razor syntax to render output.

💾 SQLite Local Database Setup:
-------------------------------
Step 1: Install SQLite and EF Core Tools
Make sure the following packages are installed in your project:
Command Prompts:
----------------
Microsoft.EntityFrameworkCore
Microsoft.EntityFrameworkCore.Sqlite
Microsoft.EntityFrameworkCore.Tools

Step 2: Define Your DbContext
Located in Data/ApplicationDbContext.cs:
CODE LOGIC FOR APPLICATIONDBCONTEXT FILE:
----------------------------------------
public class ApplicationDbContext : IdentityDbContext<ApplicationUser>
{
    public DbSet<Farmer> Farmers { get; set; }
    public DbSet<Product> Products { get; set; }
}

Step 3: Configure Connection String
In appsettings.json:
-------------------
Appsettings.json file:
----------------------
"ConnectionStrings": {
  "DefaultConnection": "Data Source=agri_energy.db"
}

Step 4: Apply Migrations & Update Database
Open the NuGet Package Manager Console:
-----------------------------------------
Command Prompots in the Package Manager console:
------------------------------------------------
Add-Migration InitialCreate
Update-Database

▶️ How to Run the Web Application in Visual Studio 2022:
--------------------------------------------------------
1.Open the .sln solution file in Visual Studio 2022.
2.Set the project as Startup Project.
3.Press Ctrl + F5 or click "Run Without Debugging".
4.The browser will open and navigate to the home page.
5.Register a new user or log in.
6.Navigate using the top navbar to test other pages.

✅ Best Practices Followed:
----------------------------
1.MVC architecture
2.Separation of concerns
3.Razor View Engines
4.Layouts with navigation bar and footer
5.Validations on form inputs
6.Organized folder structure

📌 Conclusion:
--------------
The Agri-Energy Connect Platform is an ASP. NET Core MVC project suitable for beginner to intermediate level students. 
This project provides a well structured basis for training in PHP and ASP. NET Core MVC. By learning ASP. NET Core MVC we can develop dynamic web apps dealing with the links between agriculture and energy.
The primary objective of this project is to introduce a live real-world Web app for collaboration in agriculture and energy. 
In fact we develop a integrated web application for full interoperability and information exchange among stakeholders in agriculture and energy project. 
Through modelling we intend to create a realistic and pragmatic environment, in which the complexity and challenges of these issues are reflected in our daily life.
It explains very clearly how secure user authentication, efficient data management, good user interface and integration with SQLite happen.
You need the README to get a really deep introduction and knowledge of the usage of the software. This includes setting it up, running it and understanding all the features.
If you want to use this web app for a college project, or wish to customize it with more features, it is an excellent framework with many functionalities readily available as it is used. 
Our idea was originally to design it for many functionalities, from education to research to any type of project possible. By being flexible and open to many possibilities, it provides both you and the project you wish to use it for great value.
strong foundation for database-driven, MVC-based web solutions.

GitHub Link to Web App:
https://github.com/KingLuqmaan123/ST10038389_PROG7311---POE-PART-2
