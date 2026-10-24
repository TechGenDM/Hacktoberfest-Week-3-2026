My recommendation is to build Warmup — an AI briefing assistant that researches an upcoming interview or meeting for you.

It offers the right combination of genuine usefulness, excellent UI/UX potential, open-weight AI, and a meaningful non-Gemma partner integration. Most importantly, its core experience is achievable within your 10–15-hour build budget.

The official challenge requires a new project built around open-source AI, a clear connection to “Slow and Steady,” an explanation of why open innovation matters, and a demo plus code link. Writing quality is weighted most heavily. 


DEV Community



1. The project: Warmup







freshstartdev.com


Visual direction reference — not a screenshot of the proposed application.

The problem: Before an interview, freelance client call, or important meeting, people waste time opening websites, reading company pages, searching for information, and preparing questions.

The solution: Give Warmup two or three URLs. It reads the pages using a browser agent and prepares a concise, source-linked briefing.

The user spends less time researching and more time preparing.
The main user experience

01 — Drop your links

Enter the company website, job description, and optionally a product page or company article. Specify the role and meeting purpose.




02 — Let the agent research

It visits the pages, extracts relevant information, and uses an open-weight model to synthesize the evidence.




03 — Open your briefing

Receive a company overview, role-specific talking points, thoughtful questions, and a checklist—with links back to the evidence.



What makes it different?
Do not make another chatbot. Make a purpose-built preparation tool.

Its finished briefing should contain:
- The 30-second overview: What the company does and what matters for this conversation.
- What to know: Three important facts grounded in the supplied sources.
- Talking points: Three relevant ideas the user could discuss.
- Questions worth asking: Five thoughtful questions tailored to the role.
- Verify before you go: Important information that the sources did not establish.
- Source shelf: Clickable references so the user can verify claims.
- Take it with you: Copy or export the briefing as Markdown.
If the model cannot find a deadline, requirement, or company fact, it must say so rather than inventing it. That small design decision can make your product feel much more trustworthy.
2. Why I would choose this over other ideas
I compared several directions against your actual constraints: useful for real people, distinctive experience design, feasibility in 10–15 hours, demonstration quality, and fit with non-Gemma partner categories.

These are my qualitative assessments, not measured scores or predictions of winning.
Project idea	Strength	Main drawback
Warmup — meeting/interview briefings	Excellent UX potential; strong Browserbase fit; easy to demonstrate	Live-page extraction needs testing
Link-triage assistant	Great batch workflow; very visual	Can become another generic summarizer
Receipt and return-deadline assistant	Clear consumer value	OCR, retailer policies, and date handling add risk
Generic job application tracker	Useful and easy to understand	Established products such as Huntr and Teal already offer tracking, documents, guidance, and follow-ups.  Huntr Help Center +1
Automatic file organizer	Strong match to the challenge	Safe file operations and undo functionality take time

Warmup is my pick because you can make one small workflow feel exceptionally polished without trying to build an entire platform.
3. The partner category and technology









Best Use of Browserbase
Partner prize: $100 USD


Browserbase is a natural fit because your agent's job is to read live websites. Stagehand is Browserbase's open-source browser automation SDK, with navigation and structured extraction capabilities. 


Browserbase
+1




Recommended stack
Frontend: Next.js + TypeScript + Tailwind CSS

One codebase for the interface and server-side API routes.


Browser agent: Stagehand + Browserbase

Read up to three public URLs per briefing.


AI: Ollama + Qwen3

Run an open-weight model locally to generate the structured briefing. Stagehand documents support for Ollama/Qwen3. 


GitHub





Storage: Browser local storage

Save briefings locally; no account system or database needed.



Use Browserbase for the actual browser session, not just its logo in the interface. Keep API keys on the server, restrict the agent to public HTTP/HTTPS pages, and do not let it submit forms or perform actions on external sites.

