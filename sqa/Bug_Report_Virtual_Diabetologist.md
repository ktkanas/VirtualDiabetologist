# 🐞 Bug Report – Virtual Diabetologist System  
**Reported By:** Muhammad Anas (QA Analyst)  
**Environment:** Stage – https://staging.virtualdiabetologist.com  
**Generated:** June 23, 2025  
**Platform:** Web (Chrome, Firefox), Backend (Flask), API Clients  

---

### [BUG-001] Login fails with valid credentials (500 error on API)

- **Created:** 20/Jun/25  
- **Updated:** 23/Jun/25  
- **Due Date:** 25/Jun/25  
- **Status:** To Do  
- **Project:** VD-APP  
- **Components:** Auth, Backend API  
- **Affects Version:** v1.0  
- **Fix Version:** TBD  
- **Type:** Bug  
- **Priority:** High  
- **Reporter:** Muhammad Anas  
- **Assignee:** Backend Dev  
- **Resolution:** Unresolved  
- **Labels:** login, auth, api-failure  
- **Remaining Estimate:** 2 days  
- **Time Spent:** 4h  
- **Original Estimate:** 1 day  

**Description:**  
Login API throws 500 error even with valid user credentials.

**Steps to Reproduce:**  
1. Navigate to `https://staging.virtualdiabetologist.com/login`  
2. Enter correct email and password  
3. Click “Login”  

**Expected Result:**  
User should be redirected to dashboard  

**Actual Result:**  
500 Internal Server Error (POST /api/login)  

**Test Data:**  
Email: user@test.com  
Password: Test123!  



---

### [BUG-002] Retinal image upload accepts unsupported file types

- **Created:** 21/Jun/25  
- **Updated:** 23/Jun/25  
- **Status:** To Do  
- **Components:** DR Detection, File Validation  
- **Priority:** Medium  
- **Type:** Bug  
- **Labels:** file-upload, DR  
- **Fix Version:** Next Patch  
- **Reporter:** QA Team  

**Description:**  
System allows `.txt` and `.pdf` files to be uploaded to DR Detection module, which should accept only `.jpg`, `.jpeg`, and `.png`.

**Steps to Reproduce:**  
1. Go to DR Detection module  
2. Upload a `.txt` file or `.pdf`  
3. Submit form  

**Expected Result:**  
Validation error: “Unsupported file type. Only .jpg, .jpeg, .png allowed”  

**Actual Result:**  
File is accepted, leading to crash in backend image parser  

**Test Data:**  
File: `random.txt`  


---

### [BUG-003] Chatbot crashes when input is only symbols or empty

- **Created:** 23/Jun/25  
- **Due Date:** 25/Jun/25  
- **Components:** Chatbot NLP  
- **Priority:** High  
- **Type:** Bug  
- **Status:** To Do  
- **Reporter:** Muhammad Anas  

**Description:**  
Sending only symbols (e.g., `@#$%^`) or empty input causes the chatbot to crash (LLM unhandled exception).

**Steps to Reproduce:**  
1. Login and go to chat  
2. Send input: `@#@^*&` or leave blank  
3. Observe bot behavior  

**Expected Result:**  
Bot should handle invalid input with a message like “Please enter a valid query.”  

**Actual Result:**  
Frontend freezes, backend throws null response exception  

**Logs:**  

TypeError: Cannot read properties of undefined (reading 'response')

![404](https://github.com/user-attachments/assets/b9dd8dc1-5eba-482b-baef-27ec784bc073)


