# TakeMeter

> ### 👋 Start here
>
> **New to this repo? Read [RUNNING.md](RUNNING.md) first** — setup, the
> notebook, the baseline, and what to do when something breaks.
>
> Once `python test.py` passes:
>
> ```bash
> head -5 data/practice_labels.csv     # the shape your labels.csv needs
> ```
>
> Then open `takemeter.ipynb` **in this folder** — in VS Code, or with
> `jupyter notebook` if you prefer. Pick the kernel: the `.venv` inside this
> project. Run section 1, which reports the hardware you'll be training on.
> Everything else waits until you have data.
>
> Nothing to upload, nothing to connect, no accounts and no keys. The notebook
> runs on your machine and writes next to your code.
>
> **The rest of this file is your submission.** Fill it in as you go.

---

<!-- ─────────────────────────────────────────────────────────────────────────
     HOW TO USE THIS FILE

     Unit 5 asks for the first five sections. Unit 6 adds the five below them.

     Everything is pasted as TEXT. No screenshots, no images.

     ⚠️ The confusion matrix especially. The notebook prints one as a markdown
     table, ready to copy. A screenshot of a matrix earns nothing. Paste the
     table.
     ───────────────────────────────────────────────────────────────────────── -->

<!-- ═══════════════════════ UNIT 5 — THE BUILD ═══════════════════════ -->

## What This Does

<!-- Your community, and what your classifier sorts posts into. Three or four
     sentences. -->



---

## Label Taxonomy

<!-- Each label: a one-sentence definition and two real examples from your
     reading. Then your decision rule for the hardest boundary.

     The decision rule is worth a point on its own and it's the thing most
     people leave out. Every taxonomy has a hardest boundary. Name yours. -->

