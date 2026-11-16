# Exam Prep

Static study site published with GitHub Pages at **https://exams.castafero.com**.

There's no build step. Every page is plain HTML, CSS, and JavaScript.

## Layout

```
index.html        Landing page listing every exam
az-104/index.html AZ-104 study guide, practice exam, and flashcards
az-305/index.html AZ-305 study guide, practice exam, and flashcards
CNAME             Custom domain for GitHub Pages
.nojekyll         Tells GitHub Pages to serve files as-is
```

## Adding a new exam

1. Copy `az-104/` to a new folder, for example `az-305/`.
2. In the new `index.html`, replace the guide content, the `Q` array (practice questions), the `FC` array (flashcards), the `DOM` domain list, and `FULL_PLAN` (how many questions to draw from each domain).
3. Rename the browser storage keys (`KEY`, `WKEY`, `FKEY`) so progress doesn't collide with other exams. For example, change `az104-prep-v1` to `az305-prep-v1`.
4. Add a card for the exam to the root `index.html`.
5. Commit and push. Pages redeploys in about a minute.

## Question format

```js
{id:"g1", d:"gov", q:"<p>Question HTML</p>", o:["A","B","C","D"], a:[1], x:"Explanation HTML"}
// m:true      multi-select ("select all that apply")
// pick:2      multi-select that says "select two"
// series:true Yes/No series question
// cs:true     case-study question (always added to the end of the full exam)
```
