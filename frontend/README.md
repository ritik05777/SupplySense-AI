# SupplySense AI Frontend

React/Vite college-project prototype. Starts in demo mode with sample data and keeps API calls in `src/api.js` for future Spring Boot integration.

## Prerequisites
- Node.js LTS (includes npm)
- VS Code or another editor
- Internet for initial package install
No Java, PostgreSQL or Python is needed to show the frontend demo.

## Run
1. Extract the ZIP and open the folder in VS Code.
2. Open Terminal in the project folder.
3. Run `npm install`
4. Run `npm run dev`
5. Open the localhost URL printed by Vite (usually http://localhost:5173).

## Demo
The app starts with sample data. Product creation/editing/deletion and recording sales work in the browser session. Demo changes are not saved to a database.

## Connect Spring Boot later
Copy `.env.example` to `.env`, set `VITE_USE_MOCK_DATA=false`, and confirm `VITE_API_BASE_URL=http://localhost:8080/api`. Implement the proposed endpoints in `src/api.js` or adjust paths/fields to match your backend. Configure CORS in Spring Boot for `http://localhost:5173`.

Forecasts and replenishment suggestions are illustrative in demo mode, not verified ML predictions. Run `npm run build` to verify production compilation.
