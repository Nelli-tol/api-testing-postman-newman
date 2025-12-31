# Endpoint Coverage (ReqRes)

This document shows what endpoints are covered by the Postman collection and what is validated.

Environment variable:
- `base_url = https://reqres.in`

---

## Covered Endpoints

### 1) GET /api/users?page=2
**Goal:** Validate list response structure and status.

**Checks:**
- Status code = 200
- Response contains `data` array
- `data.length > 0`
- Each item has `id`, `email`, `first_name`, `last_name` (basic schema sanity)
- `page` equals requested page (when present)

---

### 2) POST /api/login (positive)
**Goal:** Validate successful authentication response.

**Request body:**
- email + password

**Checks:**
- Status code = 200
- Response has `token`
- `token` is non-empty string

---

### 3) POST /api/login (negative: missing password)
**Goal:** Validate error handling.

**Request body:**
- email only (password missing)

**Checks:**
- Status code = 400
- Response has `error`
- `error` message is not empty

---

## Notes / Future Improvements (optional)
- Add schema validation (more strict)
- Add negative tests for invalid email format
- Add more endpoints (create user, update user, delete user)