# 🧪 Test Cases – Diabetic Retinopathy Detection  
**Module:** DR Detection (Image Upload + Risk Analysis)  
**Prepared By:** Muhammad Anas  
**Date:** November 2024 

---

## ✅ Test Case: Upload Valid Image

| TC ID         | TC-DR-001 |
|---------------|-----------|
| Title         | Upload valid retinal image |
| Test Type     | Functional |
| Priority      | High |
| Preconditions | User is logged in |
| Test Data     | `retina1.jpg` (valid image) |
| Steps         | 1. Go to DR Detection module  2. Click "Upload"  3. Select and submit a valid retinal image |
| Expected Result | Risk result is displayed (e.g., "No DR", "Moderate DR") |
| Actual Result   | — |
| Status          | — |

---

## ✅ Test Case: View Risk Prediction

| TC ID         | TC-DR-002 |
|---------------|-----------|
| Title         | View readable diagnostic result |
| Test Type     | Functional |
| Priority      | High |
| Preconditions | Valid image uploaded |
| Test Data     | None |
| Steps         | 
1. Submit retinal image  
2. Wait for processing  
3. Observe AI's prediction |
| Expected Result | System displays the DR status clearly (e.g., "No Diabetic Retinopathy Detected") |
| Actual Result   | — |
| Status          | — |

---

## ✅ Test Case: Download Diagnosis Report

| TC ID         | TC-DR-003 |
|---------------|-----------|
| Title         | Download DR diagnosis report |
| Test Type     | Functional |
| Priority      | Medium |
| Preconditions | Diagnosis complete |
| Test Data     | None |
| Steps         | 
1. Click “Download Report” button  
2. Save the report locally |
| Expected Result | PDF or formatted report is downloaded |
| Actual Result   | — |
| Status          | — |

---

## ❌ Test Case: Upload Invalid File Format

| TC ID         | TC-DR-004 |
|---------------|-----------|
| Title         | Upload .txt or .pdf file instead of image |
| Test Type     | Negative |
| Priority      | High |
| Preconditions | Module is open |
| Test Data     | `invalid.txt` |
| Steps         | 
1. Try uploading `.txt` file  
2. Click “Submit” |
| Expected Result | Validation error shown: “Unsupported file format” |
| Actual Result   | — |
| Status          | — |

---

## ❌ Test Case: Upload Corrupted Image

| TC ID         | TC-DR-005 |
|---------------|-----------|
| Title         | Upload corrupted image |
| Test Type     | Negative |
| Priority      | Medium |
| Preconditions | Image exists |
| Test Data     | `corrupted.jpg` |
| Steps         | 
1. Upload corrupted image file |
| Expected Result | Error message: “Unable to process image” |
| Actual Result   | — |
| Status          | — |

---

## 🔲 Test Case: Large File Upload (Boundary)

| TC ID         | TC-DR-006 |
|---------------|-----------|
| Title         | Upload large image (near size limit) |
| Test Type     | Boundary |
| Priority      | Medium |
| Preconditions | File is ~5MB+ |
| Test Data     | `retina_large.png` |
| Steps         | 
1. Upload a large-size retinal scan |
| Expected Result | System accepts and processes without timeout |
| Actual Result   | — |
| Status          | — |

---

## 🛡️ Test Case: API Validation for Image Upload

| TC ID         | TC-DR-007 |
|---------------|-----------|
| Title         | Call DR upload API directly with valid token |
| Test Type     | API |
| Priority      | High |
| Preconditions | Token acquired |
| Test Data     | Bearer token + image payload |
| Steps         | 
1. Use Postman  
2. Send POST `/api/dr/image` with correct headers and file |
| Expected Result | JSON response with risk level |
| Actual Result   | — |
| Status          | — |
