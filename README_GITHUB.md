# FE Civil Prep — Native-Question Pilot

This is a new, lightweight website inspired by the prior FE Civil Prep layout. The questions are **native HTML text and SVG drawings**, not screenshots. It is a **65-question pilot** sourced from the user-uploaded Learnova (2025) book, not a reconstruction of the entire 1,052-question index or the Islam book.

## Publish on GitHub Pages (no Terminal)

1. Extract `FE_Civil_Prep_Native_Question_Pilot_GitHub.zip`.
2. Open your new GitHub repository, choose **Add file -> Upload files**, then drag in the **extracted files**, not the ZIP. Keep `index.html` in the root.
3. Commit the files. Go to **Settings -> Pages -> Deploy from a branch -> main -> /(root)**.
4. Open the URL shown by GitHub when published.

Five files run the app: `index.html`, `styles.css`, `app.js`, `questions.js`, and `jszip.min.js`. This is far below the GitHub upload limits. The optional `SOURCE_INDEX.csv` and this README are reference documentation.

## Individual question ZIP exports

Open any problem, and click **Download this question ZIP**. Each ZIP contains one standalone HTML problem, its four choices, a worked answer, and its JSON data. This export uses local JSZip and does not need a server or upload. There is also an optional master ZIP with 65 separately packaged question ZIPs. **Do not upload 65 individual question ZIPs to make the site work**: the site reads its native database from `questions.js`.

## Quality and limitations

- 65 problems manually reconstructed and engineering/calculation checked to a best-effort level. This is not independent professional validation.
- Source problem numbers and source-PDF pages are preserved. Some original wording is reformatted/shortened for readability.
- Diagrams for Problems 1 and 189 are newly drawn SVGs; problems that need more careful visual reconstruction are excluded from this pilot.
- **Known source inconsistency:** Problem 18 shows a source key of B in the automated index, but the equation of the circle tangent is **3x + 4y = 25 (A)**. The website uses the mathematically correct answer and discloses the mismatch.
- The original uploaded book contains other poorly extracted or incomplete formulas. They have not been silently added.
- The 2025 publisher material is copyrighted. Confirm authorization for public web redistribution of its question text, not only image display.
- Browser progress is local to the device/browser; no centralized accounts or reports.

## Files

- `questions.js`: all 65 native question records
- `app.js`: browser UI, local progress, timed sessions, per-question exports
- `styles.css`: site design
- `SOURCE_INDEX.csv`: source mapping and audit remarks
