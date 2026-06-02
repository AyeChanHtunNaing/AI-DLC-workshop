# AI-DLC Core Framework Note

# 1. AI-DLC Core Framework ဆိုတာဘာလဲ?

**AI-DLC** ဆိုတာ **AI-Driven Development Lifecycle** ဖြစ်ပါတယ်။  
Software development လုပ်တဲ့အခါ AI နဲ့ လူသား developer တွေ ပူးပေါင်းပြီး requirement analysis, design, code generation, testing, deployment, monitoring စတဲ့ အဆင့်တွေကို စနစ်တကျလုပ်ဆောင်တဲ့ development framework ဖြစ်ပါတယ်။

AI-DLC ရဲ့ အဓိကအယူအဆက—

```text
AI helps with speed, planning, decomposition, and code generation.
Humans handle verification, decision-making, and oversight.
```

မြန်မာလိုဆိုရင်—

```text
AI က မြန်မြန်ဆန်ဆန် စဉ်းစားကူတယ်၊ plan ဆွဲကူတယ်၊ task ခွဲကူတယ်၊ code ရေးကူတယ်။
လူက မှန်/မမှန် စစ်တယ်၊ ဆုံးဖြတ်တယ်၊ approve လုပ်တယ်။
```

AI-DLC မှာ AI က coding assistant တစ်ခုတည်းမဟုတ်ပါဘူး။  
AI ကို development lifecycle တစ်ခုလုံးမှာ collaborator တစ်ယောက်လို အသုံးပြုပါတယ်။

---

# 2. Collaboration Flow

![AI-DLC Collaboration Flow](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-02-en.png)


## ပုံရဲ့ အဓိကအဓိပ္ပါယ်

ဒီပုံက **AI နဲ့ လူသား developer တွေ ဘယ်လိုပူးပေါင်းလုပ်ဆောင်လဲ** ဆိုတာကို ပြထားပါတယ်။

AI-DLC က **AI-Human Collaboration** ကို အခြေခံထားတဲ့ development standard အသစ်တစ်ခုဖြစ်ပါတယ်။

## The Role of AI

AI ရဲ့ တာဝန်က—

```text
Planning လုပ်ကူခြင်း
Task decomposition လုပ်ခြင်း
Architecture proposal ပေးခြင်း
Clarification questions မေးခြင်း
Development deliverables ထုတ်ပေးခြင်း
```

AI က project တစ်ခုလုံးကို စနစ်တကျ ခွဲခြမ်းစိတ်ဖြာပြီး developer တွေ လုပ်ရမယ့်အလုပ်တွေကို အဆင့်လိုက် စီစဉ်ကူညီပေးပါတယ်။

## The Role of Humans

လူသား developer / team ရဲ့ တာဝန်က—

```text
AI မေးတဲ့မေးခွန်းတွေကို ဖြေခြင်း
AI ထုတ်ပေးတဲ့ deliverables တွေကို review လုပ်ခြင်း
မှန်/မမှန် verify လုပ်ခြင်း
ဆုံးဖြတ်ချက်ချခြင်း
Approval ပေးခြင်း
Oversight လုပ်ခြင်း
```

## AI-Human Collaboration Flow

AI နဲ့ လူသားကြားမှာ ဒီလို communication loop ရှိပါတယ်။

```text
AI → Questions for Clarification → Human
Human → Answers to the Questions → AI
AI → Development Deliverables → Human
Human → Review / Approval of Deliverables → AI
```

ဒီ flow က **AI က အလုပ်တွေကို generate လုပ်ပေးပြီး လူက review/approve လုပ်တဲ့ process** ဖြစ်ပါတယ်။

## Key Message

```text
AI-DLC is the new standard where AI's speed and human judgment achieve balance.
```

မြန်မာလို—

> AI-DLC ဆိုတာ AI ရဲ့ မြန်ဆန်မှုနဲ့ လူသားရဲ့ ဆုံးဖြတ်နိုင်စွမ်းကို မျှတအောင်ပေါင်းစပ်ထားတဲ့ development approach ဖြစ်ပါတယ်။

---

# 3. 3-Phase Development Lifecycle

![AI-DLC Development Life Cycle](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-03-en.png)

