[readme.md](https://github.com/user-attachments/files/33351616/readme.md)
# Modern job search for software engineers

## From code completion to agentic engineering

This is a self-contained, evidence-based playbook for finding work in a software market shaped by coding agents. It is designed to do more than produce a polished resume. Used well, it helps a programmer:

- understand the difference between code completion and agentic development;
- decide which kinds of work are actually desirable;
- learn how different job markets describe that work;
- build credible evidence of modern engineering practice;
- turn a broad career history into role-specific, defensible evidence;
- treat each application and interview as a research cycle;
- improve the search even when an opportunity initially looks like a strong fit; and
- convert interview discoveries into a credible 30/60/90-day proposal.

The central idea is simple:

> Do not begin with “How do I make myself sound right for this job?” Begin with “What does this organization need, what work do I want, and what verified evidence connects the two?”

No other files are required to use this guide. The filenames and directory structures below are optional suggestions for people who want to run their job search as a small, version-controlled project.

## How to use this guide

Read the agentic-development section first if your current AI workflow is mostly autocomplete. Then work through the numbered steps in order for a new search. Return to the relevant step for each application and interview.

A private working directory can help keep facts, preferences, applications, and interview learning separate:

```text
job-search/
  evidence/
    master-evidence.md
    factual-canon.md
  direction/
    career-thesis.md
    target-markets.md
    target-titles.md
    anti-goals.md
  applications/
    Company-Role/
  templates/
  tracker.md
```

Keep private evidence, personal data, interview notes, and employer information out of a public repository. If you publish this guide or your own templates, use fictional examples and verify that no confidential material remains.

## The operating model

The system separates five kinds of information that are often mixed together:

| Layer | Question | Suggested record |
|---|---|---|
| Facts | What did the candidate actually do? | Master evidence file and factual canon |
| Preferences | What kind of work and environment does the candidate want? | Career thesis and anti-goals |
| Market language | How does this market name and describe that work? | Target-title list, saved postings, and market notes |
| Opportunity hypothesis | What does this particular employer appear to need? | Application directory and evidence map |
| Interview evidence | What did the employer reveal, and what did the candidate learn? | Per-round notes, retrospective, and presentation |

Keeping these layers separate prevents three common failures:

- treating a job description as proof that the candidate wants the job;
- turning market keywords into unsupported claims; and
- allowing one exciting opportunity to redefine the entire search.

## For programmers: move from code completion to agentic development

This section is for a programmer whose AI workflow still consists mainly of accepting line or function completions. Code completion remains useful, but it is only one point on a larger spectrum.

The modern shift is from **asking AI to type code** to **delegating a bounded engineering outcome**. An agent can inspect a repository, search for relevant code, form a plan, edit multiple files, run tools and tests, respond to failures, and return a change for human review. GitHub’s current documentation describes coding agents in these terms: they can research, plan, modify code, run work asynchronously, and open pull requests for review ([GitHub agent concepts](https://docs.github.com/en/copilot/concepts/agents), [GitHub agent workflow](https://docs.github.com/en/copilot/how-tos/copilot-on-github/use-copilot-agents/overview)).

That does not make human engineering judgment less important. It changes where that judgment creates value. The 2026 Stack Overflow Developer Survey reports widespread daily AI use alongside conditional trust: developers most often validate output by running it locally, comparing it with the existing codebase, and checking tests or security ([survey overview](https://survey.stackoverflow.co/2026), [validation data](https://survey.stackoverflow.co/2026/ai/data)). A credible modern programmer is therefore neither “AI-free” nor willing to merge whatever a model produces. The valuable skill is controlled delegation with verification.

### Understand the capability ladder

| Mode | What the tool does | What the programmer must do |
|---|---|---|
| Search and documentation | Finds explanations, APIs, or examples | Judge relevance, currency, and authority |
| Code completion | Predicts the next lines in the active file | Keep local intent and correctness in mind |
| Chat or edit assistance | Explains code or proposes a bounded change | Supply context, compare options, and review the patch |
| Interactive agent | Inspects the repository, changes files, runs commands, and iterates | Define the outcome and constraints; monitor, steer, and verify |
| Asynchronous coding agent | Works on a task or issue and returns a branch or pull request | Write a delegable task, review evidence, request revisions, and own the merge decision |
| Agentic workflow | Repeated tasks use defined tools, instructions, checks, and approval gates | Design the workflow, permissions, observability, and failure handling |

The key transition is not a better prompt. It is learning to create an environment in which work can be delegated safely and evaluated objectively.

### What the programmer’s job becomes

Agentic development moves more of the programmer’s attention toward:

- turning ambiguous requests into explicit behavior and acceptance criteria;
- decomposing work into tasks with useful boundaries;
- giving the agent the right repository context without exposing unrelated secrets;
- choosing architecture and interfaces before implementation sprawls;
- deciding what the agent may read, write, execute, or publish;
- creating fast tests, linters, type checks, security checks, and preview environments;
- reviewing diffs for correctness, maintainability, and unintended scope;
- debugging failures the agent cannot explain reliably;
- reconciling concurrent changes and protecting source-of-truth decisions;
- measuring whether automation improved cycle time or merely moved work into review; and
- communicating product and engineering tradeoffs to people.

Typing speed becomes less differentiating. Problem selection, system understanding, taste, verification, and responsibility become more visible.

### Learn the agentic engineering loop

Use this loop for one real task at a time:

```text
Frame -> constrain -> delegate -> observe -> verify -> refine -> integrate -> document
```

1. **Frame the outcome.** State the user-visible or system-visible change, not merely the file to edit.
2. **Constrain the work.** Name non-goals, compatibility requirements, security limits, files that must remain untouched, and what requires approval.
3. **Provide context.** Point to architecture notes, relevant code, conventions, failing tests, and examples of correct behavior.
4. **Ask for a plan when risk is high.** Review the proposed approach before authorizing broad changes.
5. **Let the agent use tools.** A coding agent should be able to inspect, edit, run checks, and react to results within its permission boundary.
6. **Observe the trajectory.** Redirect early when the agent misunderstands the system or expands scope.
7. **Verify independently.** Read the diff, run the checks, exercise edge cases, and compare behavior with the acceptance criteria.
8. **Refine the environment.** When the agent fails repeatedly, improve tests, documentation, task boundaries, or repository instructions instead of endlessly rephrasing the same request.
9. **Integrate deliberately.** The programmer owns the commit, pull request, release, rollback plan, and downstream consequences.
10. **Document durable learning.** Preserve the new invariant, decision, or test so the next human or agent does not rediscover it.

### Build the missing skills deliberately

Use this assessment to identify the next learning project:

| Capability | Beginner behavior | Job-ready evidence |
|---|---|---|
| Task framing | “Build this feature” | Brief with user outcome, constraints, non-goals, and acceptance tests |
| Context management | Pastes a large prompt | Directs the agent to authoritative files and removes irrelevant context |
| Repository literacy | Accepts edits file by file | Traces architecture, ownership, dependencies, and existing conventions |
| Verification | Accepts plausible output | Uses tests, types, linters, security checks, runtime inspection, and manual review |
| Review judgment | Checks whether code runs | Finds scope creep, bad abstractions, missing cases, regressions, and operational risk |
| Tool permissions | Grants broad access | Uses least privilege, approval gates, secret boundaries, and isolated environments |
| Decomposition | Gives one enormous task | Creates independently testable, reviewable work units |
| Recovery | Restarts with a new prompt | Diagnoses why the attempt failed and improves the task or environment |
| Collaboration | Hides the AI workflow | Explains what was delegated, what was verified, and what remains uncertain |
| Measurement | Claims to be “10x” | Shows cycle time, defect, coverage, review, or adoption evidence |

### Use a four-project learning progression

Do not begin with a greenfield application whose quality is impossible to judge. Progress through increasingly realistic work:

1. **Known-code refactor**

   Delegate a refactor in a codebase the programmer understands. Add or strengthen characterization tests first. The exercise tests review quality, not novelty.

2. **Bug investigation**

   Give the agent a reproducible failure and ask it to identify the root cause, propose options, implement the smallest fix, and add a regression test. Compare its explanation with the actual code path.

3. **Small vertical feature**

   Write acceptance criteria for one feature that crosses a user interface, API, and persistence boundary. Require migration safety, error behavior, tests, and documentation.

4. **Repository workflow**

   Automate a recurring maintenance task, such as dependency review, test-gap identification, release-note drafting, or issue triage. Add explicit permissions, dry runs, logs, and a human approval gate.

The goal is not to finish four demos. It is to learn which work delegates cleanly, which context the agent needs, where verification catches mistakes, and how the repository can make correct work easier.

### Turn the learning into portfolio evidence

A modern portfolio should show engineering control, not a collection of generated applications. For each project, include:

- the real problem and why it mattered;
- the task brief and acceptance criteria;
- a small architecture or workflow diagram when useful;
- what was delegated to an agent;
- what the programmer decided personally;
- the tests and checks used as independent evidence;
- an example of a wrong or incomplete agent result that the programmer caught;
- the final tradeoffs and remaining limitations;
- before-and-after measures when they are meaningful; and
- a clean repository history or pull request showing review and iteration.

Do not publish proprietary prompts, employer code, secrets, private transcripts, or model output that the programmer does not have the right to share. The valuable artifact is the reasoning and verified result, not a giant chat log.

### Search for modern work without chasing “AI” titles

The ability to work with coding agents can improve performance in ordinary software roles. It does not require becoming an AI researcher or applying only to jobs with “AI” in the title.

Search by the problems the programmer wants to own:

- product engineering and full-stack feature delivery;
- developer productivity, internal tools, or platform engineering;
- build, test, release, and CI/CD infrastructure;
- quality engineering and automated verification;
- modernization, migrations, and technical-debt reduction;
- security tooling and dependency management;
- data or integration workflows;
- applied AI product engineering;
- AI evaluation, agent infrastructure, or model-tool integration; and
- forward-deployed or solutions engineering when the programmer enjoys discovery and implementation with customers.

Then inspect the posting for modern operating signals:

- ownership of outcomes rather than a ticket queue;
- strong automated tests and code-review practices;
- permission to improve the development system;
- explicit AI-tool policy rather than vague pressure to “use AI”;
- secure access to useful development environments and internal documentation;
- expectations around evaluation, observability, privacy, and human approval;
- teams that value maintainability and operational quality; and
- interview exercises that permit realistic tools and evaluate judgment.

Warning signs include:

- promises that agents eliminate the need for design, testing, or review;
- productivity measured mainly by lines of code or raw output volume;
- pressure to place proprietary data into unapproved tools;
- no clear owner for generated code or production failures;
- “vibe coding” presented as an engineering standard;
- take-home work that asks for a production-sized system without constraints; and
- roles that use “AI-native” to hide understaffing or unlimited scope.

### Translate agentic work into resume evidence

Do not list “AI,” “prompt engineering,” or a vendor name without showing what changed. Use the same intervention-and-outcome standard as any other engineering work.

Weak:

> Used AI coding tools to write code faster.

Stronger:

> Introduced agent-assisted regression-test generation behind mandatory review and CI gates, expanding coverage of legacy parsing cases while preserving the existing public API.

Stronger when supported by real measures:

> Reduced routine dependency-update turnaround from days to hours by delegating patch preparation and test execution to a bounded coding agent; retained human approval for compatibility and security changes.

Only claim measurements the programmer actually captured. The interesting evidence is usually the workflow designed, the risk controlled, the review performed, and the outcome delivered.

### Discuss agent use credibly in interviews

A good answer distinguishes delegation from accountability:

> “I use agents for bounded implementation and investigation when the repository gives me a way to verify the result. I define the behavior and constraints, review the plan when the change is risky, inspect the diff, and run independent checks before I own the change. I do not delegate architecture, security, or production judgment blindly.”

Be ready with one example of each:

- a task an agent completed effectively;
- a plausible result the programmer rejected;
- a task that was too ambiguous or risky to delegate;
- a test or repository improvement that made later delegation safer; and
- a measured outcome, including whether review time offset implementation speed.

Never imply expertise the programmer only borrowed temporarily from a model. If the candidate cannot explain, debug, maintain, and defend the resulting system, it is not yet portfolio evidence.

### Ask employers how they actually use agents

Useful interview questions include:

1. Which development tasks are engineers currently delegating, and which remain human-led?
2. What evidence is required before agent-generated code can merge?
3. Which tools and models are approved for proprietary code and data?
4. How are secrets, permissions, network access, and external tool calls controlled?
5. Has agent use changed code-review load, defect rates, or cycle time?
6. Who owns failures caused by an automated change?
7. Are engineers expected to improve shared instructions, tests, and workflows?
8. How does the interview process evaluate candidates who use modern development tools?

These questions reveal whether the company has an engineering practice or merely a slogan.

### A practical 30-day bridge from completion to agency

| Week | Focus | Deliverable |
|---:|---|---|
| 1 | Learn the loop on familiar code | One reviewed refactor with characterization tests and a written critique of the agent’s patch |
| 2 | Practice diagnosis and constraints | One reproduced bug, root-cause note, minimal fix, and regression test |
| 3 | Delegate a vertical slice | One small feature with acceptance criteria, implementation plan, tests, and manual verification |
| 4 | Build durable workflow proof | One permission-bounded maintenance workflow plus a short case study and resume-ready evidence |

At the end of the month, the programmer should not merely know how to operate a particular tool. They should be able to explain how to define work, delegate it safely, determine whether it is correct, and improve the engineering environment for the next task.

## Step 1: build the candidate’s evidence warehouse

Before tailoring anything, create a broad factual record. Gather old resumes, project summaries, performance reviews, portfolios, talks, writing, product documentation, and personal notes. Extract useful facts into the master list.

Capture more than conventional resume bullets. For each project or role, record:

- the problem or constraint;
- what the candidate personally owned;
- the people or teams served;
- the technical and organizational context;
- tools, interfaces, systems, and methods used;
- scale, such as products, users, sites, teams, revenue, cost, or time;
- the observable result;
- durable artifacts left behind;
- what changed upstream because of the work;
- which statements are estimates or need confirmation; and
- who could corroborate the claim.

Use a simple evidence pattern:

```text
Situation -> personal intervention -> scope/mechanism -> observable result -> durable capability
```

Do not discard relevant facts because they do not fit the current target. The warehouse should remain broader than every generated resume.

### Evidence quality labels

Label uncertain items so later drafts cannot accidentally upgrade them into facts:

- **Confirmed:** directly supported by records or confident recollection.
- **Approximate:** directionally true, but the number or wording needs qualification.
- **Needs verification:** potentially useful, but not ready to publish.
- **Context only:** explains a situation but should not become a public claim.
- **Do not use:** private, legally sensitive, misleading, or otherwise unsuitable.

Every public claim should survive a hiring-manager question and a reference check.

## Step 2: find the work the candidate actually wants

Titles are poor starting points. Begin with work patterns.

Ask the candidate to describe moments when work felt unusually satisfying and unusually draining. For each example, identify:

- the problem being solved;
- the activity performed day to day;
- the user or stakeholder who benefited;
- the degree of ownership;
- whether the work produced a reusable capability or a one-time intervention;
- the pace and ambiguity level;
- the amount of collaboration, persuasion, travel, support, or on-call work; and
- what happened after the candidate finished.

Then convert the discussion into four lists:

1. **More of:** activities, users, problems, and environments that create energy.
2. **Less of:** work the candidate can do but does not want as the center of the job.
3. **Non-negotiables:** location, compensation, schedule, travel, authorization, values, or health constraints.
4. **Unknowns to test:** attractive ideas that have not yet been experienced directly.

### Write a one-sentence career thesis

Use this template:

```text
Build or improve [systems/capabilities] that help [primary users] achieve [valuable outcome], with enough ownership to [desired form of leverage or change].
```

The thesis should describe the shape of good work, not a single title. It is allowed to change as evidence accumulates.

### Define anti-goals

Strong searches name what to avoid. Write down roles that are plausible on paper but repeatedly create the wrong work pattern. For each one, state the condition under which it becomes acceptable.

Example:

```text
Customer-facing engineering is acceptable when repeated customer problems become product, tooling, or documentation improvements. It is a poor fit when success is measured mainly by reactive ticket closure or quota support.
```

This is more useful than a permanent blacklist of ambiguous titles.

### Run small search experiments

If the candidate is unsure, do not force a single answer. Select three to five provisional lanes and run a short experiment in each:

1. Review 10-20 real postings.
2. Save the three most appealing.
3. Identify repeated responsibilities and market vocabulary.
4. Speak with one person doing the work, when possible.
5. Score interest before and after learning the day-to-day reality.

Use a lightweight scorecard from 0 to 2:

| Dimension | 0 | 1 | 2 |
|---|---|---|---|
| Work itself | Mostly undesirable | Mixed | Energizing |
| Primary users | Wrong audience | Acceptable | People the candidate wants to enable |
| Ownership | Executes others’ plans | Partial influence | Can change the system |
| Reusability | Mostly one-off work | Some durable output | Builds lasting capability |
| Evidence | Weak or speculative | Adjacent proof | Strong direct proof |
| Market viability | Rare or impractical | Possible | Enough real openings |
| Life fit | Conflicts with constraints | Manageable | Fits well |

The score is a conversation aid, not an automatic decision. Pay special attention to low scores in “work itself,” “ownership,” and “life fit.”

## Step 3: adapt the search to different job markets

A job market can mean a function, industry, company stage, geography, or economic environment. Tailor the search at all five levels without changing the candidate’s facts.

### Build a market map

For each target market, capture:

| Field | Questions to answer |
|---|---|
| Primary users | Who benefits from this role’s work? |
| Business problem | Why does the company fund this role now? |
| Common titles | What labels appear in real postings? |
| Capability clusters | Which underlying abilities repeat across postings? |
| Proof expected | What projects, scale, metrics, credentials, or artifacts establish credibility? |
| Local vocabulary | Which accurate terms help insiders recognize the work? |
| Constraints | Location, language, authorization, clearance, travel, or hours |
| Hiring pattern | Portfolio review, coding exercise, case study, panel, presentation, or certification |
| Compensation model | Salary, equity, commission, contract, or location bands |
| Risks | Common ways this role differs from its title or becomes undesirable |

Use current postings and conversations as the source for market language. A title list should evolve whenever the market uses an unexpected label for desirable work.

### Translate evidence; do not manufacture it

The same achievement can be framed differently for different markets:

- an infrastructure market may value repeatability, self-service, maintainability, and reduced toil;
- a product market may value customer impact, adoption, revenue, and feedback into the roadmap;
- a regulated market may value traceability, verification, risk controls, and documentation;
- an early-stage company may value ambiguity tolerance, breadth, fast learning, and establishing a function;
- an established company may value scale, cross-team interfaces, governance, and migration without disruption.

The underlying facts remain fixed. Only the selection, order, vocabulary, and explanation change.

Never:

- insert a tool solely because the posting requests it;
- imply direct experience when the evidence is only adjacent;
- invent metrics to make an outcome look complete;
- hide an important constraint; or
- make the resume sound company-specific by flattering the employer.

### Create resume families, not one universal resume

Build one base version for each durable role family. A family should have a coherent professional identity and a repeatable evidence hierarchy. Examples might include:

- engineering tools and infrastructure;
- product or electrical design;
- test automation and validation systems;
- NPI and manufacturing systems;
- customer-facing technical implementation; or
- technical content and developer enablement.

For an individual opening, start from the nearest family and tailor by selection and emphasis. Do not make a new professional identity for every posting.

### Geographic-market adaptation

When moving between regions, verify rather than assume:

- expected resume length and whether a photo or personal details are customary or inappropriate;
- spelling, date, address, and telephone conventions;
- degree and credential equivalence;
- local title and seniority meanings;
- work-authorization disclosure;
- compensation and currency conventions; and
- whether recruiters expect a CV, resume, portfolio, cover letter, or application form.

Legal and cultural norms change. Confirm them from current, authoritative local sources before publishing personal information.

## Step 4: screen an opportunity before writing

Save the full posting with its source URL and capture date in a new application directory:

```text
applications/Company-Role/
  Company-Role-Posting.md
  fit-assessment.md
  evidence-map.md
  Candidate-Role-Company.md
  Candidate-Role-Company.html
  Candidate-Role-Company.pdf
  interview-notes.md
  30-60-90-plan.md
```

Before drafting a resume, produce a short fit assessment:

- one-sentence role mandate;
- the employer’s likely reason for hiring now;
- three strongest reasons to pursue it;
- honest gaps and whether they are direct, adjacent, learnable, or absent;
- life and logistics compatibility;
- organizational risks to test;
- what is known versus inferred; and
- an apply, investigate, or skip recommendation.

Ask one blunt question:

> Would the candidate still want this work if the company name, prestige, and mission language were removed?

## Step 5: create an evidence map

Translate the posting into a small number of capability clusters. Do not match every bullet independently when several bullets describe the same underlying need.

| Employer need | Direct evidence | Adjacent evidence | Missing detail | Gap treatment | Resume location | Interview question |
|---|---|---|---|---|---|---|
| What must this person make possible? | Closest completed work | Transferable analog | Scale, ownership, method, or outcome to confirm | Show, explain, learn, or omit | Profile, selected fit, experience, or tools | What would validate the hypothesis? |

For each major need, ask:

1. What was broken, risky, slow, expensive, or unavailable?
2. What did the candidate personally own?
3. What did the candidate design, build, change, automate, or institutionalize?
4. Who used the result?
5. What was the scale?
6. What changed afterward?
7. What durable artifact or capability remained?
8. Could a former colleague confirm the wording?

Also name three true things that should **not** dominate this application. That subtraction step protects a broad candidate from looking unfocused.

## Step 6: generate and verify the resume

Draft the resume as a testable positioning hypothesis. A useful structure is:

1. role-family headline;
2. two-sentence profile;
3. three or four pieces of unusually relevant proof;
4. selected experience ordered around the role mandate;
5. relevant, supportable tools; and
6. education or credentials.

Strong bullets usually contain at least three elements:

```text
Intervention + technical/organizational scope + observable consequence
```

Review the draft in separate passes:

- **Positioning:** can a recruiter place the candidate correctly in 10 seconds?
- **Missing evidence:** which promises are not yet proven?
- **Technical precision:** are tools, causality, scale, and ownership exact?
- **Subtraction:** what impressive but distracting material should be removed?
- **Defensibility:** can every line survive detailed questioning?
- **Market recognition:** are accurate terms from the target market present?

Export the Markdown with a renderer you trust. The exact tool matters less than checking both the visual result and the extracted text. Keep the source Markdown beside the generated HTML, PDF, or DOCX so future revisions remain auditable.

After every substantive revision:

1. rebuild HTML and PDF;
2. confirm the page count;
3. inspect every rendered page;
4. check headings, breaks, density, alignment, and type size;
5. extract the PDF text to confirm it remains machine-readable;
6. verify links and contact information;
7. confirm that internal comments are absent; and
8. inspect the Git diff for unrelated changes.

Do not solve weak content by silently shrinking the type.

Repeat these editing passes until another revision would mostly rearrange wording instead of revealing stronger evidence.

## Step 7: keep refining the goal when a strong fit appears

A strong match is evidence, not the end of discovery. Excitement can cause premature convergence: the candidate starts treating the first appealing company as the definition of the goal.

When a strong fit appears, write down:

- what specifically feels attractive;
- which parts are verified and which are imagined;
- whether the attraction comes from the work, people, product, prestige, compensation, relief, or scarcity;
- what would make the opportunity fail despite the apparent fit;
- which other employers could provide the same desirable work pattern; and
- what this opportunity teaches about the career thesis.

### Use a disconfirmation pass

Actively look for reasons the initial story may be wrong:

- Is the advertised strategic work actually a small portion of the week?
- Does the role have authority to fix root causes?
- Are resources and approved headcount real?
- Is success measured in the same terms the candidate values?
- Does the manager want the capability described in the posting?
- Is the role open because the organization repeatedly burns people out?
- Will broad ownership mean real influence or merely unbounded cleanup?

Do not turn skepticism into cynicism. The purpose is to replace projection with evidence.

### Maintain two decisions

Keep these decisions separate throughout the process:

1. **Can the candidate perform and win this job?**
2. **Should the candidate want this job?**

A high score on one does not guarantee a high score on the other.

### Update the thesis, not just the application

After every unusually strong or weak reaction, update the broader search model:

- add newly discovered desirable work patterns;
- add warning signs;
- revise title vocabulary;
- clarify non-negotiables;
- note evidence gaps worth filling; and
- create a new resume family only if the lane is durable.

Continue a small amount of market exploration until the offer is accepted. This preserves perspective and prevents scarcity from doing the decision-making.

## Step 8: prepare for each interview round

Create a round-specific plan rather than rehearsing the same generic answers for every interviewer. The checklist below can be copied into each application directory.

### Build an interviewer map

For each interviewer, record:

| Interviewer | Likely responsibility | What they may be protecting | Evidence to emphasize | Questions to ask |
|---|---|---|---|---|
| Name and title | What they own | Schedule, reliability, revenue, team health, architecture, risk, or execution | Two or three relevant stories | Questions only this person can answer |

Research should produce hypotheses, not false familiarity. Give the interviewer room to correct the model.

### Build a steelman question bank

For each likely question, write:

| Likely question | Concern behind it | Headline answer | Supporting story | Follow-up risk |
|---|---|---|---|---|
| “Walk me through your background.” | Can this person tell a relevant, coherent story? | One direct sentence | Evidence tied to this mandate | Rambling into unrelated breadth |

Prepare at least:

- a concise career narrative;
- why this work and this company;
- reason for leaving;
- two or three quantified wins;
- a real failure with a safe, constructive outcome;
- a disagreement with no villain;
- an ambiguous problem;
- a learning example;
- a cross-functional example;
- a likely gap and the truthful bridge; and
- a first-90-days answer stated as hypotheses, not a prewritten verdict.

Say answers aloud. Lead with the answer, then supply evidence. Most initial answers should fit in roughly 60-90 seconds.

### Prepare round-specific materials

Before each round, have one page of notes containing:

- the role mandate;
- the interviewer’s likely priorities;
- three proof points;
- two likely concerns;
- five questions;
- facts learned in earlier rounds that should be confirmed; and
- one sentence describing what the candidate still needs to learn before wanting the job.

## Step 9: use the interview as requirements gathering

An interview is both an evaluation and a discovery session. The candidate should leave with a better model of the organization’s needs than the job posting provided.

### Before the interview

Write a requirements hypothesis:

```text
They appear to need [capability] because [business or technical pressure].
The first visible outcome may be [result].
The largest risks may be [risks].
The unknowns are [questions].
```

### During the interview

Answer the interviewer’s question first. Then, when appropriate, use concise follow-ups to learn:

- What must be true six months after this person starts?
- What triggered the opening?
- Which problem is urgent, and which is merely desirable?
- Who experiences the pain today?
- What has already been tried?
- What prevents the obvious solution?
- Who owns decisions, budget, implementation, and adoption?
- Which dependencies are outside the team’s control?
- What tradeoffs are acceptable?
- What would make leadership call the hire a success?
- Which metric or behavior would change first?
- What failure mode worries this interviewer most?

Capture exact phrases when possible. Employer language is valuable, but do not force every phrase into the resume or repeat confidential information outside the process.

Pay attention to differences among interviewers. Disagreement may reveal unclear ownership, competing success measures, or a role that is still being designed.

If recording or transcription would help, obtain explicit consent from every participant first and follow applicable law and company policy.

### Immediately afterward

Within 15-30 minutes, write a raw debrief:

- questions asked;
- answers given;
- where the answer landed well or poorly;
- new requirements and exact language;
- stakeholders and decision makers;
- constraints, dependencies, and risks;
- contradictions with the posting or earlier rounds;
- promises or follow-ups;
- changes in the candidate’s interest;
- changes in the candidate’s fit assessment; and
- what to test in the next round.

Separate the notes into three labels:

- **Observed:** directly stated or demonstrated.
- **Inferred:** a reasonable interpretation that still needs confirmation.
- **Unknown:** important and unanswered.

Draft the thank-you note while the details are fresh. Reference a specific discussion and, when useful, briefly connect it to relevant evidence. Do not use the thank-you note to deliver an unsolicited consulting report.

## Step 10: turn interview learning into a 30/60/90-day presentation

A 30/60/90 plan should demonstrate listening, prioritization, and execution judgment. It should not pretend the candidate already understands the organization well enough to prescribe a final solution.

### Decide whether a presentation is appropriate

Create one when:

- the interview process requests a plan or case presentation;
- the role is senior, cross-functional, or responsible for establishing a capability;
- enough requirements have been gathered to make the plan specific; or
- the hiring manager welcomes a short follow-up artifact.

Before sending an unsolicited deck, ask whether it would be useful. A concise leave-behind is often better than a large speculative presentation.

### Ground every proposal in evidence

Start with a requirements traceability table:

| Interview evidence | Interpreted requirement | Confidence | Proposed response | Open question |
|---|---|---:|---|---|
| What was said or observed | What it appears to mean | High / medium / low | Experiment, decision, or deliverable | What must be confirmed |

Mark assumptions visibly. Do not include confidential details from one interviewer unless they are appropriate for the full audience.

### Recommended presentation structure

1. **Role mandate**

   One sentence describing the outcome the organization appears to need.

2. **What I heard**

   Three to five requirements, constraints, or success measures gathered during interviews.

3. **Working principles**

   The decision rules that will guide discovery and prevent premature implementation.

4. **Days 0-30: learn and baseline**

   Validate stakeholders, current state, failure modes, workflows, metrics, dependencies, and decision rights. Deliver a shared problem definition and prioritized baseline.

5. **Days 31-60: pilot and prove**

   Select a bounded high-value problem, build or improve a pilot, define adoption and quality measures, and gather feedback. Deliver evidence about what should scale.

6. **Days 61-90: operationalize and roll out**

   Expand the successful approach, document ownership, train users, add observability, and establish a roadmap. Deliver a capability that can continue without heroics.

7. **Measures and review points**

   Show leading indicators, outcome measures, decision gates, and when the plan will be revised.

8. **Open questions and dependencies**

   Name the information, access, authority, staffing, or cross-team commitments still required.

### Use the same planning frame for every phase

| Phase | Outcomes | Activities | Deliverables | Measures | Decisions/dependencies |
|---|---|---|---|---|---|
| 0-30 | What becomes understood or aligned? | Interviews, observation, audits, baselining | Current-state map, baseline, prioritized problem statement | Coverage and confidence, not vanity output | What must be decided or provided? |
| 31-60 | What becomes demonstrably better? | Pilot, integration, user testing | Working pilot and findings | Early quality, time, reliability, or adoption signal | Scale, revise, or stop? |
| 61-90 | What becomes repeatable? | Rollout, documentation, training, monitoring | Operational capability and roadmap | Outcome trend and independent use | Ownership, investment, and next horizon |

### Examples by role family

Adapt the outputs to the work:

- **Engineering tools:** workflow inventory -> pilot automation -> supported self-service platform.
- **Test infrastructure:** failure and coverage baseline -> bounded rig/framework pilot -> release-gated, observable test capability.
- **Design or NPI:** requirements and interface audit -> prototype or DFT improvement -> controlled release and manufacturing feedback loop.
- **Product:** customer/problem synthesis -> narrow discovery or experiment -> roadmap decision and adoption plan.
- **Customer-facing technical role:** account and friction map -> repeatable implementation playbook -> scalable enablement and product-feedback loop.
- **Technical content or DevRel:** audience and journey baseline -> working example/content pilot -> measured curriculum, distribution, and feedback system.

### Presentation rules

- Use the employer’s stated outcomes, not generic management language.
- Show sequencing and tradeoffs, not a long task list.
- Keep the first month discovery-heavy but not passive; include tangible outputs.
- Make the pilot small enough to learn from within 60 days.
- Include adoption, documentation, ownership, and maintenance in the 90-day phase.
- Use ranges and decision gates where dates depend on access or staffing.
- Explain which previous experience informs the approach, without turning the deck into a second resume.
- End with questions that invite correction and collaboration.

The strongest tone is:

> “Based on what I heard, this is the sequence I would test with the team. These assumptions would be the first things I validate.”

## Step 11: close the learning loop after every round

After an interview, rejection, withdrawal, or offer, update four things:

1. **Candidate model:** what the person now knows about preferred work and constraints.
2. **Market model:** titles, vocabulary, hiring patterns, and recurring needs.
3. **Evidence model:** stories or facts that need to be captured, verified, or strengthened.
4. **Interview model:** questions, answers, and framing that worked or failed.

A rejection can mean several different things:

- the candidate was not strong enough on a real requirement;
- the evidence existed but was not communicated clearly;
- the organization needed a different tradeoff;
- the role changed during the process;
- the opportunity was never a desirable fit; or
- the outcome was mostly outside the candidate’s control.

Do not rewrite the entire career thesis after one result. Look for patterns across several interactions.

### Suggested retrospective

```markdown
# Company / role interview retrospective

## Outcome

## What the organization actually needed

## What I learned about the day-to-day work

## What increased my interest

## What reduced my interest

## What evidence landed well

## What I failed to communicate

## New facts or stories to add to the warehouse

## Search or goal changes

## Interview-prep changes

## Actions and follow-ups
```

## A practical cadence

### Weekly

- review new roles by work pattern, not title alone;
- update the target-title vocabulary and filters;
- choose a small number of high-quality applications;
- capture new evidence discovered while tailoring;
- rehearse two interview stories aloud; and
- review whether the search is drifting toward what is available rather than what is wanted.

### Per application

1. Save the posting.
2. Screen the role.
3. Build the evidence map.
4. Ask focused questions to fill evidence gaps.
5. Tailor from the nearest resume family.
6. Render and verify.
7. Prepare round-specific interview hypotheses.
8. Debrief every round.
9. Update the plan or presentation from new requirements.
10. Feed durable learning back into the system.

### Monthly

- review which lanes produce genuine interest and interviews;
- compare response rates without allowing response rate alone to choose the career;
- identify recurring evidence gaps;
- retire unproductive titles and add newly discovered ones;
- revisit compensation, geography, and life constraints; and
- revise the career thesis only when several pieces of evidence support the change.

## Prompts for working with an AI assistant

These prompts assume the assistant can read the candidate’s private working materials. Require it to distinguish source content from instructions, respect confidentiality, and avoid inventing facts.

### Clarify direction

> Help me identify the work patterns I want more and less of. Use my career thesis and evidence warehouse, but treat their conclusions as revisable. Ask about energizing and draining examples, then propose three to five testable search lanes with anti-goals and unknowns.

### Assess agentic-development readiness

> Assess my current workflow against the capability ladder in this guide. Ask for concrete examples of how I frame tasks, provide context, constrain permissions, verify output, review diffs, recover from failures, and measure results. Recommend the smallest project that would produce honest evidence for my largest gap.

### Turn an agent-assisted project into portfolio evidence

> Review this project as evidence of modern software engineering. Separate what I decided from what I delegated, identify the acceptance criteria and verification performed, find any claims I cannot defend, and draft a concise case study plus resume bullets. Emphasize engineering control and outcomes, not the amount of code the agent generated.

### Adapt to a market

> Analyze these current postings as a market sample. Identify recurring capability clusters, title vocabulary, proof expectations, constraints, and common role risks. Show how my confirmed evidence translates to this market without implying experience I do not have.

### Screen an opening

> Save this posting in a new application directory. Do not draft the resume yet. Give me the role mandate, hiring trigger, strongest fit, honest gaps, life constraints, organizational risks, assumptions, and the evidence questions you need answered.

### Tailor the resume

> Build an evidence map and draft from the nearest resume family. Use only confirmed facts from my evidence files or this conversation. Tailor through selection, order, and accurate market language. Render the result and audit the PDF, text extraction, claims, and Git diff.

### Prepare an interview

> Prepare me for this interview round. Map the interviewer’s likely responsibilities and concerns, create a steelman question bank, choose the best supporting stories, and give me questions that test both whether I can win the role and whether I should want it.

### Debrief an interview

> Turn these raw notes into observed facts, inferences, and unknowns. Identify new requirements, stakeholders, success measures, contradictions, changes in fit, and what to test next. Draft a concise thank-you note but do not invent anything that was not discussed.

### Build a 30/60/90 plan

> Use the saved posting and interview notes to build a requirements-traceable 30/60/90-day plan. Separate evidence from assumptions, make the first month discovery-oriented with tangible outputs, define a bounded pilot for days 31-60, and show how days 61-90 operationalize what works. Include measures, decision gates, dependencies, and open questions. Do not pretend to know the company better than the interview evidence supports.

## Final quality standard

The system is working when it produces more than attractive documents. At any point, the candidate should be able to answer:

- What work am I pursuing, and why?
- Which markets call that work by different names?
- What evidence proves I can do it?
- Which gaps are honest and manageable?
- What have interviews taught me about the role and myself?
- What would I test in the first 30 days?
- What would I prove by day 60?
- What would become repeatable by day 90?
- What new evidence would change my current goal?

The resume earns the interview. The interviews improve the requirements. The requirements improve the plan. The plan and the candidate’s reactions improve the career goal. That loop is the system.
