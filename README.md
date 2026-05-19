# Wendy / 詹文婷 | AI Engineering · Backend · LLM Applications · Document Intelligence

信息与计算科学本科，数学学院背景。关注 LLM 应用、文档智能、后端 API / 自动化工作流，以及把 AI 功能做成可运行、可审核、可测试的工程系统。

<p>
  <a href="https://Wendy-James.github.io/"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-GitHub%20Pages-0969da?style=flat-square"></a>
  <img alt="Open to internships" src="https://img.shields.io/badge/Open%20To-AI%20%7C%20Backend%20%7C%20LLM%20Internships-0f766e?style=flat-square">
  <img alt="Python" src="https://img.shields.io/badge/Python-Workflow%20Automation-3776ab?style=flat-square&logo=python&logoColor=white">
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-ES6+-f7df1e?style=flat-square&logo=javascript&logoColor=111">
  <img alt="Vue" src="https://img.shields.io/badge/Vue-2.x-42b883?style=flat-square&logo=vue.js&logoColor=white">
</p>

## 30-Second Fit

- Target roles: AI Engineer Intern, Backend Engineer Intern, LLM Application Engineer, Software Engineer Intern, Data / Algorithm related intern.
- Core direction: LLM applications, document intelligence, backend workflow automation, AI-assisted business tools.
- Engineering habits: README first, module boundaries, API contracts, dry-run safety gates, privacy constraints, local automated safety tests.
- Math foundation: 信息与计算科学 + 数学学院训练，关注数据结构、模型评估、优化问题和可解释输出。
- Product mindset: 不只做页面 Demo，更关注输入、处理、生成、人工审核、日志、测试和异常处理的闭环。

## Featured Work