Community: [r/Marathon_Training](https://www.reddit.com/r/Marathon_Training/)

### `specific_question`

**Definition:** A post asking for advice about a particular running problem or decision, with enough detail to identify what the author needs help with.

**Example 1:**
> TODO: paste a real post
To "long run" or not to "long run"?

Hi everyone,

I'm preparing for my first marathon in 7 weeks from now. My goal is to finish it in 5 hours (while enjoying it and not getting injured). I'm male, 40 years old and in good shape. I run already 2 half-marathons in 2 hours but I had a knee injury this year and I had to stop training for 2-3 months (I went swimming, cycling and tried to stay fit though).

I've been doing a simple routine so far (25-30km per week) + gym and physio work for the knees/legs:

- Easy Run
- Tempo Run
- Long Run (max 15km so far)

My question is: should I just continue doing this and increase the milage ~10% per week in the long run or shall I just try to put as many Kms under my belt with easy pace run?

My last long run data: 1:35:00 - 13.82Km - Avg pace 6:53/km at 141 BPM

Do you have any recommendation on how to do the last few weeks or shall I keep doing like this?

Thanks for your help!

**Example 2:**
> TODO: paste a real post
Failed long run (10 weeks out)

Hi r/Marathon_Training community,

Looking for a bit of advice—I'm planning to sign up for a local marathon on October 19th, which gives me about 9–10 weeks of training. Right now, I’ve been averaging 20–25 miles per week for the past couple of weeks.

Today I had a long run scheduled for 11 miles, but my city was under a heat advisory. I got out at 8 a.m., and it was already 80°F with over 90% humidity. I started super slow (~13:30–14:00 min/mi for the first 2 miles), then settled into a ~12:30 pace from miles 3 to 6. I brought two GU gels, planned a Gatorade stop at mile 6, and carried a flask to refill along the way. The first 6–7 miles felt okay, but after that, things went downhill. My heart rate climbed into the 170–180 range, the temp was over 90°F with a heat index above 100, and I had to walk/run the last couple miles. I ended up finishing 10 miles at around a 14:00 pace overall (2:22).

Now I’m wondering: should I take this as a sign that I’m not ready for the marathon? Or chalk it up to tough weather conditions and move on?


### `general_question`

**Definition:** A post asking for broad running advice, recommendations, or tips without a clearly defined problem or decision.

**Example 1:**
> TODO: paste a real post
First Marathon tips

Hi all just signed up for my first marathon (Salt Lake City Marathon) on April 26th. Since it being my first marathon I’m kinda just looking for any tips/info on how the whole process kind of works. One of my questions was about the bib bc some things I saw was that some races ship it to you and some you pick up when you check in but it didn’t say on their website. Other than that i appreciate any tips you all have leading up to the race, the day before, and during the race. Thank you in advance!


**Example 2:**
> TODO: paste a real post

Beginner

Hi everyone,

It’s always been a goal of mine run a marathon, this upcoming year I’m looking forward to at least participating in completing a half marathon.

Please share any tips, training curriculums and advice you would share. I have not ran in a long time so I’m going basically from a couch potato to running. 26F in fairly good health but want to start this up and get the courage to do it, help!

Thanks

### `experience_sharing`

**Definition:** A post sharing personal experiences, marathon results, training
progress, reviews, or opinions without asking readers for advice or
information.

**Example 1:**
> TODO: paste a real post

My first marathon

Completed my first ever marathon yesterday (Sunday 13th october)

Such a blast, really enjoyed it. Such a great experience.

Little bit of context; 2 years ago was around 22stone(132kg) serverly inactive in everything I did.

Lost loads of weight and here we are.

Massive win for me, I'm on Such a high and think I will be for the rest of the week.

16 weeks of training, executed to the best of my ability.

Around the 35/36km point was where I really started to feel it.

But....I AM A MARATHONER FINISHER

**Example 2:**
> TODO: paste a real post

My first marathon humbled me — here's what I learned

Marathon update: 3:45 was doable, but I learned the hard way

A little update after my previous post!
https://www.reddit.com/r/Marathon_Training/comments/1vxsvis/marathon_345_doable/

First of all, thank you to everyone who commented on my original post and gave me advice and encouragement.

Unfortunately, the marathon didn't go quite as planned. I started out way too fast, got carried away, and paid the price later on. I ended up hitting the wall, and the strong headwind certainly didn't make things any easier, especially during the later stages of the race.

Looking back, I think I underestimated just how different running a marathon is compared to shorter distances. My 5K and 10K times gave me confidence, and my training had been going really well. I had completed long runs of 28–32 km that felt relatively comfortable, so I genuinely thought I was ready.

But being in good shape and being able to execute a marathon properly are two different things.

My biggest mistake was going out too hard. I should have stuck to a more conservative pace instead of letting the excitement get the better of me. The headwind was an additional challenge, but I can't blame the conditions for everything. I made the pacing decisions myself, and that's something I need to take responsibility for.

The experience has given me a lot of respect for the marathon distance. It's not just about having the fitness to run the pace — it's about patience, pacing, fuelling, and being able to manage your effort when things start getting tough.

I'm disappointed that I didn't execute the race the way I had hoped, but I'm not disappointed that I did it. If anything, it's made me more motivated to improve.

Next time, I'll be wiser, more patient, and hopefully a lot better at keeping my ego in check during those first few kilometres.

Hit the wall arround 26km mark.

Lesson learned: The marathon doesn't care how fast you can run a 5K. Respect the distance, trust the plan, and don't go out too hard.

Over and out

### The hardest boundary

**Which two labels:** `specific_question` vs. `general_question`

**The decision rule I used every time:**
If the post identifies a particular running problem or decision that the author wants help resolving, classify it as specific_question. Otherwise, if the author asks for broad advice or recommendations without focusing on one problem, classify it as general_question. If the post primarily shares an experience rather than requesting advice, classify it as experience_sharing. 

**Question or not:** If the post asks readers for advice or information
anywhere, it gets a question label, even if most of it is a story. Rhetorical
lines ("Who else is running Chicago?!", "Wish me luck!") don't count as
questions.



---

## The Dataset

<!-- Where you collected from, how you labelled, your counts, and three hard
     cases. -->

**Where the posts came from:**

**How I labelled them:** <!-- Cold first? Pre-labelled with AI and corrected?
Say so plainly — the disclosure is required, not penalised. -->

**Counts per label:**

| Label | Count | Share |
|---|---|---|
|  |  |  |
|  |  |  |
|  |  |  |
| **Total** |  | 100% |

**Three hard cases**

<!-- Any post that made you pause: what it was, which two labels it could have
     been, and what you chose. These are worth more than the easy 190. -->

**1.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**2.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

**3.**
> *The post:*
>
> *Could have been:*
>
> *I chose, because:*

---

## The Training Run

<!-- Your starting model, your settings, and anything you changed and why. -->

**Base model:**

**Settings:** <!-- epochs, learning rate, batch size, seed -->

**Anything I changed from the defaults, and why:**

**Split sizes:** <!-- train / val / test, and per-label counts in the test
split. If a label had fewer than about 8 in test, say so — it explains a lot
of next unit's variance. -->



---

## How I Used AI

<!-- Two specific moments — what you asked, what came back, what you changed.

     ⚠️ Plus disclosure of any pre-labelling. If you had a model pre-label a
     batch and then read and corrected every one, say that. It's an allowed
     workflow and disclosing it costs you nothing. Not disclosing it is the
     problem. -->

**Moment 1**

- *What I asked for:*
- *What came back:*
- *What I changed:*

**Moment 2**

- *What I asked for:*
- *What came back:*
- *What I changed:*

**Pre-labelling disclosure:**

<!-- ═══════════════════════ UNIT 6 — THE TEST ═══════════════════════

     Don't fill these in during unit 5.
     ═══════════════════════════════════════════════════════════════════ -->

---

## Baseline vs. Trained

<!-- Both models on the same posts. `python baseline.py --trained results.json`
     prints this table for you. -->

| Measure | Baseline | Trained | Difference |
|---|---|---|---|
| Overall accuracy |  |  |  |
| Macro F1 |  |  |  |
| F1 — `label_one` |  |  |  |
| F1 — `label_two` |  |  |  |

**What I predicted before I looked:**
<!-- Milestone 1 asks you to write this BEFORE seeing the trained numbers. A
     prediction made afterwards isn't one. -->

**What the gap actually means:**
<!-- If the baseline matched your trained model, your fine-tuning added
     nothing — and that is a real finding, not a failure. Say it plainly. -->



---

## Run Log — Before

<!-- Five criteria across three seeds. The notebook's section 6 prints the
     spread table; the Target and Verdict columns are yours. -->

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1.  |  |  |  |  |  |
| 2.  |  |  |  |  |  |
| 3.  |  |  |  |  |  |
| 4.  |  |  |  |  |  |
| 5.  |  |  |  |  |  |

### Confusion matrix

<!-- ⚠️ TYPED AS A MARKDOWN TABLE. The notebook prints one ready to paste.
     An image of a matrix earns nothing. -->

| true \ predicted |  |  |  |
|---|---|---|---|
| **** |  |  |  |
| **** |  |  |  |
| **** |  |  |  |

**My biggest off-diagonal number, and what it means:**
<!-- Not "the model made mistakes" — WHICH boundary it didn't learn, and which
     direction. "7 real analysis posts were called hot_take and only 3 went the
     other way" is a direction, not just an error rate. -->



---

## Verdicts and Diagnoses

<!-- MET or MISSED against LAST UNIT's target. The target has to hold across
     all three seeds, not turn up sometimes. -->

| # | Criterion | Target | Verdict | How I decided |
|---|---|---|---|---|
| 1 |  |  |  |  |
| 2 |  |  |  |  |
| 3 |  |  |  |  |
| 4 |  |  |  |  |
| 5 |  |  |  |  |

**Diagnoses**

<!-- For each miss: the cause, and how you know. The four common causes are:
     too few examples for a label, a boundary you applied inconsistently, a
     genuinely hard label pair, and a task the model can't reach from this
     much data.

     ⚠️ Use your agreement report as evidence. It is the only instrument you
     have that can tell a LABELLING problem from a MODEL problem, and this
     section is graded on whether you used it that way. -->



---

## Agreement Report

<!-- Your rate against the staff set, and every disagreement adjudicated.

     Remember you labelled these 30 under the STAFF taxonomy in
     data/staff_taxonomy.md, not your own — so every argument below is made
     from those definitions and those decision rules. -->

**Agreement rate:** ___ / 30 = ___%

<!-- Nobody grades this number. A 60% who argues every disagreement from the
     stated rules beats a 95% who wrote "staff was right" nine times. Several
     of the 30 were chosen because they're genuinely ambiguous — you should be
     winning some of these. -->

**Disagreements**

<!-- Three lines each: the post, both labels, and who you think is right and
     why — grounded in the staff definitions you were both applying.

     Then sort each into one of three piles:
       (a) the rule covered it and I applied it loosely → a consistency problem
       (b) the rule genuinely doesn't say               → a gap in the definitions
       (c) the rule is ambiguous here and my reading is defensible → argue it.
           This is a legitimate win.

     Pile (a) is the one that matters most for your diagnosis: if you applied a
     written rule two different ways on 30 posts, that is direct evidence about
     what you did across your own 200. -->

**1.**
> *The post:*
>
> *Staff said / I said:*
>
> *My call, and why:*
>
> *Which pile:*

**2.**
> *The post:*
>
> *Staff said / I said:*
>
> *My call, and why:*
>
> *Which pile:*

**What the pattern in my disagreements tells me:**



---

## The Improvement

**What I changed:**

**Which diagnosis pointed at it:**

### Run Log — After

| Criterion | Target | Seed 42 | Seed 7 | Seed 2024 | Verdict |
|---|---|---|---|---|---|
| 1.  |  |  |  |  |  |
| 2.  |  |  |  |  |  |
| 3.  |  |  |  |  |  |
| 4.  |  |  |  |  |  |
| 5.  |  |  |  |  |  |

**Did it help, and how do I know:**

<!-- If it didn't, say so. Relabelling that didn't help is a genuinely
     interesting result and earns full credit. -->



---

## What's Still Broken

<!-- For each criterion still missed: what you'd do, and why you stopped. -->



**The gap between what I meant my labels to capture and what the model
learned:**
<!-- Two sentences. Your confusion matrix is the evidence. -->



<!-- ═════════════════════════════════════════════════════════════════════

     SUBMISSION CHECKLIST — unit 5

       [ ] criteria.md has five numbered criteria, each naming a NUMBER
       [ ] Each has a reason underneath tied to your data or taxonomy
       [ ] labels.csv: at least 150 rows, text/label/note, ONE file not split
       [ ] No label above 70%
       [ ] All five unit 5 sections have real content
       [ ] Label Taxonomy includes the decision rule for your hardest boundary
       [ ] The Dataset includes three hard cases
       [ ] results.json and test_split.csv committed (the notebook does this)
       [ ] At least four new commits
       [ ] Repository URL submitted — WRITE IT DOWN

     SUBMISSION CHECKLIST — unit 6

       [ ] Baseline vs. Trained table, with your prediction written beforehand
       [ ] Run Log — Before, five criteria across three seeds
       [ ] Confusion matrix TYPED AS A MARKDOWN TABLE
       [ ] A verdict on every criterion
       [ ] A diagnosis for every miss, using the agreement report as evidence
       [ ] Agreement Report with every disagreement adjudicated
       [ ] One improvement, with Run Log — After
       [ ] What's Still Broken
       [ ] results_three_seeds_before.json, results_three_seeds_after.json,
           baseline_results.json and
           agreement_results.json committed
       [ ] At least four new commits
       [ ] The SAME repository URL as last unit

     Do not delete and recreate this repository.
     ═════════════════════════════════════════════════════════════════════ -->

---

📖 **How to run this project: [RUNNING.md](RUNNING.md)**
