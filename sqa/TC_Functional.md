# ✅ Functional Test Cases – Virtual Diabetologist  
**Prepared By:** Muhammad Anas  
**Module:** Auth, Chatbot, DR Detection, Report Generation  
**Date:** November 2024  

---

## Module: User Registration and Login

| TC ID        | Title                         | Type       | Priority | Preconditions      | Test Data            | Steps                                                                 | Expected Result                                  | Status |
|--------------|-------------------------------|------------|----------|---------------------|----------------------|-----------------------------------------------------------------------|--------------------------------------------------|--------|
| TC-FUNC-001  | Register new user             | Functional | High     | None                | Valid name, email, password | 1. Visit `/register` <br> 2. Fill details <br> 3. Submit         | Account created and redirect to login            | ✅ Pass |
| TC-FUNC-002  | Login with valid credentials  | Functional | High     | User registered     | Valid email, password        | 1. Go to `/login` <br> 2. Enter credentials <br> 3. Submit        | User logged in and taken to dashboard            | ✅ Pass |
| TC-FUNC-003  | Logout                        | Functional | Medium   | User is logged in   | N/A                        | Click logout button                                                  | User redirected to login, session destroyed       | ✅ Pass |

---

## Module: Health Input + Chatbot

| TC ID        | Title                                   | Type       | Priority | Preconditions   | Test Data                    | Steps                                                                 | Expected Result                              | Status |
|--------------|-----------------------------------------|------------|----------|------------------|------------------------------|-----------------------------------------------------------------------|--------------------------------------------------|--------|
| TC-FUNC-010  | Submit health input                     | Functional | High     | User is logged in | Age, blood sugar, HbA1C     | 1. Open chatbot <br> 2. Input health values                          | Confirmation: Data saved for analysis           | ✅ Pass |
| TC-FUNC-011  | Receive personalized recommendation     | Functional | High     | Health data added | N/A                          | Ask chatbot for advice                                               | Personalized advice based on vitals             | ✅ Pass |
| TC-FUNC-012  | Generate and download summary PDF       | Functional | Medium   | Completed chat   | N/A                          | Click “Generate Report”                                              | PDF downloaded with chat & insights             | ✅ Pass |

---

## Module: DR Detection

| TC ID        | Title                                | Type       | Priority | Preconditions   | Test Data           | Steps                                                                 | Expected Result                             | Status |
|--------------|--------------------------------------|------------|----------|------------------|---------------------|-----------------------------------------------------------------------|---------------------------------------------|--------|
| TC-FUNC-020  | Upload valid retinal image           | Functional | High     | User is logged in | retina1.jpg         | 1. Open DR module <br> 2. Upload image <br> 3. Submit                | DR risk result displayed                     | ✅ Pass |
| TC-FUNC-021  | View DR result on-screen             | Functional | High     | Image uploaded    | N/A                 | View result after processing                                          | “No DR” / “Mild DR” or other classification   | ✅ Pass |
| TC-FUNC-022  | Download DR diagnosis report         | Functional | Medium   | DR result ready   | N/A                 | Click “Download Report”                                               | PDF downloaded                               | ✅ Pass |
