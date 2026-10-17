# Acceptance criteria — TakeMeter

Five criteria that say what "working" means for this classifier, written in
unit 5 **before** anything was trained.

**All five are yours this time.** None are given. You've had two projects of
practice.

An acceptance criterion names a number. *"The model is accurate"* is an
opinion. *"Every label has an F1 of at least 0.60 on the held-out set"* is a
criterion.

Under each, write a sentence or two on **why that number**. A reason that says
something about your data or your taxonomy earns credit — *"I picked 0.60 F1
for `reaction` because it's my smallest label and I only have about 50
examples of it"*. A reason that could be attached to any project does not.

> Missing your own targets next unit costs you nothing. Setting a target so
> easy you can't miss it does.

---

## Pick numbers you can defend

Not numbers that sound impressive. Three labels means a coin-flip guesser gets
about 33%, so a target of 0.40 is barely a target. Your number should sit
somewhere you'd honestly call useful.

**Cover at least three of these five areas.** They're here as prompts, not as a
form to fill in — a criterion that fits none of them is fine if it names a
number.

| Area | A question it could answer |
|---|---|
| Overall accuracy | How often does it need to be right to be worth using? |
| Per-label performance | Is one label allowed to be much worse than the others? |
| Balance | How lopsided can your label counts get before it's a problem? |
| Consistency | If someone else labelled the same posts, how often should you agree? |
| Confidence | Should a confident prediction be right more often than an unsure one? |

Two things worth knowing before you pick numbers, because both will affect
whether you hit them:

- **Your smallest label will have the jumpiest score.** If a label has 50
  examples, about 8 land in the test split. An F1 computed on 8 examples moves
  a lot between seeds. A target for that label should be looser than one for
  your biggest label, and saying so is a good reason.
- **Unit 6 tests across three seeds, and the target has to hold across all
  three.** A target of 0.65 against results of 0.71, 0.62, 0.68 is a **miss**.
  Pick with that in mind — it is stricter than it first sounds.

---

## 1. Overall accuracy

The classifier achieves **at least 65% accuracy** on the held-out test set on
each of the three random seeds.

**Why this target:** With only 200 Reddit posts, the training set is small, and
`specific_question` and `general_question` can share a lot of wording. 65% is
well above the ~33% a random guesser gets on three labels, so it still
requires the classifier to actually separate the categories.

---

## 2. Per-label performance

On each of the three seeds, `specific_question` and `experience_sharing` each
have an **F1 of at least 0.60**, and `general_question` has an **F1 of at least
0.45**.

**Why this target:** `general_question` is likely my smallest label, because
most runners on r/Marathon_Training ask about a specific training problem.
With few examples in the test split, its F1 will swing between seeds, so its
target is looser than the other two.

---

## 3. Label balance

Each label has **at least 30 of the 200 collected posts** (15%).

**Why this target:** The subreddit has both advice-seeking posts and personal
race and training stories, but they don't show up equally often. At least 30
examples per label keeps any one category from being too small to train on or
evaluate.

---

## 4. Labelling consistency

My labels agree with the staff labels on **at least 70% of the 30 staff
posts** (21 of 30), measured with `agreement.py`.

**Why this target:** The line between `specific_question` and
`general_question` depends on how carefully I apply my written decision rule.
The staff set tests the same skill, applying a written rule exactly as written,
on rules I didn't write myself, so it shows whether I label by the rule or by
feel.

---

## 5. Prediction confidence

On each of the three seeds, accuracy on the **most-confident third** of test
predictions is **at least 15 percentage points higher** than accuracy on the
least-confident third.

**Why this target:** Posts with a detailed training problem or a clear race
report should be easy to classify with confidence. Posts that mix background
with a broad request for advice are harder. If the model's confident guesses
aren't clearly more accurate than its unsure ones, its confidence means
nothing for my data.


---

<!-- ─────────────────────────────────────────────────────────────────────────
     UNIT 6 — read this before you change anything above.

     If a criterion turns out to be BROKEN rather than merely unmet, you can
     revise it, and that earns credit. But never delete or edit the original
     line. Add the revision underneath, like this:

         ## 2. Every label performs acceptably

         The model performs well on all labels.

         **Why this target:** ...

         > **Revised in unit 6:** Every label has an F1 of at least 0.60 on
         > the held-out set.
         >
         > **Why revised:** "performs well" gave me nothing to check. I
         > couldn't produce a verdict from it at all.

     That's a revision because the criterion couldn't be MEASURED.

     Lowering a target because you missed it is not a revision, and it costs
     you the point:

         ✗ "Overall accuracy of at least 0.65" → "at least 0.55", because
            0.65 turned out to be optimistic for 200 examples.

     A number you missed stays where it is, gets diagnosed, and gets a fix
     attempted. That's where the points are.
     ───────────────────────────────────────────────────────────────────────── -->
