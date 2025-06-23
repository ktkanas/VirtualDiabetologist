# 📄 Software Requirements Specification (SRS)
**Project Title:** Virtual Diabetologist  
**Prepared By:** Muhammad Anas  
**Date:** June 2024

---

## 1. Introduction

The *Virtual Diabetologist* is a chatbot-based platform that helps diabetic patients by offering personalized recommendations, risk assessments, and diagnostic support. The system uses AI (LLaMA3) and integrates diabetes prediction, diabetic retinopathy detection, and lifestyle guidance.

---

## 2. Overall Description

- **Target Users:** Diabetic individuals, healthcare API clients, admin
- **Platform:** Web-based (React frontend, Flask backend)
- **Technologies:** LLaMA3, CNN for DR detection, MongoDB, ChromaDB
- **Key Modules:**
  - User Management (Registration/Login)
  - Chatbot (AI + Health Recommendation Engine)
  - Diabetes Risk Predictor
  - Retinopathy Detection (Image Upload + CNN)
  - Chat History Summary Generator (PDF)
  - API for External Access

---

## 3. Functional Requirements

| ID     | Description |
|--------|-------------|
| FR1    | User shall register and login with email and password. |
| FR2    | User shall input health data (e.g., age, glucose, BMI). |
| FR3    | Chatbot shall provide personalized advice based on inputs. |
| FR4    | User shall upload retinal images for DR detection. |
| FR5    | System shall classify DR status and show results. |
| FR6    | System shall allow PDF export of chatbot conversation. |
| FR7    | Admin shall manage compliance and platform health. |
| FR8    | API clients shall access system functions via keys. |
| FR9    | Context shall be retained across chatbot sessions. |
| FR10   | User shall update or delete their profile data. |

---

## 4. Non-Functional Requirements

| ID     | Category      | Requirement |
|--------|---------------|-------------|
| NFR1   | Usability     | UI must be intuitive and mobile-responsive. |
| NFR2   | Performance   | System should respond within 3 seconds. |
| NFR3   | Security      | Use HTTPS, JWT auth, secure image handling. |
| NFR4   | Availability  | Uptime must be ≥ 95.9% (excluding maintenance). |
| NFR5   | Scalability   | Backend should scale with increased traffic. |
| NFR6   | Compliance    | GDPR compliance for data retention and removal. |
| NFR7   | Compatibility | Works on all major browsers. |
| NFR8   | Maintainability| Easy to debug and deploy with versioned code. |

---

## 5. Assumptions

- Users have stable internet and devices.
- Retinal images are captured via approved medical equipment.
- APIs are integrated with authorized systems.

---

## 6. Limitations

- No real-time emergency diagnostics.
- Does not prescribe medication.
- No mental health or psychological support.

---