## ပုံရဲ့ အဓိကအဓိပ္ပါယ်

AI-DLC မှာ development lifecycle ကို phase ၃ ခုနဲ့ သွားပါတယ်။

```text
Inception → Construction → Operations
```

အဆင့်တစ်ခုချင်းစီက နောက်အဆင့်အတွက် context ပိုကောင်းအောင် တည်ဆောက်ပေးပါတယ်။

## Phase 1: Inception

**Inception** ဆိုတာ project ကို define လုပ်တဲ့အဆင့်ပါ။

ဒီအဆင့်မှာ—

```text
Project scope သတ်မှတ်ခြင်း
Requirements စုဆောင်းခြင်း
AI နဲ့ Q&A လုပ်ခြင်း
User stories စဉ်းစားခြင်း
High-level architecture စဉ်းစားခြင်း
```

လုပ်ပါတယ်။

Example:

```text
User က “online booking app တစ်ခုလုပ်ချင်တယ်” လို့ပြောတယ်။
AI က booking type, user roles, payment, notification, admin dashboard စတဲ့ requirement များကို မေးတယ်။
```

## Phase 2: Construction

**Construction** ဆိုတာ plan နဲ့ design အပေါ်မူတည်ပြီး software ကို တည်ဆောက်တဲ့အဆင့်ပါ။

ဒီအဆင့်မှာ—

```text
Functional design
NFR requirements
Infrastructure design
Code generation
Build and test
```

လုပ်ပါတယ်။

Example:

```text
AI က API, database schema, frontend components, tests တွေကို generate လုပ်ကူနိုင်တယ်။
Human က code review, security review, test result review လုပ်ရတယ်။
```

## Phase 3: Operations

**Operations** ဆိုတာ application ကို deploy လုပ်ပြီး run/monitor/maintain လုပ်တဲ့အဆင့်ပါ။

ဒီအဆင့်မှာ—

```text
Deployment
Monitoring
Logging
Incident response
Rollback planning
Performance improvement
```

လုပ်ပါတယ်။

Example:

```text
Production မှာ API 500 error ဖြစ်လာရင် AI ကို logs ပြပြီး possible root cause မေးနိုင်တယ်။
ဒါပေမယ့် rollback လုပ်မလား၊ hotfix လုပ်မလားကို လူကဆုံးဖြတ်ရတယ်။
```

## ဒီ Lifecycle ရဲ့ အကျိုးကျေးဇူး

ပုံထဲက message အရ AI-DLC က—

```text
Structured context ကို AI နဲ့ Q&A လုပ်ပြီး အဆင့်လိုက်တည်ဆောက်နိုင်တယ်။
Cross-team collaboration ကို ပိုစနစ်ကျစေတယ်။
Enterprise-grade quality ကို standardized process နဲ့ ထိန်းနိုင်တယ်။
```

အတိုချုပ်—

> AI-DLC သည် project အစမှ production အထိ AI နဲ့ လူသားအလုပ်လုပ်ပုံကို lifecycle အနေနဲ့ စနစ်တကျ သတ်မှတ်ပေးတဲ့ framework ဖြစ်ပါတယ်။

---

# 4. AI-DLC Execution Flow

![AI-DLC Execution Flow](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-04-en.png)

## ပုံရဲ့ အဓိကအဓိပ္ပါယ်

ဒီပုံက AI-DLC ကို  project တစ်ခုမှာ ဘယ်လို execution flow အဖြစ် လုပ်ဆောင်လဲဆိုတာကို ပြထားပါတယ်။

AI-DLC Execution Flow မှာ အဓိက phase ၃ ခုပါဝင်ပါတယ်။

```text
1. Inception
2. Construction
3. Operations
```

---

## 4.1 Inception Phase

Inception phase သည် project scope, requirements, high-level structure တွေကို define လုပ်တဲ့အဆင့်ပါ။

ပုံထဲမှာ Inception phase ထဲမှာ အောက်ပါ stages တွေ ပါပါတယ်။

```text
requirements-analysis
user-stories
application-design
units-generation
```

### requirements-analysis

Role:

```text
Define System Requirements
```

လုပ်ဆောင်ချက်—

```text
Intent analysis
Functional requirements
Non-functional requirements
Deliverable: requirements.md
```

