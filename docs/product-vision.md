UniEase — Product Vision

Project: UniEase — Smart Academic Success Platform

Tagline: Plan smarter. Grow stronger. Achieve more.

Document status: Approved product direction; requirements pending user research

Course context: Year 03 — User Experience Designing

Architecture decision: Full-stack web application from the beginning

1\. Vision

UniEase aims to help university students organise academic responsibilities, pursue academic and career aspirations, and understand their progress through an accessible, supportive digital experience.

2\. Problem hypotheses

Students may find it difficult to coordinate coursework across modules, prioritise competing deadlines, turn long-term ambitions into actionable steps, and recognise meaningful progress. These are hypotheses, not research findings. Interviews, surveys and usability tests will establish which needs matter most.

3\. Target users

Primary: university students managing multiple modules, assignments and exams. Secondary use cases to investigate: students preparing for internships, portfolio development and skills milestones. Accessibility needs and different study practices must be considered in research.

4\. Core product principles

\- Make the next useful action obvious.

\- Connect daily academic tasks to meaningful long-term goals.

\- Show transparent progress based on actual recorded activity.

\- Support keyboard use, readable layouts and responsive screens.

\- Respect privacy, autonomy and student control.

\- Avoid punitive streaks, misleading productivity scores and unsupported claims of academic improvement.

5\. Approved feature direction

5.1 Academic dashboard

A focused overview of upcoming deadlines, today's priorities, modules, study sessions and goal progress. Include loading, empty and error states.

5.2 Modules and assignments

Students can create and manage modules; add, edit, complete and prioritise assignments; associate tasks with modules; and view due dates and task status. All actions require validation and ownership checks.

5.3 Calendar and study timetable

Present assignments and planned study sessions in calendar and agenda views. Let students create and update study sessions.

5.4 Targets \& Dreams

Support academic and career goals, such as a target grade, finishing a portfolio, developing a skill or preparing for an internship. Each goal may have a target date, milestones and related tasks. Progress is based on completed milestones or explicit measurable criteria, not AI-generated guesses.

5.5 My Growth

Provide weekly and monthly charts for recorded task completion, study sessions and goal milestones. Recognise verifiable milestones with optional achievement badges. Explain metric definitions; distinguish engagement and task completion from academic performance. Grade trends require actual grade data.

5.6 UniEase AI Study Assistant

A study-focused assistant to explain concepts, help break assignments into steps and suggest revision plans. The assistant should clarify uncertainty, avoid fabricating student progress and support learning rather than academic dishonesty. Personal data is shared with the AI service only when clearly authorised; API credentials remain on the server. Provide graceful failure and cost/rate limits.

5.7 Premium light and dark themes

Create a coherent original design system with both light and dark modes, a persistent user preference, accessible contrast, visible focus states and responsive layouts. The visual direction is premium and calm, not visually cluttered.

5.8 Supporting features

Study notes/resources, focus sessions, deadline reminders and richer analytics are planned, but their priority will be validated during research.

6\. MVP scope and boundaries

MVP target: a secure full-stack student account, modules, assignments, basic calendar/study sessions, goals/milestones, simple progress visualisations and light/dark theme. This is the smallest end-to-end release we intend to test with real students; the exact scope may change after research.

Later increments: rich notes, focus timer, notification delivery, advanced analytics and live AI chat. The AI interface may be prototyped during UX design without claiming a working AI integration.

Not in initial scope: institutional LMS integrations, automatic grade prediction, social networking, and broad mental-health or career counselling claims.

7\. Proposed technical architecture

\- Frontend: React, TypeScript, Vite, responsive CSS/design tokens.

\- Backend: Node.js, Express, TypeScript, versioned REST API.

\- Database: PostgreSQL, Prisma ORM; verify versions and migration workflow during setup.

\- Validation: shared or aligned Zod schemas, with server-side enforcement.

\- Authentication: securely hashed passwords, protected sessions/cookies, authorisation on every student-owned resource, rate limiting and secure recovery design.

\- AI: backend-only integration with secret management, request limits and consent-aware context handling.

\- Testing: unit/component tests, API integration tests, accessibility checks and end-to-end user journeys.

\- Delivery: Git branches and pull requests, environment examples without secrets, automated lint/build/test checks.

Conceptual data entities

User, Module, Assignment, StudySession, Goal, GoalMilestone and (later) Note, Reminder, AIConversation. Relationships and fields will be specified after task-flow and requirements review.

8\. UX research and validation

Begin with a research plan and open-ended student interviews. Use surveys to explore patterns, not to claim statistical representativeness. Record consent, anonymise notes and preserve contradictory findings. Create evidence-based personas, user journeys and task flows. Evaluate task completion, errors, time-on-task and qualitative feedback; test keyboard access and WCAG 2.2 AA considerations.

9\. Success criteria to validate

\- Students can create a module and assignment and locate the deadline without assistance.

\- Students can set an academic or career goal and update a milestone.

\- Students can understand what each growth metric measures.

\- Core tasks work with keyboard navigation and on mobile layouts.

\- Users understand when AI suggestions are generated and what data is shared.

Specific performance targets and success thresholds will be agreed after baseline usability research.

10\. Development sequence

1\. Approve product vision and research plan.

2\. Conduct discovery research and prioritise requirements.

3\. Define flows, information architecture and Figma prototypes.

4\. Set up backend, database, authentication and API contracts.

5\. Build and test core academic workflows end-to-end.

6\. Implement goals, growth insights and both themes.

7\. Validate usability and accessibility; improve the product.

8\. Add AI study assistance and secondary features in planned increments.

9\. Deploy, document and publish an evidence-based portfolio case study.

11\. Open decisions

\- Which students will participate in interviews and testing?

\- Which authentication/session approach best fits deployment?

\- Which hosting and managed PostgreSQL service fit the budget?

\- What student information may be provided to the AI assistant, and how is consent captured?

\- Which progress metrics do students actually find useful?

12\. Decision log

\- Academic management is the primary product focus.

\- Targets \& Dreams covers academic and career aspirations.

\- My Growth uses both charts and optional achievement milestones.

\- The AI chatbot focuses on academic study assistance.

\- The UI supports premium light and dark themes.

\- Full-stack architecture is selected from the beginning.

Integrity note: This document captures product intentions, not completed implementation or validated research findings.

