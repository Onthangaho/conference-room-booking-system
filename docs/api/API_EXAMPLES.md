# Conference Room Booking API — Usage Examples

## 1. Introduction
This document provides practical examples of how to interact with the Conference Room Booking API.  
All requests assume the API is running locally at `http://localhost:5000`.  
Authentication is required for most endpoints using a **Bearer token**.

---

## 2. Authentication
The API uses **Bearer Token authentication**.  
All protected endpoints require the client to include an access token in the `Authorization` header.

**Authentication Details:**
- Type: Bearer Token
- Header format: `Authorization: Bearer <token>`
- Token is assumed to be issued by a login/auth service (not implemented in this assignment).

**Example Request:**
```bash
curl -X POST http://localhost:5000/auth/login \
  -H "Content-Type: application/json" \
  -d '{"username":"admin","password":"secret"}'

**Example Response
 ```json
 {
    "token": "eygjgfkhkfhlgnfmnsdsfioRE..."
 }
 ```
 ## 3. Conference Rooms
 ### Retrieve All Rooms

 ```bash
 curl -X GET http://localhost:5000/rooms \
  -H "Authorization: Bearer <token>"

**example Response(200 OK)**
```json
[
  { "id": "1", "name": "Boardroom A", "capacity": 10 },
  { "id": "2", "name": "Meeting Room B", "capacity": 6 }
]
```

### Retrive Room by ID
```bash
curl -X GET http://localhost:5000/rooms/1 \
  -H "Authorization: Bearer <token>"
```

## 4. Bookings

### Create Booking
```bash
curl -X POST http://localhost:5000/bookings \
  -H "Authorization: Bearer <token>" \
  -H "Content-Type: application/json" \
  -d '{"roomId":1,"date":"2026-02-01","startTime":"09:00:00","endTime":"10:00:00"}'
```

## 5. Availability
### Check room availability
```bash
curl -X GET "http://localhost:5000/availability?roomId=1&date=2026-02-01" \
  -H "Authorization: Bearer <token>"

**Example response(200 OK)
```json
{
  "roomId": 1,
  "date": "2026-02-01",
  "available": true
}
```

## 6. Error Handling examples
The API uses standard HTTP status codes to indicate errors.
### Room NOT Found(404 NOt found)
```json
{ "message": "Room not found" }
```

### Booking Conflict(409)
```json
{ "message": "Room not available for the selected time" }
```