အဓိပ္ပါယ်—

> User request ကို သေချာနားလည်ပြီး system requirement အဖြစ် ပြောင်းရေးတဲ့အဆင့်ဖြစ်ပါတယ်။

### user-stories

Role:

```text
Define Features from User Perspective
```

လုပ်ဆောင်ချက်—

```text
Persona
Story
Gherkin Acceptance Criteria
Deliverables: personas.md, stories.md
```

အဓိပ္ပါယ်—

> Feature တွေကို user perspective ကနေ ရေးပြီး ဘာကို ဘာကြောင့်လုပ်ချင်တယ်ဆိုတာ ဖော်ပြတဲ့အဆင့်ဖြစ်ပါတယ်။

Example:

```text
As a customer,
I want to search for products,
so that I can find what I need quickly.
```

### application-design

Role:

```text
Design System Architecture
```

လုပ်ဆောင်ချက်—

```text
Components
Services
Dependencies
Deliverables: components.md, services.md, component-dependency.md
```

အဓိပ္ပါယ်—

> System structure, component relationship, service dependency တွေကို design လုပ်တဲ့အဆင့်ဖြစ်ပါတယ်။

### units-generation

Role:

```text
Configure Development Units
```

လုပ်ဆောင်ချက်—

```text
Divide stories into units
Deliverables: unit-of-work.md, unit-of-work-story-map.md
```

အဓိပ္ပါယ်—

> Project အကြီးကြီးကို unit သေးသေးလေးတွေခွဲပြီး implementation လုပ်လို့ရအောင် စီစဉ်တဲ့အဆင့်ဖြစ်ပါတယ်။

---

## 4.2 Construction Phase

Construction phase သည် detailed design, code generation, build, testing တွေကို unit တစ်ခုချင်းစီအတွက် လုပ်ဆောင်တဲ့အဆင့်ပါ။

ပုံထဲမှာ Construction phase ထဲမှာ အောက်ပါ stages တွေ ပါပါတယ်။

```text
functional-design
nfr-requirements
nfr-design
infrastructure-design
code-generation
build-and-test
```

### functional-design

Role:

```text
Model Business Logic
```

လုပ်ဆောင်ချက်—

```text
Domain
Rules
Logic
Deliverables: domain-entities.md, business-rules.md, business-logic-model.md
```

အဓိပ္ပါယ်—

> Business logic ကို code မရေးခင် model လုပ်ထားတဲ့အဆင့်ဖြစ်ပါတယ်။

Example:

```text
Order total = item subtotal + shipping fee - discount
Out-of-stock products cannot be checked out
Payment failed ဖြစ်ရင် order status = payment_failed
```

### nfr-requirements

Role:

```text
Define Non-Functional Requirements
```

လုပ်ဆောင်ချက်—

```text
Quality metrics
Tech stack
Deliverables: nfr-requirements.md, tech-stack-decisions.md
```

အဓိပ္ပါယ်—

> Performance, security, scalability, reliability စတဲ့ system quality requirement တွေကို သတ်မှတ်တဲ့အဆင့်ဖြစ်ပါတယ်။

Example:

```text
Page load time < 3 seconds
Passwords must be hashed
System should support many concurrent users
```

### nfr-design

Role:

```text
Design Quality Attributes
```

လုပ်ဆောင်ချက်—

```text
Patterns
Components
Mapping
Deliverables: nfr-design-patterns.md, logical-components.md
```

အဓိပ္ပါယ်—

> NFR တွေကို ဘယ် design pattern, component, architecture နဲ့ ဖြည့်ဆည်းမလဲဆိုတာ design လုပ်တဲ့အဆင့်ဖြစ်ပါတယ်။

Example:

```text
Use caching for performance
Use retry pattern for reliability
Use RBAC for security
Use pagination for large lists
```

### infrastructure-design

Role:

```text
Design Infrastructure Configuration
```

လုပ်ဆောင်ချက်—

```text
Cloud
CI/CD
Cost
Deliverables: infrastructure-design.md, deployment-architecture.md
```

အဓိပ္ပါယ်—

> Application ကို production မှာ run ဖို့ cloud, server, CI/CD, deployment architecture တွေကို design လုပ်တဲ့အဆင့်ဖြစ်ပါတယ်။

