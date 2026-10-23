# MG628 Week 7 — Decisions Under Uncertainty (Enhanced)

## Deploy

1. Open GitHub repository `monroeu/MG628`.
2. Upload `week07/index.html` to the `week07` directory, replacing the older standalone version.
3. Optionally upload `Decisions_Under_Uncertainty_Study_Guide.pdf` to the repository root.
4. Commit changes; visit https://monroeu.github.io/MG628/week07/ after GitHub Pages updates.

## Existing Supabase integration

This HTML uses the existing project `Monroe University Academic Analytics`, existing `participation-api` Edge Function, standard Supabase Auth student login, and the `bootstrap`, `resume_session`, `start_session`, `card_opened`, `answer_knowledge`, `save_worksheet`, and `recalculate_completion` actions. No service-role key is exposed.

Week 7 assignment slug: `week-07-decisions-under-uncertainty`; assignment ID: `d3cfc7ac-175c-4547-a0fa-691bbd3f1212`.

Content registered: 24 flip cards; 28 server-graded multiple-choice questions with protected answer keys; 6 written exercises. Published offerings were registered for MG628 Fall 2026 sections 155W, 158W, 159W. Opening/closing dates intentionally left unset; configure due dates from Instructor Control Center. Existing roster checks and automatic completion calculation apply.

**Limitations:** End-to-end testing with a real student login was not performed. Public GitHub Pages publication has not been performed. The Edge Function has only two supported track values, `business` and `health`. Public Administration students select `Business / Public Administration` for backend compatibility, and should identify their actual program in their written recommendation. On the shared Supabase client, verify GitHub Pages and Student Portal share the same auth storage key in the same browser. Existing service contains first-attempt locking.


## Revision: Embedded activities and Student ID authentication
- Cards and MCQs are now displayed immediately after their corresponding lesson sections, not in a single activity block at the end.
- Students use their Monroe Student ID and password through the existing `student-auth-api` Edge Function. The returned Supabase session is installed using `supabase.auth.setSession`, and all activity recording continues through `participation-api`.
- Existing Student Portal sessions are reused; student passwords and answer keys are not embedded in the HTML.
- The backend stores 24 flip cards, 28 first-attempt MCQs and six written exercises.
- GitHub Pages deployment: replace `MG628/week07/index.html`; no changes to existing Student Portal or Instructor Control Center code are necessary.
- Perform a live student login, answer submission, and instructor view test before classroom rollout.


## October 2026 first-principles edition
The Week 7 HTML now includes expanded derivations of probability, EMV, variance, Bayes, EVPI/EVSI, expected utility, decision trees, Monte Carlo simulation, sample statistics, t-tests, confidence intervals, correlation, and 3-track recommendations. Embedded interactive EMV, normal-demand Monte Carlo, and CI-width demonstrations run locally. Student ID login and server-side participation API remain unchanged. No simulated practice data is sent as a graded submission.
