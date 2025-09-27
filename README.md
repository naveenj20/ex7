# Exercise: Extract Text from PDF and Write to Text File

## Objective
To automate reading text from a PDF file and saving the extracted content into a text file using UiPath.

---

## Step-by-Step Instructions

### 1. Create New Project
- Open **UiPath Studio** → New Project → Process  
- Name it `PdfToTextExample`.

### 2. Install Dependencies
- Go to **Manage Packages**.  
- Install:
  - `UiPath.PDF.Activities` (for reading PDF files).  
  - `UiPath.System.Activities` (already included by default).  

### 3. Define Variables
| Name      | Data Type | Scope | Purpose                        |
|-----------|-----------|-------|--------------------------------|
| Text   | String    | Main  | Stores extracted text from PDF |

### 4. Read PDF File
1. Drag **Read PDF Text** activity into the workflow.  
2. Set **FileName** = path to your input PDF (e.g., `"C:\Users\admin\Desktop\resume.pdf"`).  
3. Output → assign to variable `Text`.

---

### 5. Write to Text File
1. Drag **Write Text File** activity below **Read PDF Text**.  
2. Set:
   - **FileName** = `"C:\Users\admin\Desktop\sample.txt"`  
   - **Text** = `Text`  

---

## Workflow
1. **Read PDF Text** → extracts text from the given PDF file.  
2. **Write Text File** → writes extracted text into `sample.txt`.  

---

## Output
- Input: `resume.pdf` (or any PDF with text content).
<img width="653" height="827" alt="image" src="https://github.com/user-attachments/assets/f2d86f69-b25d-4e8e-addb-edcc26d1de4f" />

- Output: `sample.txt` containing the extracted PDF text.  
<img width="1919" height="1142" alt="Screenshot 2025-09-27 102421" src="https://github.com/user-attachments/assets/68871f28-3f48-4f6d-bca1-00a723cbb252" />

---

## Result
Thus, the workflow successfully extracts text from a PDF and writes it into a text file for further processing.
