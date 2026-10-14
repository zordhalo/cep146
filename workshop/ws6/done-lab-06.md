# Lab 6: Essay Project, Collaboration, and Fixing Mistakes

Student: Lucas Krawczak
Completed: 2026-10-14 (Exercises 1 and 3; Exercise 2 blocked — see below)
Solo lab (no team requirement).

Repository used: [zordhalo/my-essay](https://github.com/zordhalo/my-essay) — created
**private**. Can be flipped to public if the instructor needs to view it directly.

---

## Exercise 1: Essay Project with GitHub

Created `my-essay` on GitHub, cloned it, built `essay.txt` across three commits.

### Command line method

```
$ git log --oneline
74a2caa Add body paragraph with research
1c7cffd Add introduction paragraph
9df4e14 Add essay title

$ git diff HEAD~2 HEAD
diff --git a/essay.txt b/essay.txt
index 1b15029..32f5ee8 100644
--- a/essay.txt
+++ b/essay.txt
@@ -1 +1,3 @@
 Essay Title: The Impact of Social Media
+Introduction: Social media has changed how we communicate...
+Body: Studies show that social media usage...
```

`HEAD~2` is two saves ago, back when the file was just a title. `HEAD` is now. The
diff is the two lines that showed up in between.

### GitHub website method

The commit list on GitHub shows the same three commits. Clicking each one shows the
added lines in green for that step. Same information as `git diff`, rendered side by
side instead of as plus and minus text.

### Reflection questions

**Which method helps you understand your changes better?**

They answer different questions, so I use both.

The command line is faster and I can point it anywhere. `git diff HEAD~2 HEAD`
compares exactly the two points I care about without leaving the editor. That's the
one I use while I'm actually working.

The website is better for reading a change, especially a big one. Colour-coded,
side by side, no revision syntax to remember. That's the one I use for reviewing
someone else's work.

The real split: command line for changes I made, website for changes I'm judging.

**Can you see how your essay developed over time?**

Yes, and that's entirely because of how the commits were split. Title, then
introduction, then body. One structural move each. The log reads like an outline of
how the document got built.

That only works because the commits are small. One commit saying "final version"
would carry the same file and tell you nothing about how it got there. Small commits
are what turn history into something you can actually read later.

---

## Exercise 2: Collaboration Practice — BLOCKED

This exercise requires forking an instructor-created `class-resources` repository.

**As of 2026-10-14 that repository does not exist.** The `seneca-cep146` organisation
contains only the `cep146` course repo:

```
$ gh repo list seneca-cep146
seneca-cep146/cep146    public    2026-10-09T22:39:54Z

$ gh search repos class-resources --owner seneca-cep146
(no results)
```

Nothing to fork until the instructor publishes it, or tells the class where it
actually lives — a different org, or a private repo needing an invite.

**Action required:** get the `class-resources` URL from the instructor, then run
fork → edit → pull request. The steps don't change:

1. Fork the repository
2. Edit the resources file with the pencil icon, add a study tip
3. Commit as "Add study group tip"
4. Open a pull request explaining the addition

---

## Exercise 3: Fix a Mistake Practice

Committed the error locally and pushed it, then fixed it **on GitHub** rather than
locally, so the correcting commit is authored server-side exactly like the pencil-icon
edit would be.

```
$ git log --oneline
951da1e Correct Canada's capital city      <- the fix, authored on github.com
51c478c Add Canada fact                    <- the mistake
74a2caa Add body paragraph with research
1c7cffd Add introduction paragraph
9df4e14 Add essay title

$ cat facts.txt
The capital of Canada is Ottawa
```

### Observation: the mistake is still in history

```
$ git log -p -- facts.txt
-The capital of Canada is Toronto
+The capital of Canada is Ottawa
...
+The capital of Canada is Toronto
```

The working copy is right. The wrong version is still sitting in commit `51c478c`,
permanently.

Git doesn't erase mistakes. It supersedes them. The record shows what was wrong, who
changed it, when, and the commit message says why.

That's a feature. On a real project, "this value was wrong until March" is often the
entire explanation for a bug someone finds in June. History you can't trust is
history you can't debug with.

The flip side, worth saying once: if what you committed was a password instead of a
wrong capital city, a later commit does not fix it. It's still there, still readable,
still cloned by everyone who pulled. That needs history rewriting, which is a
different and much uglier operation. Supersede fixes wrong. It doesn't fix leaked.

---

## Submission checklist

### Exercise 1 (Essay Project)
- [x] Repository "my-essay" created and cloned
- [x] `essay.txt` with 3 commits showing progressive development
- [x] Evidence of both command line (`git log --oneline`, `git diff HEAD~2 HEAD`) and website
- [x] Answers to reflection questions

### Exercise 2 (Collaboration Practice)
- [ ] **BLOCKED** — instructor's `class-resources` repository does not exist yet

### Exercise 3 (Fix Mistake Practice)
- [x] `facts.txt` created with the intentional Toronto error
- [x] Corrected to Ottawa through GitHub (server-side commit)
- [x] Demonstrated mistake remains in history while current version is correct
- [x] Proper commit message for the correction

**Rubric impact:** 2 of 3 exercises complete lands in the "Fair — 1 mark" band until
Exercise 2 is done. Chase the instructor for the repository.

**Note on screenshots:** terminal output above is reproduced verbatim as text rather
than images. Capture GitHub web UI screenshots if the instructor requires them.

---
*Commands executed and write-up assisted with AI (Claude) per course policy on tool
use, same as Lab 2. Reflections are my own positions — review before submitting.*
