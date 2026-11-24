# Like Hero To Zero

Case study from my Bachelor of Science in Computer Science at IU International University of Applied Sciences, module *Programming of Industrial Information Systems with Java EE (IPWA02-01)*, December 2023. The project is a prototype and not meant for public use.

<p align="center">
  <img src="images/EmissionOverview.png" width="600" alt="Like Hero To Zero: emission overview">
</p>

A web front end for worldwide CO₂ emissions. Everyone can view the data. Registered users can log in to change and extend it. The prototype shows the emissions of the years 2018 to 2021, based on the public EDGAR dataset of the European Commission.

## Features

- **Public overview** of CO₂ emissions per country, shown in a PrimeFaces data table
- **Login** for registered users
- **Edit, delete and add** emission data with validation (for example, a country can only be added once and emissions must be valid numbers)

## Two versions

The repository contains the project in two development steps:

| Version | Data storage |
|---|---|
| **Without database** | Emissions and users are kept in a list inside the application. Data is lost when the server restarts. |
| **With database** | Emissions and users are stored in a MySQL database and loaded through Data Access Objects (DAO). |

The first version was used to build and test the pages, the login and the navigation. The second version replaces the lists with the database connection.

## Screenshots

<p align="center">
  <img src="images/AddEmission.png" width="650" alt="Adding data with validation messages">
</p>

## Built with

- Java EE with **JSF** (XHTML pages and beans) and **PrimeFaces**
- Maven project in Eclipse, running on an Apache **Tomcat** server
- **MySQL** with **EclipseLink** (ORM) for the database version

## Limitations

- Pages can be opened directly through the URL, which bypasses the login.
- Navigation with buttons and the `outcome` attribute is only a simple solution.
- Registered users change or delete data directly. There is no approval process.

## Author

Jule Engel
