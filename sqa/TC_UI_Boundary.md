# 🎨 UI & Boundary Test Cases – Virtual Diabetologist  
**Prepared By:** Muhammad Anas  
**Module:** Forms, Frontend Layout, Field Validation  
**Date:** November 2024  

---

## 🎯 Boundary Value Test Cases

### ✅ Test Case: Minimum valid age

| TC ID         | TC-BND-001 |
|---------------|------------|
| Title         | Enter minimum acceptable age (1) |
| Test Type     | Boundary |
| Priority      | Medium |
| Preconditions | Health form visible |
| Test Data     | Age: 1 |
| Steps         | 
1. Go to user profile or health input form  
2. Input age: 1  
3. Submit |
| Expected Result | Data accepted without error |
| Actual Result   | Data submitted successfully |
| Status          | ✅ Pass |

---

### ✅ Test Case: Maximum valid age

| TC ID         | TC-BND-002 |
|---------------|------------|
| Title         | Enter maximum acceptable age (120) |
| Test Type     | Boundary |
| Priority      | Medium |
| Preconditions | Health form visible |
| Test Data     | Age: 120 |
| Steps         | 
1. Input age: 120  
2. Submit |
| Expected Result | Data accepted without error |
| Actual Result   | Data submitted successfully |
| Status          | ✅ Pass |

---

### ❌ Test Case: Age above maximum limit

| TC ID         | TC-BND-003 |
|---------------|------------|
| Title         | Enter unrealistic age (e.g., 200) |
| Test Type     | Boundary, Negative |
| Priority      | High |
| Preconditions | Form open |
| Test Data     | Age: 200 |
| Steps         | 
1. Enter age: 200  
2. Submit form |
| Expected Result | Error message: “Invalid age” |
| Actual Result   | “Invalid age” message displayed |
| Status          | ✅ Pass |

---

### ❌ Test Case: BMI below threshold

| TC ID         | TC-BND-004 |
|---------------|------------|
| Title         | Enter BMI below 10 |
| Test Type     | Boundary, Negative |
| Priority      | Medium |
| Preconditions | Health form ready |
| Test Data     | BMI: 9 |
| Steps         | 
1. Enter BMI: 9  
2. Submit form |
| Expected Result | Validation error shown |
| Actual Result   | Validation message: “BMI value too low” |
| Status          | ✅ Pass |

---

## 💻 UI/UX & Responsiveness Test Cases

### ✅ Test Case: UI layout on mobile screen

| TC ID         | TC-UI-010 |
|---------------|------------|
| Title         | Check layout responsiveness on mobile device |
| Test Type     | UI |
| Priority      | Medium |
| Preconditions | Application deployed |
| Test Data     | None |
| Steps         | 
1. Open browser dev tools  
2. Toggle mobile view (e.g., iPhone X)  
3. Navigate through pages |
| Expected Result | Layout adjusts properly (no horizontal scroll) |
| Actual Result   | Layout responsive, no scroll needed |
| Status          | ✅ Pass |

---

### ✅ Test Case: Button visibility and alignment

| TC ID         | TC-UI-011 |
|---------------|------------|
| Title         | Ensure CTA buttons are clearly visible and aligned |
| Test Type     | UI |
| Priority      | Low |
| Preconditions | Home page loaded |
| Test Data     | None |
| Steps         | 
1. Load landing page  
2. Observe all primary CTA buttons |
| Expected Result | Buttons are visible, accessible, and centered |
| Actual Result   | All CTA buttons are visible and properly aligned |
| Status          | ✅ Pass |

---

### ❌ Test Case: Text overflow on small screen

| TC ID         | TC-UI-012 |
|---------------|------------|
| Title         | Check for text clipping on small screens |
| Test Type     | UI, Boundary |
| Priority      | Medium |
| Preconditions | Mobile screen view |
| Test Data     | None |
| Steps         | 
1. Resize browser to < 350px width  
2. Navigate to chatbot and reports pages |
| Expected Result | Text should wrap or scale correctly |
| Actual Result   | Some text clipped or overlapped in chatbot area |
| Status          | ❌ Fail |

---

### GUI Test Screenshot

![GUI Test](https://github.com/user-attachments/assets/aa039865-e0a2-4190-bcfa-5d2ae589f72a)
