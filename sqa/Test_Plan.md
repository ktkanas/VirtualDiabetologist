# 🧪 Test Plan – Virtual Diabetologist

**Project:** Virtual Diabetologist  
**Prepared By:** Muhammad Anas (QA Analyst)  
**Date:** November 2024   
**Version:** 1.0  

---

## 1. Test Plan Identifier
**VD-TP-01** – Virtual Diabetologist Test Plan v1.0

---

## 2. Introduction
This document outlines the testing strategy for the Virtual Diabetologist system, which assists diabetic patients via AI-powered chatbot recommendations, retinopathy detection, and diabetes risk prediction. This test plan aims to ensure the system meets all defined requirements and is stable, secure, and user-friendly.

---

## 3. Test Items
Modules and components to be tested:
- User Registration and Login
- Health Data Input
- Chatbot Interaction (LLaMA3)
- Diabetic Retinopathy Image Upload and Analysis
- Diabetes Risk Prediction
- Chat Summary PDF Generation
- Admin Management
- API Access (for hospitals/clients)

---

## 4. Features to be Tested

| ID | Feature |
|----|---------|
| F1 | User Registration & Authentication |
| F2 | Health Data Entry and Validation |
| F3 | Personalized AI Chatbot Responses |
| F4 | Upload and Analyze Retinal Images |
| F5 | Diabetes Risk Prediction |
| F6 | Report Generation (PDF) |
| F7 | Admin Data Maintenance |
| F8 | API Key Request and Access |

---

## 5. Features Not to be Tested
- Emergency diagnostics and real-time patient monitoring
- Psychological or emotional health counseling
- Live doctor-patient chat

---

## 6. Approach / Test Strategy

### Test Levels:
- **Unit Testing:** Done by developers (functions, image classification, etc.)
- **Integration Testing:** Frontend ↔ Backend data flow
- **System Testing:** End-to-end testing of workflows
- **User Acceptance Testing (UAT):** Based on project use cases

### Testing Types:
- ✅ Functional Testing
- ❌ Negative Testing
- 🔲 Boundary Value Analysis
- 🎨 UI/UX Testing (Responsiveness, consistency)
- 🔐 Security Testing (JWT, access control)
- ⚙️ API Testing (key handling, request/response)
- 📊 Performance Testing (PDF load, image upload speed)
- 📱 Compatibility Testing (multiple devices & browsers)

---

## 7. Test Criteria

### Entry Criteria:
- All major modules are implemented
- Test data is ready
- Environment is deployed locally or on staging

### Exit Criteria:
- 95%+ test cases executed
- All major/critical bugs resolved
- Test summary report prepared

---

## 8. Deliverables
- ✅ Software Requirements Specification (SRS)
- ✅ Test Plan (this document)
- ✅ Detailed Test Cases (Functional, UI, API, etc.)
- ✅ Bug Reports (Jira-style)
- ✅ [Optional] Test Summary Report (post-execution)

---

## 9. Testing Schedule

| Phase                   | Dates          |
|------------------------|----------------|
| Requirements Review    | 25–26 November 2024 |
| Test Case Design       | 26–27 November 2024 |
| Test Execution         | 27–29 November 2024 |
| Bug Fix & Retesting    | 29–30 November 2024 |

---

## 10. Resources

| Resource      | Role            |
|---------------|-----------------|
| Muhammad Anas | QA Analyst      |
| LLM Model     | Response Engine |
| Postman       | API Testing     |
| Chrome DevTools | UI/Responsive Checks |

---

## 11. Risks

- User health input varies widely → Chatbot responses may be inconsistent.
- Retinopathy detection is image-quality dependent.
- LLM may crash with unexpected input (e.g., empty messages or symbols).

---

## 12. Approvals

| Name               | Role         | Signature |
|--------------------|--------------|-----------|
| Dr. Sumaira Kausar - associate Professor Bahria University Islamabad | Supervisor   | ✅        |

