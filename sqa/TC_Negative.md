# ❌ Negative Test Cases – Virtual Diabetologist  
**Prepared By:** Muhammad Anas  
**Module:** Auth, Chatbot, DR Upload, Input Validation  
**Date:** November 2024  

---

## Module: Registration and Login

| TC ID        | Title                              | Type     | Priority | Preconditions | Test Data                         | Steps                                                               | Expected Result                              | Status |
|--------------|------------------------------------|----------|----------|----------------|------------------------------------|---------------------------------------------------------------------|--------------------------------------------------|--------|
| TC-NEG-001   | Register with empty fields         | Negative | High     | None           | Empty name, email, password        | 1. Go to `/register` <br> 2. Leave fields blank <br> 3. Submit     | Error: Required fields                        | —      |
| TC-NEG-002   | Register with invalid email        | Negative | Medium   | None           | Email: anas[at]mail                | Enter invalid email and submit                                      | Error: Invalid email format                   | —      |
| TC-NEG-003   | Login with incorrect password      | Negative | High     | User registered | Correct email, wrong password      | Enter valid email and wrong password                                | Error: Invalid credentials                    | —      |

---

## Module: Health Input / Chatbot

| TC ID        | Title                              | Type     | Priority | Preconditions | Test Data         | Steps                                                             | Expected Result                           | Status |
|--------------|------------------------------------|----------|----------|----------------|-------------------|-------------------------------------------------------------------|---------------------------------------------|--------|
| TC-NEG-010   | Skip health input before chat      | Negative | High     | Just logged in | None              | Ask chatbot question without entering health data                | Prompt: “Please enter vitals first”         | —      |
| TC-NEG-011   | Input letters in numeric field     | Negative | Medium   | Form open      | Glucose: `abc`     | Enter non-numeric values in numeric field                         | Validation error: “Enter valid number”       | —      |

---

## Module: DR Detection

| TC ID        | Title                                | Type     | Priority | Preconditions | Test Data     | Steps                                                               | Expected Result                             | Status |
|--------------|--------------------------------------|----------|----------|----------------|---------------|---------------------------------------------------------------------|---------------------------------------------|--------|
| TC-NEG-020   | Upload `.txt` file instead of image  | Negative | High     | DR module open | invalid.txt   | Upload `.txt` file and submit                                       | Error: Invalid file type                    | —      |
| TC-NEG-021   | Upload corrupted image file          | Negative | Medium   | DR module open | corrupted.jpg | Upload a corrupted image                                            | Error: Failed to analyze image              | —      |

---

## Module: Report & Chatbot Stability

| TC ID        | Title                            | Type     | Priority | Preconditions | Test Data | Steps                                                          | Expected Result                         | Status |
|--------------|----------------------------------|----------|----------|----------------|-----------|----------------------------------------------------------------|-----------------------------------------|--------|
| TC-NEG-030   | Generate report with no chat     | Negative | Medium   | Logged in      | None      | Click “Generate Report” before starting session                | Error: “No chat data to summarize”       | —      |
| TC-NEG-031   | Send only symbols to chatbot     | Negative | High     | Chat window    | `@#$%^`   | Send input with just symbols                                   | Error or “Please enter a valid query”    | —      |