Example:

```text
Frontend: CDN/static hosting
Backend: container service
Database: managed database
CI/CD: GitHub Actions
Monitoring: Cloud monitoring service
```

### code-generation

Role:

```text
Generate Code
```

လုပ်ဆောင်ချက်—

```text
Planning
Generation
Tracking
Deliverables: actual code, tests, deployment artifacts
```

အဓိပ္ပါယ်—

> Approved design အပေါ်မူတည်ပြီး actual source code, tests, deployment artifacts တွေ generate လုပ်တဲ့အဆင့်ဖြစ်ပါတယ်။

### build-and-test

Role:

```text
Verify Quality
```

လုပ်ဆောင်ချက်—

```text
Build
Test
Results
Deliverables: build-instructions.md, *-test-instructions.md
```

အဓိပ္ပါယ်—

> Code ကို build လုပ်ပြီး tests run လုပ်ကာ quality ကို စစ်တဲ့အဆင့်ဖြစ်ပါတယ်။

Example commands:

```bash
npm run build
npm test
```

or

```bash
mvn test
mvn package
```

---

## 4.3 Operations Phase

Operations phase သည် production deployment နဲ့ operational systems တွေကို establish လုပ်တဲ့အဆင့်ပါ။

ပုံထဲမှာ Operations phase ထဲမှာ—

```text
operations
```

stage ပါပါတယ်။

### operations

Role:

```text
Establish Operations Framework
```

လုပ်ဆောင်ချက်—

```text
Deployment
Monitoring
Incident response
Deliverables: confirmation needed
```

အဓိပ္ပါယ်—

> Application ကို production မှာ deploy လုပ်ပြီး monitoring, logging, incident response စတဲ့ operations setup တွေကို စီစဉ်တဲ့အဆင့်ဖြစ်ပါတယ်။

Example:

```text
Deploy to production
Set up monitoring
Set up alerting
Prepare rollback plan
Create incident response checklist
```

---

# 5. Overall Deliverable Structure

AI-DLC သည် application code, IaC code, test code များအပြင် design documents များကိုလည်း ထုတ်ပေးပါတယ်။  
ပုံထဲမှာ **over 12 design documents** ထုတ်ပေးနိုင်တယ်လို့ ဖော်ပြထားပါတယ်။

## Main Folder

```text
aidlc-docs/
├── audit.md
├── aidlc-state.md
├── inception/
└── construction/
```

### audit.md

```text
Audit trail for all decisions
```

AI-DLC process အတွင်း decision တွေကို မှတ်တမ်းတင်ထားတဲ့ file ဖြစ်ပါတယ်။

### aidlc-state.md

```text
Current progress state
```

လက်ရှိ progress state ကို သိမ်းထားတဲ့ file ဖြစ်ပါတယ်။

---

## 5.1 Inception Deliverables

```text
aidlc-docs/
└── inception/
    ├── requirements/
    │   ├── requirement-verification-questions.md
    │   └── requirements.md
    ├── user-stories/
    │   ├── personas.md
    │   └── stories.md
    ├── application-design/
    │   ├── components.md
    │   ├── component-methods.md
    │   ├── services.md
    │   └── component-dependency.md
    └── plans/
        ├── story-generation-plan.md
        └── application-design-plan.md
```

### Inception deliverables meaning

| File | Meaning |
|---|---|
| `requirement-verification-questions.md` | Requirement clarification questions |
| `requirements.md` | Requirements document |
| `personas.md` | User personas |
| `stories.md` | User stories using INVEST + Gherkin |
| `components.md` | Component definitions |
| `component-methods.md` | Method signatures |
| `services.md` | Service layer |
| `component-dependency.md` | Dependency matrix |
| `story-generation-plan.md` | Story generation plan |
| `application-design-plan.md` | Application design plan |

---

## 5.2 Construction Deliverables

```text
aidlc-docs/
└── construction/
    ├── document-upload/
    ├── functional-design/
    │   ├── domain-entities.md
    │   ├── business-rules.md
    │   └── business-logic-model.md
    ├── search/
    │   └── functional-design/
    │       └── ...
    └── indexing/
        └── functional-design/
            └── ...
```

