# Proposed API contract (adjust with backend)

Base URL: `http://localhost:8080/api`
- `GET /products` -> `[{id,name,category,currentStock,unitPrice,safetyStock,supplierId}]`
- `POST /products` -> product JSON; response saved product
- `PUT /products/{id}` -> updated product
- `DELETE /products/{id}` -> success/204
- `GET /sales` -> `[{id,productId,quantitySold,saleDate}]`
- `POST /sales` -> `{productId,quantitySold,saleDate}` (backend should update sale and stock in one transaction)
- `GET /suppliers` -> `[{id,name,contact,leadTimeDays}]`
- `POST /suppliers` -> `{name,contact,leadTimeDays}`
- `POST /forecasts/{productId}` -> `{forecastDays:7}`; response includes `predictedDailyDemand`, `totalPredictedDemand`, `averageDailyDemand`, `modelName`
- `GET /recommendations` -> recommendation array
- `GET /dashboard/summary` -> `{totalProducts,inventoryValue,lowStockCount,salesToday}`

Use camelCase JSON. Product IDs must be consistent. Enable CORS for `http://localhost:5173`. Never put DB credentials or API keys in frontend code.