One important distinction: with a cloud-hosted Browserbase browser, Warmup is not completely offline. Your model inference can run locally, but browsing happens through Browserbase. Be transparent about that in the README.
4. Your UI/UX direction
I would give Warmup a restrained, editorial design identity—not the typical AI-tool interface filled with gradients, chat bubbles, and glowing effects.









Visual identity

Warm ivory background, deep pine green, charcoal typography, and a restrained coral accent. Strong typography, generous whitespace, clear visual hierarchy, and thin dividers.











Briefing workspace

A compact source rail beside the briefing, with numbered evidence references and clearly separated sections. Avoid burying the useful information in nested cards.











Agent progress

Show real stages—“Opening sources,” “Extracting evidence,” and “Preparing your brief”—with meaningful progress and useful error states.



The detail that can make the UI stand out is the transition from messy research to a calm, ready-to-use briefing. Focus your design effort on that moment, rather than on dozens of screens.
5. The 10–15-hour execution plan
Your PDF gives the deadline as October 25 at 11:59 PM PDT, which is Monday, October 26, at 12:29 PM IST. From the current time on October 24, that leaves roughly 42 hours on the clock. 


DEV Community



Allocate your focused build time like this:
Hour 0–1.5

Validate the core integration

Create a fresh repository. Connect Stagehand to one live public URL and verify that Ollama/Qwen3 can return valid structured output. This is your go/no-go test.


Hour 1.5–4

Build the research pipeline

Read up to three URLs, extract relevant page text, generate the briefing schema, attach source references, and handle failures.


Hour 4–8

Build the main experience

Create the landing form, live progress view, briefing layout, source shelf, and copy/export interaction.


Hour 8–10

Make it trustworthy and polished

Improve typography, spacing, responsive layout, loading/error states, source verification, and local saving.


Hour 10–11.5

Test real scenarios

Test successful URLs, blocked pages, broken URLs, missing facts, malformed model output, and repeated runs.


Hour 11.5–13

Prepare the demo and README

Record a real end-to-end run, document the architecture and setup, and explain why open-weight AI is useful here.


Hour 13–15

Submission and contingency

Fix only the most important remaining issues, capture screenshots, finalize the DEV post, and verify the code/demo links.



Scope you must protect
Do not add authentication, calendar integrations, email integrations, resume uploads, a database, or automatic job applications. They will consume your time without improving the core demo enough.

Your non-negotiable acceptance criteria are:
- A real browser agent reads live pages.
- A real open-weight model generates the briefing.
- The output is structured, useful, and linked to evidence.
- The interface handles success, loading, and failure beautifully.
- The repository has clear setup instructions and the demo is reproducible.
If the Browserbase + local-model integration is still broken after the first 90 minutes, simplify the browser workflow immediately. Do not sacrifice the entire UI and submission to one difficult integration.
6. How to make the submission stand out
The DEV post deserves as much care as the application, since the contest explicitly weights writing quality most heavily. A valid entry also needs the code link, a demo link or video, an explanation of open innovation, the required submission template, and the #hf26challenge tag. Each submission must be a new project completed within the entry period. 


DEV Community



Use this post structure:
1. The problem: Preparing for a conversation should not require a 15-tab research spiral.
2. The product: Demonstrate Warmup reading real URLs and producing a source-linked briefing.
3. The design: Explain how your interface makes research results easier to scan and act on.
4. The technical approach: Show Stagehand, Browserbase, and local Qwen3 working together.
5. Why open innovation matters: Explain local inference, model choice, cost control, and the trade-off introduced by cloud browsing.
6. Evidence: Show a real run, how long it took, which sources were used, what worked, and what remains limited.
7. Reproducibility: Include the repository, installation instructions, and a short demo video.
Do not claim a specific amount of time saved until you have tested the workflow and have a defensible estimate.
My final advice
Build Warmup as a single, excellent workflow, not a feature-rich platform. Make the live research real, the evidence trustworthy, and the interface feel like a polished product someone would genuinely enjoy using.

Your first action should be to validate the Stagehand–Browserbase–Ollama path against one public URL. Once that works, protect the remaining hours for the interface, real-world testing, and submission.