### Construction deliverables meaning

| File / Folder | Meaning |
|---|---|
| `document-upload/` | Per-unit structure for document upload unit |
| `functional-design/domain-entities.md` | Domain entities using DDD |
| `functional-design/business-rules.md` | Business rules |
| `functional-design/business-logic-model.md` | Business logic model |
| `search/functional-design/` | Functional design for search unit |
| `indexing/functional-design/` | Functional design for indexing unit |

---

# 6. AI-DLC Rules: Structured Prompt Chains

AI-DLC သည် **structured prompt chains** ကိုအသုံးပြုပြီး step-by-step execute and verify လုပ်တဲ့ development flow ဖြစ်ပါတယ်။

ဆိုလိုတာက AI ကို prompt တစ်ခုတည်းနဲ့ code တန်းရေးခိုင်းတာမဟုတ်ပါဘူး။

AI-DLC မှာ—

```text
Step 1: Requirement analysis prompt
Step 2: User stories prompt
Step 3: Application design prompt
Step 4: Unit generation prompt
Step 5: Functional design prompt
Step 6: NFR prompt
Step 7: Infrastructure prompt
Step 8: Code generation prompt
Step 9: Build and test prompt
Step 10: Operations prompt
```

လိုမျိုး structured prompt chain နဲ့ တစ်ဆင့်ချင်းစီ လုပ်ဆောင်ပါတယ်။

---

## 6.1 INCEPTION Phase Rules

| Rules File | Role | Key Deliverables |
|---|---|---|
| `requirements-analysis.md` | Define system requirements | `requirements.md` |
| `user-stories.md` | Define features from user perspective | `personas.md`, `stories.md` |
| `application-design.md` | Design system structure | `components.md`, `services.md`, `component-dependency.md` |
| `units-generation.md` | Organize development units | `unit-of-work.md`, `unit-of-work-story-map.md` |

### Summary

Inception phase rules သည် project ကို နားလည်ပြီး design base တည်ဆောက်ရန်အတွက် အသုံးပြုပါတယ်။

```text
Requirement → User Story → Application Design → Unit Generation
```

---

## 6.2 CONSTRUCTION Phase Rules

| Rules File | Role | Key Deliverables |
|---|---|---|
| `functional-design.md` | Business logic modeling | `domain-entities.md`, `business-rules.md`, `business-logic-model.md` |
| `nfr-requirements.md` | Define non-functional requirements | `nfr-requirements.md`, `tech-stack-decisions.md` |
| `nfr-design.md` | Quality attribute design | `nfr-design-patterns.md`, `logical-components.md` |
| `infrastructure-design.md` | Infrastructure configuration design | `infrastructure-design.md`, `deployment-architecture.md` |
| `code-generation.md` | Code generation | Actual code, tests, deployment artifacts |
| `build-and-test.md` | Quality verification | `build-instructions.md`, `*-test-instructions.md` |

### Summary

Construction phase rules သည် approved design ကို actual software အဖြစ်ပြောင်းလဲဖို့ အသုံးပြုပါတယ်။

```text
Functional Design → NFR → Infrastructure → Code → Build/Test
```

---

## 6.3 OPERATIONS Phase Rules

| Rules File | Role | Key Deliverables |
|---|---|---|
| `operations.md` | Establish operations framework | To be updated |

### Summary

Operations phase rules သည် production deployment, monitoring, incident response, rollback plan စတဲ့ operations setup တွေအတွက် အသုံးပြုပါတယ်။

---

# 7. Mandatory and Conditional Stages

AI-DLC မှာ stage တိုင်းကို အမြဲလုပ်ရတာ မဟုတ်ပါဘူး။  
Project type, request complexity, existing codebase ရှိ/မရှိပေါ်မူတည်ပြီး stages တွေကို သင့်တော်သလိုရွေးလုပ်နိုင်ပါတယ်။

## Mandatory Stages

အမြဲလိုအပ်နိုင်တဲ့ stages—

```text
Requirements Analysis
Workflow Planning
Code Generation
Build and Test
```

## Conditional Stages

လိုအပ်မှလုပ်နိုင်တဲ့ stages—