| Project | Status | Stack / Area | What to Look At |
|---|---|---|---|
| [外贸全品类获客助手 / AI B2B Outreach Workbench](https://github.com/Wendy-James/waimao-quanpinlei-huoke-zhushou) | Public repo / local workflow project | Python, local web console, workflow scripts, automated safety tests | Campaign workflow, lead research and scoring, email dry-run, send safety gates, reply triage, anonymized supplier RFQ |
| AI Job Search / Interview Assistant | Project experience, public code to be organized | LLM application workflow, JD parsing, resume generation, interview prep | JD parsing, resume tailoring, interview question flow, human review loop |
| Document Intelligence Research | Academic research, provincial project lead | Document structuring, requirement understanding, multi-scenario adaptation | Structured extraction thinking, scenario adaptation, evaluation and research documentation |
| 5G Network Slicing for Intelligent Transportation | Academic / algorithm research | Network performance, optimization strategy, data / algorithm analysis | Performance modeling, resource allocation thinking, traffic scenario analysis |
| [AI Document Q&A Assistant Prototype](https://github.com/Wendy-James/ai-zhishi-zhushou) | Public frontend prototype | HTML, CSS, JavaScript, Fetch API | Document upload UI, chat-style Q&A, `POST /upload` and `POST /ask` API contract, answer/reference display slots |
| [Vue 2 Admin Dashboard Practice](https://github.com/Wendy-James/mas-chuangzuozhe-houtai) | Public frontend engineering project | Vue 2, Element UI, Vue Router, Axios, ECharts | Login flow, token request interception, admin routes, CRUD pages, table/form/upload components |

## Case Study: 外贸全品类获客助手 / AI B2B Outreach Workbench

This is my strongest engineering sample so far: a local, human-in-the-loop Python workbench for turning a loosely defined business process into auditable workflow modules.

Repository: [waimao-quanpinlei-huoke-zhushou](https://github.com/Wendy-James/waimao-quanpinlei-huoke-zhushou)

What it covers:

- Campaign creation, ICP / keyword breakdown, candidate lead import and deduplication.
- Website research, lead scoring, personalized draft generation and compliance checks.
- QQ email dry-run, `READY_TO_SEND` gate, domain frequency limit, blacklist / unsubscribe blocking.
- Reply triage, suggested response drafting, CRM status update and follow-up planning.
- Supplier-side anonymized RFQ routing, privacy leak detection and sanitized supplier resources.
- Chrome form assistant that fills contact forms but does not submit, bypass captcha or make business commitments.

Safety and verification:

- Default mode is dry-run; real sending requires explicit confirmation and runtime authorization.
- Authorization codes are not stored in code, CSV, logs, Markdown or test reports.
- High-risk content, formal quotes, contracts, payment, certificate, inventory and delivery promises require human review.
- Local automated safety tests cover core entrypoints, send gates, secret scanning, RFQ anonymization, form non-submission and web runtime checks.

## Public Repositories to Pin

1. [外贸全品类获客助手 / AI B2B Outreach Workbench](https://github.com/Wendy-James/waimao-quanpinlei-huoke-zhushou)
2. [AI Document Q&A Assistant Prototype](https://github.com/Wendy-James/ai-zhishi-zhushou)
3. [Vue 2 Admin Dashboard Practice](https://github.com/Wendy-James/mas-chuangzuozhe-houtai)
4. [Open Source Engineering Reading Notes](https://github.com/Wendy-James/open-source-reading-notes)
5. [Wendy Engineering Portfolio](https://github.com/Wendy-James/Wendy-James.github.io)
6. Early learning projects only if there is an extra slot; they are useful history, not the main signal.

## Technical Keywords

| Area | Keywords |
|---|---|
| AI / LLM Applications | JD parsing, resume generation, interview assistant, document upload, Q&A UI, extraction and generation workflow, human review |
| Backend / Automation | Python, local web console, workflow scripts, API contract, file processing, dry-run, safety gate, logging, automated checks |
| Document Intelligence | document structuring, field extraction, requirement understanding, multi-scenario adaptation, explainable output |
| Frontend | Vue 2, Element UI, Vue Router, Axios, ECharts, HTML, CSS, JavaScript |
| Engineering Practice | README documentation, module split, privacy boundary, mock data, failure reason, testable workflow |

## Open Source Reading

I use open-source projects as engineering references, not as claimed ownership. Notes are collected in [open-source-reading-notes](https://github.com/Wendy-James/open-source-reading-notes).

| Project | Reading Focus |
|---|---|
| [vuejs/core](https://github.com/vuejs/core) | reactivity, component runtime, compiler, TypeScript organization |
| [element-plus/element-plus](https://github.com/element-plus/element-plus) | enterprise UI components, forms, tables, theme variables, component APIs |
| [ant-design/ant-design](https://github.com/ant-design/ant-design) | design system, complex component states, documentation and tests |
| [vercel/next.js](https://github.com/vercel/next.js) | routing, rendering modes, server-side capabilities, developer experience |
| [fastapi/fastapi](https://github.com/fastapi/fastapi) | API design, validation, OpenAPI docs, async backend patterns |
| [microsoft/TypeScript](https://github.com/microsoft/TypeScript) | type inference, compiler structure, language service, refactor safety |

## Scope Notes

- The AI knowledge assistant is a frontend prototype with explicit backend API expectations, not a completed model service.
- Research and academic projects are listed as experience, not presented as public software repositories unless code/materials are available.
- The automation project is designed around safe local dry-run, mock data and explicit human review; no real customer data or credentials should be committed.

## Currently Improving

- TypeScript, React, Node.js / SQL backend basics.
- Algorithms, computer networks, operating systems, databases and system design communication.
- Turning existing AI and research projects into cleaner public repos with screenshots, test notes and deployment notes.
- Writing more precise English project summaries and engineering documentation.

## Links

- Portfolio: [https://Wendy-James.github.io/](https://Wendy-James.github.io/)
- GitHub: [https://github.com/Wendy-James](https://github.com/Wendy-James)
- Contact: [GitHub Issues](https://github.com/Wendy-James/Wendy-James/issues)

---

English snapshot: AI / backend internship candidate with a math background, focused on LLM application workflows, document intelligence, Python automation, and honest engineering evidence.
