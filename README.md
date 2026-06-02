# AI-DLC Workshop Notes

This repository contains personal study notes and summaries from the **AI-DLC Workshop**.

**AI-DLC** stands for **AI-Driven Development Lifecycle**. It is a development approach where AI helps throughout the software development lifecycle, while humans review, decide, and approve the outputs.

> AI asks questions, designs, and writes code.  
> Humans review, decide, and approve.

## Workshop Link

Official AWS Workshop:

https://catalog.us-east-1.prod.workshops.aws/workshops/a1753e26-c705-4920-88f8-09ee62b203eb/en-US

## Repositories

Official AI-DLC GitHub Repository:

https://github.com/awslabs/aidlc-workflows/

---

## What This Workshop Is About

The workshop explains how AI can support software development beyond simple code generation. Instead of asking AI to directly write code, AI-DLC encourages a structured workflow where AI first understands the project, asks clarification questions, creates plans, proposes designs, generates code, helps with testing, and supports operations.

The main idea is that **AI should not only speed up coding**. AI should also help with:

- requirements analysis
- planning
- user stories
- system design
- domain modeling
- code generation
- testing
- deployment
- monitoring
- incident response
- continuous improvement

---

## Why AI-DLC Matters

Many developers think AI improves software development only by making coding faster. However, coding is only one part of software development.

Software development also includes:

- design and analysis
- testing and validation
- communication and coordination
- deployment and monitoring
- maintenance and improvement

That is why AI-DLC focuses on the whole development lifecycle, not only the coding stage.

---

## Key Workshop Images

### Coding Speed Is Not Development Speed

![Root Cause 1: Coding Speed is not Development Speed](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-01-en.png)

### AI-Human Collaboration Flow

![AI-DLC Collaboration Flow](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-02-en.png)

### AI-DLC Development Life Cycle

![AI-DLC Development Life Cycle](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-03-en.png)

### AI-DLC Execution Flow

![AI-DLC Execution Flow](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-04-en.png)

---

## AI-DLC Main Phases

AI-DLC consists of three major phases:

```text
1. Inception
2. Construction
3. Operations
```

---

## Phase 1: Inception

The **Inception** phase transforms business objectives into actionable development units.

This phase is about understanding the project before writing code. Product owners, developers, and AI collaborate to clarify requirements and prepare the project for implementation.

### Main Goals

- Understand the project request
- Identify whether the project is new or existing
- Analyze the current workspace
- Clarify requirements
- Create user stories when needed
- Design application components when needed
- Break complex systems into development units
- Prepare an execution plan

### Main Stages

| Stage | Execution Condition | Key Artifacts |
|---|---|---|
| Workspace Detection | Always | `aidlc-state.md` |
| Requirements Analysis | Always | `requirements.md` |
| Workflow Planning | Always | `execution-plan.md` |
| Reverse Engineering | Existing projects only | `architecture.md`, `component-inventory.md` |
| User Stories | User-facing features | `personas.md`, `stories.md` |
| Application Design | When new components are needed | `components.md`, `services.md` |
| Units Generation | Complex projects | `unit-of-work.md` |

### Simple Explanation

```text
Inception = Understand + Ask + Plan + Design
```

In this phase, AI should not jump directly to code. AI should first understand the project, ask clarification questions, and create a plan.

---

## Phase 2: Construction

The **Construction** phase transforms the development units from the Inception phase into tested, production-ready code.

This phase applies **Domain-Driven Design (DDD)** principles. It starts with domain design and then generates code based on that design.

### Main Goals

- Design business logic
- Define non-functional requirements
- Select technology stack
- Design infrastructure if needed
- Plan code generation
- Generate actual code
- Build and test the system
- Prepare production-ready artifacts

### Main Stages

