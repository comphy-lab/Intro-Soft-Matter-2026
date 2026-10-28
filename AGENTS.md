# Introduction to Soft Matter 2026

Public coding-assessment repository for the 2026 run of the Durham course *Soft Condensed Matter: An Introduction*. Students fork it, add their work under `submissions/`, and open a pull request. `README.md` is the authoritative assignment text; this file is the operating manual for AI assistants working in the repository.

## Structure

```
.
├── README.md                 # assignment: options, questions, dates, submission rules
├── submissions/              # student files only: submissions/<github-user>_<filename>
├── .github/
│   ├── workflows/validate-submission.yml   # path and filename check; never runs student code
│   ├── pull_request_template.md
│   └── CODEOWNERS
└── LICENSE                   # GPL-3.0
```

## Rules for changes

- Student pull requests add files directly in `submissions/`, each prefixed with the author's exact GitHub username and `_`. They do not delete or edit other files, create nested folders or add symbolic links.
- Every submission includes `<github-user>_README.md` and `<github-user>_AI-log.md`. The validation workflow enforces this.
- The validation workflow must never execute submitted code. It reads file names and modes only.
- Do not commit credentials, student numbers, marks or private contact details.

## Helping a student

AI assistance is encouraged in this course, but the student must be able to explain and defend every line and figure. Prefer explaining reasoning, checks and numerical method choices to producing code the student cannot follow, and record the exchange in the student's AI log.
