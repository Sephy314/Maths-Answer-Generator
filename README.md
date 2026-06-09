# Maths Answer Generator

Maths Answer Generator is a two-stage AI pipeline for processing Korean mathematics exam papers.

The system automatically:

1. Extracts problems from exam images using OCR
2. Converts them into structured Markdown with LaTeX
3. Solves the extracted problems
4. Generates a print-ready answer sheet
5. Produces a PDF suitable for printing

---

## Architecture

```text
Exam Image
    │
    ▼
OCR.md
    │
    ▼
Structured Markdown
    │
    ▼
AnswerGenerator.md
    │
    ▼
Final Answers
    │
    ▼
A4 HTML
    │
    ▼
PDF
```

---

## Components

### OCR.md

Specialized OCR prompt for Korean mathematics exam papers.

Features:

* Korean text preservation
* LaTeX conversion
* Structured Markdown output
* Question numbering reconstruction
* Diagram recognition
* Exam paper formatting preservation

Output example:

```markdown
# 문제지

## 1번

다음 식을 계산하시오.

$$
x^2 + 3x + 2
$$
```

---

### AnswerGenerator.md

Answer-sheet generation prompt.

Features:

* Solves extracted problems
* Produces final answers only
* Generates print-ready A4 layout
* Creates two identical answer sheets
* Adds dashed cut line
* Exports PDF

Output:

```text
PDF
└── Answer Sheet
    ├── Question 1
    ├── Question 2
    └── ...
```

---

## Workflow

### Step 1

Provide an exam image.

### Step 2

Run OCR.md to convert the image into structured Markdown.

### Step 3

Pass the Markdown output to AnswerGenerator.md.

### Step 4

Generate the final PDF answer sheet.

---

## Goals

* High-quality Korean maths OCR
* Consistent LaTeX conversion
* Automatic answer generation
* Printable school-style answer sheets
* Minimal manual editing

---

## Future Improvements

* Multi-page exam support
* Handwritten answer recognition
* Geometry figure extraction
* Automatic grading
* Batch processing
* Web API
* Local model support

---

## Author

Davie (Sephy)

Student Developer interested in:

* Distributed Systems
* Networking
* Go
* PostgreSQL
* Educational Technology
* AI-assisted Learning Tools
