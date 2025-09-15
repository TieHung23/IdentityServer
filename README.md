# 🛡️ Identity Project

This project provides Identity + JWT authentication using **ASP.NET Core** and **Entity Framework Core**.

---

## 📂 Setup Database
1. Open `appsettings.json` and update your **SQL Server connection string**:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=YOUR_SERVER;Database=IdentityDb;User Id=sa;Password=123456;TrustServerCertificate=True;"
   }
   ```

2. Apply migrations and update the database:
   ```bash
   dotnet ef database update -p Identity.Application -s Identity.API
   ```

---

## 🚀 Run the API
1. Start the API:
   ```bash
   dotnet run --project Identity.API
   ```

2. The API will be available at:
   - Swagger UI → `https://localhost:7260/swagger`
   - Example endpoint → `https://localhost:7260/weatherforecast`

---

## 🔑 Identity Endpoints
When running, the following endpoints are automatically available:
- `POST /register`
- `POST /login`
- `POST /logout`
- `POST /refresh`
- `GET /manage/info`

(See them in **Swagger UI**)

---

## 📖 Notes
- Make sure you have the correct **.NET SDK** installed (`dotnet --list-sdks`).
- Requires **SQL Server** running (local or remote).
- To change port, edit `launchSettings.json`.