```text
Reverse Engineering
User Stories
Application Design
Units Generation
Functional Design
NFR Requirements
NFR Design
Infrastructure Design
Operations
```

## Example: Small Bug Fix

Bug fix သေးသေးလေးဆိုရင်—

```text
Requirements Analysis
Code Generation
Build and Test
```

လောက်ပဲလိုနိုင်ပါတယ်။

## Example: New Application

New application တစ်ခုလုံးဆောက်မယ်ဆိုရင်—

```text
Requirements Analysis
User Stories
Application Design
Units Generation
Functional Design
NFR Requirements
NFR Design
Infrastructure Design
Code Generation
Build and Test
Operations
```

လိုမျိုး full flow လုပ်ရနိုင်ပါတယ်။

---

# 8. General Example: Online Shopping Website

AI-DLC Core Framework ကို Online Shopping Website နဲ့ ဥပမာကြည့်ပါ။

## Inception

AI က မေးနိုင်တာ—

```text
Product list ပါမလား?
Search feature ပါမလား?
Cart feature ပါမလား?
Payment ပါမလား?
Order history ပါမလား?
Admin dashboard ပါမလား?
```

AI ကထုတ်ပေးနိုင်တဲ့ deliverables—

```text
requirements.md
personas.md
stories.md
components.md
services.md
component-dependency.md
unit-of-work.md
```

## Construction

AI က design နဲ့ requirement အပေါ်မူတည်ပြီး—

```text
Product API
Cart API
Checkout logic
Order database model
Frontend components
Unit tests
Build instructions
```

တွေကို generate လုပ်ကူနိုင်ပါတယ်။

AI ကထုတ်ပေးနိုင်တဲ့ deliverables—

```text
domain-entities.md
business-rules.md
business-logic-model.md
nfr-requirements.md
tech-stack-decisions.md
infrastructure-design.md
actual code
tests
build-instructions.md
```

## Operations

Production deploy အတွက် AI က—

```text
Deployment checklist
Monitoring checklist
Rollback plan
Incident response checklist
```

တွေကို ကူညီပေးနိုင်ပါတယ်။

---

# 9. Easy Way to Remember

AI-DLC Core Framework ကို အလွယ်မှတ်ရင်—

```text
Ask → Plan → Design → Split → Build → Test → Operate
```

မြန်မာလို—

```text
မေးပါ
Plan ဆွဲပါ
Design လုပ်ပါ
Task ခွဲပါ
Code ရေးပါ
Test လုပ်ပါ
Run/Monitor လုပ်ပါ
```

ပိုပြီး အတိုချုပ်မှတ်ချင်ရင်—

```text
AI assists.
Human verifies.
Human decides.
Human approves.
```

---

# 10. Final Summary

**AI-DLC Core Framework** ဆိုတာ AI နဲ့ လူသား developer တွေ ပူးပေါင်းပြီး software development lifecycle တစ်ခုလုံးကို စနစ်တကျလုပ်ဆောင်တဲ့ framework ဖြစ်ပါတယ်။

အဓိကအချက် ၅ ခု—

```text
1. AI နဲ့ လူသား ပူးပေါင်းလုပ်ဆောင်တယ်။
2. AI က code တန်းမရေးဘဲ requirement ကို အရင်နားလည်တယ်။
3. Development ကို Inception → Construction → Operations ဆိုပြီး phase ၃ ခုနဲ့လုပ်တယ်။
4. Structured prompt chains နဲ့ deliverables တွေ step-by-step ထုတ်တယ်။
5. လူက အဆင့်တိုင်းမှာ review, verify, approve လုပ်ရတယ်။
```

အရေးကြီးဆုံး message—

```text
AI-DLC is not only about faster coding.
AI-DLC is about better collaboration, better design, better validation, and better operations.
```

မြန်မာလို—

> AI-DLC ဆိုတာ code မြန်မြန်ရေးဖို့တစ်ခုတည်းမဟုတ်ပါဘူး။  
> AI နဲ့ လူသားပူးပေါင်းပြီး design ပိုကောင်းအောင်၊ validation ပိုစနစ်ကျအောင်၊ operations ပိုတည်ငြိမ်အောင်လုပ်တဲ့ development framework ဖြစ်ပါတယ်။
