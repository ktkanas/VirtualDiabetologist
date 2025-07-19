# ❌ Negative Test Cases – Virtual Diabetologist  
**Prepared By:** Muhammad Anas  
**Module:** Auth, Chatbot, DR Upload, Input Validation  
**Date:** November 2024  

---

## Module: Registration and Login

| TC ID      | Title                          | Type     | Priority | Preconditions | Test Data                      | Steps                                                                 | Expected Result                        | Status     |
|------------|--------------------------------|----------|----------|----------------|--------------------------------|-----------------------------------------------------------------------|----------------------------------------|-------------|
| TC-NEG-001 | Register with empty fields     | Negative | High     | None           | Empty name, email, password    | 1. Go to `/register` <br> 2. Leave all fields blank <br> 3. Submit   | Error message: Required fields         | ❌ Failed   |
| TC-NEG-002 | Register with invalid email    | Negative | Medium   | None           | Email: anas[at]mail            | 1. Enter invalid email <br> 2. Submit                                 | Error message: Invalid email format     | ✅ Passed   |
| TC-NEG-003 | Login with incorrect password  | Negative | High     | User registered | Correct email, wrong password | 1. Enter registered email <br> 2. Enter wrong password <br> 3. Submit | Error message: Invalid credentials      | ✅ Passed   |

---

## Module: Health Input / Chatbot

| TC ID      | Title                          | Type     | Priority | Preconditions | Test Data     | Steps                                                                 | Expected Result                               | Status     |
|------------|--------------------------------|----------|----------|----------------|----------------|-----------------------------------------------------------------------|------------------------------------------------|-------------|
| TC-NEG-010 | Skip health input before chat  | Negative | High     | Just logged in | None           | 1. Ask chatbot question without entering any vitals                   | Prompt: "Please enter vitals first"           | ✅ Passed   |
| TC-NEG-011 | Input letters in numeric field | Negative | Medium   | Form open      | Glucose: `abc` | 1. Type letters in numeric field <br> 2. Submit                       | Error message: Enter valid number             | ✅ Passed   |

---

## Module: DR Detection

| TC ID      | Title                            | Type     | Priority | Preconditions | Test Data       | Steps                                                             | Expected Result                            | Status     |
|------------|----------------------------------|----------|----------|----------------|------------------|-------------------------------------------------------------------|---------------------------------------------|-------------|
| TC-NEG-020 | Upload `.txt` file instead image | Negative | High     | DR module open | `invalid.txt`    | 1. Upload `.txt` file <br> 2. Submit                              | Error message: Invalid file type            | ✅ Passed   |
| TC-NEG-021 | Upload corrupted image file      | Negative | Medium   | DR module open | `corrupted.jpg`  | 1. Upload corrupted image <br> 2. Submit                          | Error message: Failed to analyze image      | ❌ Failed   |

---

## Module: Report & Chatbot Stability

| TC ID      | Title                          | Type     | Priority | Preconditions | Test Data | Steps                                                   | Expected Result                               | Status     |
|------------|--------------------------------|----------|----------|----------------|-----------|----------------------------------------------------------|------------------------------------------------|-------------|
| TC-NEG-030 | Generate report with no chat   | Negative | Medium   | Logged in      | None      | 1. Click “Generate Report” without starting a session    | Error message: No chat data to summarize      | ✅ Passed   |
| TC-NEG-031 | Send only symbols to chatbot   | Negative | High     | Chat window    | `@#$%^`   | 1. Send input with just symbols                          | Error or prompt: Please enter a valid query   | ✅ Passed   |
