# 🔐 API Test Cases – Virtual Diabetologist  
**Prepared By:** Muhammad Anas  
**Module:** API Authentication, DR Upload  
**Date:** November 2024  

---

## ✅ Test Case: Access profile with valid token

| TC ID         | TC-API-001 |
|---------------|-------------|
| Title         | Valid token allows user profile access |
| Test Type     | API |
| Priority      | High |
| Preconditions | User is authenticated |
| Test Data     | Valid JWT token |
| Steps         | 
1. Send GET request to `/api/user/profile`  
2. Include valid bearer token in headers |
| Expected Result | Response 200 OK with user data |
| Actual Result   | — |
| Status          | — |

---

## ❌ Test Case: Access profile with expired token

| TC ID         | TC-API-002 |
|---------------|-------------|
| Title         | Expired JWT returns 401 |
| Test Type     | API, Security |
| Priority      | High |
| Preconditions | Token is expired |
| Test Data     | Expired token |
| Steps         | 
1. Send GET `/api/user/profile`  
2. Use expired token in headers |
| Expected Result | Response 401 Unauthorized |
| Actual Result   | — |
| Status          | — |

---

## ❌ Test Case: Missing token

| TC ID         | TC-API-003 |
|---------------|-------------|
| Title         | No token in API request |
| Test Type     | API, Security |
| Priority      | High |
| Preconditions | None |
| Test Data     | No token provided |
| Steps         | 
1. Send GET `/api/user/profile` without headers |
| Expected Result | 403 Forbidden or 401 Unauthorized |
| Actual Result   | — |
| Status          | — |

---

## ✅ Test Case: DR Upload API with valid image

| TC ID         | TC-API-010 |
|---------------|-------------|
| Title         | Upload valid image via API |
| Test Type     | API |
| Priority      | High |
| Preconditions | Token generated |
| Test Data     | JPEG image file |
| Steps         | 
1. Use Postman to POST `/api/dr/image`  
2. Add image as multipart/form-data  
3. Include authorization header |
| Expected Result | 200 OK with DR risk JSON |
| Actual Result   | — |
| Status          | — |

---

## ❌ Test Case: Upload invalid file type via API

| TC ID         | TC-API-011 |
|---------------|-------------|
| Title         | Upload `.pdf` file to image API |
| Test Type     | API, Negative |
| Priority      | High |
| Preconditions | API is running |
| Test Data     | File: `sample.pdf` |
| Steps         | 
1. Call `/api/dr/image`  
2. Attach `.pdf` instead of image |
| Expected Result | 400 Bad Request with file validation error |
| Actual Result   | — |
| Status          | — |

---

## ❌ Test Case: Upload without image field

| TC ID         | TC-API-012 |
|---------------|-------------|
| Title         | Send POST request without image in body |
| Test Type     | API, Negative |
| Priority      | Medium |
| Preconditions | Auth header present |
| Test Data     | None |
| Steps         | 
1. Call `/api/dr/image`  
2. Send request without `file` field |
| Expected Result | 422 Unprocessable Entity |
| Actual Result   | — |
| Status          | — |