| Order | Stage | Description | Execution Condition | Key Deliverables |
|---:|---|---|---|---|
| 1 | Functional Design | Technology-independent business logic design | Conditional, per unit | `domain-entities.md`, `business-rules.md` |
| 2 | NFR Requirements | Non-functional requirements and technology stack selection | Conditional, per unit | `nfr-requirements.md`, `tech-stack-decisions.md` |
| 3 | NFR Design | Define NFR patterns and logical components | Conditional, per unit | `nfr-design-patterns.md`, `logical-components.md` |
| 4 | Infrastructure Design | Map logical components to infrastructure | Conditional, per unit | `infrastructure-design.md`, `deployment-architecture.md` |
| 5 | Code Planning | Establish detailed code generation plan | Always | `code-generation-plan.md` |
| 6 | Code Generation | Generate actual code according to the plan | Always | `src/`, `tests/` |
| 7 | Build and Test | Build and run comprehensive tests | Always | `build-instructions.md`, test results |

### Simple Explanation

```text
Construction = Design → Code → Test
```

In this phase, AI helps convert domain models, business rules, and design documents into actual application code and tests.

---

## Phase 3: Operations

The **Operations** phase deploys the built system to a production environment and uses AI-driven monitoring to improve operational efficiency.

This phase focuses on proactive problem detection, automated incident response, reliability, security, performance, and continuous improvement.

### Main Goals

| Goal | Description |
|---|---|
| Deployment Automation | Consistent deployments with Infrastructure as Code |
| Intelligent Monitoring | Real-time analysis of telemetry data |
| Predictive Problem Resolution | Detection and response before issues occur |
| Continuous Improvement | Performance optimization and cost reduction |

### 6-Step Process

```text
1. AI prepares the deployment unit
2. Human approves the deployment
3. AI continuously monitors the system
4. AI generates operations guidebooks
5. AI predicts problems and suggests solutions
6. Human maintains operational excellence
```

### Three Pillars of Operational Excellence

```text
1. Reliability
2. Security
3. Performance
```

### Simple Explanation

```text
Operations = Deploy → Monitor → Detect → Respond → Improve
```

In this phase, AI helps monitor the system, predict possible issues, recommend fixes, and support continuous improvement. Humans still validate, approve, and govern production decisions.

---

## Notes Included in This Repository

This repository contains the following workshop notes:

| File | Description |
|---|---|
| `Understanding-AI-DLC-Note.md` | Introduction to AI-DLC and its main concept |
| `AI-DLC-Core-Framework-Note.md` | Overview of the AI-DLC core framework |
| `AI-DLC-Inception-Phase-Note.md` | Notes about the Inception phase |
| `AI-DLC-Construction-Phase-Note.md` | Notes about the Construction phase |
| `AI-DLC-Operations-Phase-Note.md` | Notes about the Operations phase |

---

## Suggested Repository Structure

```text
AI-DLC-workshop/
├── README.md
├── Understanding-AI-DLC-Note.md
├── AI-DLC-Core-Framework-Note.md
├── AI-DLC-Inception-Phase-Note.md
├── AI-DLC-Construction-Phase-Note.md
└── AI-DLC-Operations-Phase-Note.md
```

---

## Learning Outcomes

After studying this workshop, learners should understand:

- what AI-DLC is
- why AI-DLC is more than AI code generation
- how AI and humans collaborate in software development
- how to use AI for requirements analysis and planning
- how to transform business objectives into development units
- how to generate code from domain and design documents
- how to test and verify AI-generated code
- how AI can support deployment, monitoring, and operations
- why human review and approval are still required

---

## Key Takeaways

```text
AI-DLC is not only about faster coding.
AI-DLC is about better collaboration, better planning, better design, better validation, and better operations.
```

The most important principle is:

```text
AI assists.
Human reviews.
Human decides.
Human approves.
```

---

## Summary

AI-DLC is a structured approach for using AI across the complete software development lifecycle. It helps teams move from business objectives to production-ready systems through three phases:

```text
Inception → Construction → Operations
```

In the Inception phase, AI helps understand and plan the project.  
In the Construction phase, AI helps design, generate, build, and test the code.  
In the Operations phase, AI helps deploy, monitor, detect problems, and improve the system.

The complete AI-DLC cycle balances AI speed with human judgment.
