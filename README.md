# Exam Portal

> ASP.NET Core online examination portal with admin, faculty and student roles.

![License](https://img.shields.io/badge/license-see%20upstream-lightgrey) ![Status](https://img.shields.io/badge/status-archived-lightgrey)

> **Fork** of [DroopyPirate/Exam-Portal](https://github.com/DroopyPirate/Exam-Portal). Credit for the original work goes to its authors.

## Overview

A web portal for creating and taking tests. Faculty build question banks and tests, assign them to groups of students, and students take them online with results tracked.

## Features

- Role-based access: super admin, admin, faculty, student (ASP.NET Identity)
- Question bank with tags, question types and descriptive answers
- Test creation and assignment to student groups
- Results tracking, including descriptive-answer grading
- Excel import and email (MailKit)

## Tech stack

| Area     | Tools                                         |
| -------- | --------------------------------------------- |
| Backend  | ASP.NET Core MVC (.NET 5), Entity Framework Core, Identity |
| Database | MySQL                                         |
| Frontend | Razor views, Gulp, LibMan                     |

## Getting started

### Prerequisites

- .NET 5 SDK, MySQL, Node.js (for Gulp assets)

### Installation

```sh
git clone https://github.com/Sakar1601/Exam-Portal.git
cd Exam-Portal
npm install
dotnet restore "Exam Portal.sln"
```

### Configuration

Set your MySQL connection string and email settings in `appsettings.Development.json`, then apply migrations and run:

```sh
dotnet ef database update
dotnet run
```

## Project structure

```
Controllers/   MVC controllers (Admin, Faculty, Student, Test, Group, Tag…)
Models/        Entity and Identity models
Repository/    Data access
Views/         Razor views per area
Migrations/    EF Core migrations
wwwroot/       Static assets
```

## Security

See [SECURITY.md](SECURITY.md). Keep connection strings and SMTP credentials out of source control.

## License

No license file is included in the upstream project, so all rights remain with the original authors. See the upstream repository.
