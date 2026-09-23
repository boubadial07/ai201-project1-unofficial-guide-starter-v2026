# Acceptance criteria — The Unofficial Guide

Five criteria that say what "working" means for this system, written in unit 1
**before** any results existed.

An acceptance criterion names a target: a number, a count, a rate, or something
a person could plainly observe. *"Retrieval works"* is an opinion. *"For at
least 4 of my 5 test questions, the top results include a chunk containing the
answer"* is a criterion.

Under each one, write a sentence or two on **why that target** and not a
stricter or looser one. A reason that says something about your corpus or your
pipeline earns credit; *"80% seemed reasonable"* does not.

> Missing your own targets next unit costs you nothing. Setting a target so
> easy you can't miss it does.

---

## 1. Retrieved chunks contain the answer

For at least 4 of my 5 test questions, the retrieved chunks include one that
contains the answer.

**Why this target:**
"The `campus_life` corpus contains 88 short documents, and the information in each document is usually focused on one specific student-life topic. Because my five questions target specific topics such as housing, parking, dining dollars, and graduation requirements, I expect the relevant information to be retrieved for at least 4 of the 5 questions."

---

## 2. Every answer names a source

Every answer the system produces names at least one source document.

**Why this target:**
My corpus consists of short, focused documents, so each answer should be traceable to at least one document rather than requiring information from outside the corpus. Requiring a source for every produced answer also makes it possible to check whether the response is grounded in the retrieved material.

---

## 3. The relevance gate stops out-of-corpus questions

When I ask a question my documents clearly don't cover, the relevance gate
stops it and the system returns "I don't have enough information about that" —
in at least 4 of 5 tries.

**Why this target:**
<!-- The `campus_life` corpus is limited to university and student-life topics, while the five out-of-scope questions cover unrelated subjects such as world history, vehicle maintenance, medication, and programming. Because those topics are clearly outside the corpus, I expect the relevance gate to reject at least 4 of the 5 questions. -->

---

## 4. Something about your chunks

YOU WRITE THIS ONE.

     How would you know if your chunks were the right size? Name something
     countable or observable.

     At least 4 of 5 sampled chunks should contain a complete thought about one student-life topic without cutting a sentence in half at either end.



**Why this target:**
The `campus_life` documents are short, averaging about 317 characters, and most contain information focused on a single topic. A chunk that preserves a complete thought should make the retrieved information easier to use for answering specific student-life questions.


---

## 5. Your choice

YOU WRITE THIS ONE TOO.

     For all 5 in-scope test questions, the named source document should contain the information needed to support the answer.



**Why this target:**
Having a source listed is not enough if the source does not actually support the answer. Since my `campus_life` corpus contains short documents focused on specific topics, I want each answer's cited source to be directly relevant to the question rather than simply being one of the retrieved documents.


---

<!-- ─────────────────────────────────────────────────────────────────────────
     UNIT 2 — read this before you change anything above.

     If a criterion turns out to be BROKEN rather than merely unmet, you can
     revise it, and that earns credit. But never delete or edit the original
     line. Add the revision underneath it, like this:

         ## 1. Retrieved chunks contain the answer

         For at least 4 of my 5 test questions, the retrieved chunks include
         one that contains the answer.

         **Why this target:** ...

         > **Revised in unit 2:** For at least 4 of 5 questions, the top three
         > results contain the answer.
         >
         > **Why revised:** I couldn't judge "the chunks include one that
         > contains the answer" the same way twice — I scored two questions
         > differently on Monday than on Wednesday. The new version is
         > something I can actually check.

     That's a revision because the criterion couldn't be MEASURED.

     Lowering a target because you missed it is not a revision, and it costs
     you the point:

         ✗ "I said 4 of 5 but got 2 of 5, so 2 of 5 is more realistic."

     A number you missed stays where it is, gets diagnosed, and gets a fix
     attempted. That's where the points are.

     The whole reason the originals stay visible is so someone can see what you
     said before you knew the answer.
     ───────────────────────────────────────────────────────────────────────── -->
