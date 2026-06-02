# AI-DLC Inception Phase Note


# 1. Inception Phase ဆိုတာဘာလဲ?

**Inception Phase** ဆိုတာ AI-DLC ရဲ့ ပထမဆုံးအဆင့်ဖြစ်ပြီး **business objective တွေကို actionable development units တွေအဖြစ် ပြောင်းလဲတဲ့ phase** ဖြစ်ပါတယ်။

ဒီအဆင့်မှာ Product Owner, Developer နဲ့ AI တို့ပူးပေါင်းပြီး requirement တွေကို ရှင်းလင်းအောင်လုပ်ပါတယ်။  
ဒီ approach ကို **Mob Elaboration** လို့ခေါ်နိုင်ပါတယ်။

အလွယ်ပြောရရင်—

```text
Inception = Business idea ကို clear requirements + development plan အဖြစ်ပြောင်းတဲ့အဆင့်
```

---

# 2. Inception Phase ရဲ့ အဓိကရည်ရွယ်ချက်

Inception Phase ရဲ့ main goal က **code မရေးခင် project ကိုသေချာနားလည်အောင်လုပ်ခြင်း** ဖြစ်ပါတယ်။

ဒီ phase မှာ AI က—

```text
Project type ကိုစစ်တယ်
Requirement တွေမေးတယ်
Existing codebase ရှိရင် analyze လုပ်တယ်
User stories ထုတ်တယ်
Application design စဉ်းစားတယ်
Development units တွေခွဲတယ်
Execution plan ဆွဲတယ်
```

လူကတော့—

```text
AI မေးတဲ့မေးခွန်းတွေကို ဖြေတယ်
Requirement ကို confirm လုပ်တယ်
Plan ကို review လုပ်တယ်
Scope ကို approve လုပ်တယ်
```

---

# 3. Inception Phase Stage Summary

| Stage | Execution Condition | Key Artifacts |
|---|---|---|
| Workspace Detection | Always | `aidlc-state.md` |
| Requirements Analysis | Always | `requirements.md` |
| Workflow Planning | Always | `execution-plan.md` |
| Reverse Engineering | Existing projects only | `architecture.md`, `component-inventory.md` |
| User Stories | User-facing features | `personas.md`, `stories.md` |
| Application Design | When new components are needed | `components.md`, `services.md` |
| Units Generation | Complex projects | `unit-of-work.md` |

---

# 4. Always-Executed Stages

Always-executed stages ဆိုတာ Inception Phase မှာ အမြဲလုပ်ရတဲ့ stages တွေဖြစ်ပါတယ်။

```text
Workspace Detection
Requirements Analysis
Workflow Planning
```

---

## 4.1 Workspace Detection

**Workspace Detection** ဆိုတာ AI က project workspace ကို analyze လုပ်တဲ့အဆင့်ပါ။

AI က စစ်တဲ့အရာတွေ—

```text
Project type: New project or existing project?
Existing file structure
Technology stack in use
Git status
```

အဓိကအနေနဲ့ AI က project ကို **Greenfield** လား **Brownfield** လား ခွဲခြားပါတယ်။

| Type | Meaning |
|---|---|
| Greenfield | Project အသစ်၊ existing codebase မရှိသေး |
| Brownfield | Existing project ရှိပြီးသား |

### Artifact

```text
aidlc-docs/aidlc-state.md
```

ဒီ file က project state ကို track လုပ်ဖို့ အသုံးပြုပါတယ်။

---

## 4.2 Requirements Analysis

**Requirements Analysis** ဆိုတာ requirement တွေကို collect လုပ်ပြီး validate လုပ်တဲ့အဆင့်ပါ။

AI က user request ကို analyze လုပ်ပြီး မရှင်းတဲ့အချက်တွေကို မေးခွန်းမေးပါတယ်။

AI စစ်တဲ့အချက်များ—

```text
Request clarity: clear / ambiguous / incomplete
Request type: new feature / bug fix / refactoring
Initial scope estimation: single file / component / entire system
Initial complexity estimation: simple / moderate / complex
```

ဒီ stage မှာ AI က **requirement-verification-questions.md** file ကို generate လုပ်ပြီး user ကိုဖြေခိုင်းပါတယ်။

### Example Questions

```text
Q1: Who are the primary users, and in what context will they use this?
A) General users
B) Administrators
C) External systems
D) All types
E) Other

[Answer]:

Q2: What is the core value of the system?
[Answer]:

Q3: What are the non-functional requirements?
- Performance: [Answer]:
- Security: [Answer]:
- Compatibility: [Answer]:
```

### Your Role

User / Developer က `[Answer]:` နေရာတွေကို ဖြည့်ရပါတယ်။  
AI က အဲဒီ answers တွေကို analyze လုပ်ပြီး မရှင်းတဲ့နေရာတွေရှိရင် follow-up questions ဆက်မေးပါတယ်။

### Artifacts

```text
inception/requirements/requirement-verification-questions.md
inception/requirements/requirements.md
```

---

## 4.3 Workflow Planning

**Workflow Planning** ဆိုတာ project ကို ဆက်လုပ်ဖို့ execution plan ဆွဲတဲ့အဆင့်ပါ။

AI က project complexity နဲ့ requirement အပေါ်မူတည်ပြီး ဘယ် stages တွေ run မလဲ၊ ဘယ် stages တွေ skip မလဲ ဆုံးဖြတ်ကူညီပါတယ်။

### Example Execution Plan

```text
🔵 INCEPTION Phase:
✅ Workspace Detection (Complete)
✅ Requirements Analysis (Complete)
✅ User Stories (Scheduled)
⏭️ Application Design (Skip - Simple structure)
✅ Units Generation (Scheduled)

🟢 CONSTRUCTION Phase:
✅ Functional Design (Per unit)
✅ NFR Requirements (Per unit)
⏭️ NFR Design (Skip - Simple NFR)
⏭️ Infrastructure Design (Skip - Client only)
✅ Code Generation (Always)
✅ Build and Test (Always)

Estimated time: Approximately 3 hours
```

### Artifact

```text
inception/plans/execution-plan.md
```

---

# 5. Conditionally-Executed Stages

Conditionally-executed stages ဆိုတာ project အခြေအနေအပေါ်မူတည်ပြီး လိုအပ်မှ run တဲ့ stages တွေဖြစ်ပါတယ်။

```text
Reverse Engineering
User Stories
Application Design
Units Generation
```

---

## 5.1 Reverse Engineering

**Reverse Engineering** ဆိုတာ existing project ရှိပြီးသားဆိုရင် codebase ကို analyze လုပ်တဲ့အဆင့်ပါ။

ဒီ stage ကို **existing projects only** အတွက် run လုပ်ပါတယ်။  
New project ဖြစ်ရင် skip လုပ်နိုင်ပါတယ်။

AI analyze လုပ်တဲ့အရာတွေ—

```text
Architecture structure
Component inventory
Technology stack
Dependencies
```

### Artifacts

```text
inception/reverse-engineering/architecture.md
inception/reverse-engineering/component-inventory.md
inception/reverse-engineering/technology-stack.md
```

### Example

Existing food delivery app ထဲမှာ order tracking feature ထည့်ချင်တယ်ဆိုပါစို့။

AI က အရင်စစ်မယ်—

```text
Order module ရှိပြီးသားလား?
Delivery module ရှိလား?
Rider component ရှိလား?
Notification service ရှိလား?
Database schema ဘယ်လိုရှိလဲ?
```

ဒီလိုစစ်ပြီးမှ feature အသစ်ကို ဘယ်နေရာမှာထည့်ရမလဲ ဆုံးဖြတ်နိုင်ပါတယ်။

---

## 5.2 User Stories

**User Stories** ဆိုတာ requirement တွေကို user perspective ကနေ story အဖြစ်ပြောင်းတဲ့အဆင့်ပါ။

ဒီ stage ကို user-facing features, multiple user types, complex business logic, cross-team collaboration လိုအပ်တဲ့ project တွေမှာ run လုပ်ပါတယ်။

### Execution Conditions

```text
Features directly used by users
Multiple user types exist
Complex business logic
Cross-team collaboration is needed
```

### INVEST Principles

User stories ကောင်းတစ်ခုဟာ INVEST principle နဲ့ကိုက်သင့်ပါတယ်။

| Letter | Meaning |
|---|---|
| I | Independent |
| N | Negotiable |
| V | Valuable |
| E | Estimable |
| S | Small |
| T | Testable |

### Example User Story

```text
As a player,
I can press the spacebar to make my character jump.
```

### Example Acceptance Criteria

```text
Character moves upward on spacebar input
Jump height is consistent
Input delay < 16ms
```

### Artifacts

```text
inception/user-stories/stories.md
inception/user-stories/personas.md
```

---

## 5.3 Application Design

**Application Design** ဆိုတာ high-level components နဲ့ service layers တွေကို design လုပ်တဲ့အဆင့်ပါ။

ဒီ stage ကို new components တွေလိုအပ်တဲ့အခါ run လုပ်ပါတယ်။

### Activities

```text
Identify major system components
Define responsibilities and roles for each component
Design interfaces between components
Define service layer structure
Map dependency relationships
```

### Artifacts

```text
inception/application-design/components.md
inception/application-design/component-methods.md
inception/application-design/services.md
inception/application-design/component-dependency.md
```

### Example

Online shopping website မှာ component တွေကို ဒီလိုခွဲနိုင်ပါတယ်။

```text
Auth Component
Product Component
Cart Component
Order Component
Payment Component
Admin Component
```

Service layer တွေက—

```text
AuthService
ProductService
CartService
OrderService
PaymentService
```

---

## 5.4 Units Generation

**Units Generation** ဆိုတာ system ကို manageable development units တွေအဖြစ် ခွဲတဲ့အဆင့်ပါ။

ဒီ stage ကို complex projects တွေမှာ run လုပ်ပါတယ်။

### Development Unit ဆိုတာဘာလဲ?

**Development Unit** ဆိုတာ independent develop လုပ်နိုင်တဲ့ work unit ဖြစ်ပါတယ်။

ဥပမာ—

```text
Microservices: Each unit is an independently deployable service
Monolith: Logical modules within a single application
```

### Example: Table Order Unit Decomposition

```text
Unit 1: Order Management
- Assigned stories: Create order, View order
- Dependencies: None
- Priority: High

Unit 2: Menu Management
- Assigned stories: View menu, Search menu
- Dependencies: None
- Priority: High

Unit 3: Payment Processing
- Assigned stories: Payment calculation, Receipt generation
- Dependencies: Order Management
- Priority: Medium
```

### Artifacts

```text
inception/application-design/unit-of-work.md
inception/application-design/unit-of-work-dependency.md
inception/application-design/unit-of-work-story-map.md
```

---

# 6. Inception Phase Process Flow

Inception Phase ကို step-by-step ကြည့်ရင်—

```text
1. Workspace Detection
   ↓
2. Reverse Engineering
   ↓
3. Requirements Analysis
   ↓
4. User Stories
   ↓
5. Workflow Planning
   ↓
6. Application Design
   ↓
7. Units Generation
```

Project အမျိုးအစားအပေါ်မူတည်ပြီး Reverse Engineering, User Stories, Application Design, Units Generation တို့ကို skip လုပ်နိုင်ပါတယ်။

---

# 7. Value of This Phase

Inception Phase ကိုသေချာပြီးမြောက်အောင်လုပ်ရင် အောက်ပါ value တွေရနိုင်ပါတယ်။

## 7.1 Clear Project Vision

Business objectives တွေကို actionable development units တွေအဖြစ် ပြောင်းနိုင်ပါတယ်။

```text
ဘာလုပ်မလဲ?
ဘာကြောင့်လုပ်မလဲ?
ဘယ်သူအတွက်လုပ်မလဲ?
```

ဆိုတာတွေ ပိုရှင်းလာပါတယ်။

## 7.2 Comprehensive Requirements

Stakeholder consensus ပါတဲ့ detailed requirements documentation ရပါတယ်။

```text
Functional requirements
Non-functional requirements
Constraints
Assumptions
Success criteria
```

တွေကို document လုပ်နိုင်ပါတယ်။

## 7.3 Prioritized Backlog

User stories တွေကို map လုပ်ပြီး priority ချနိုင်ပါတယ်။

```text
High priority
Medium priority
Low priority
```

အနေနဲ့ development order သတ်မှတ်နိုင်ပါတယ်။

## 7.4 Technical Foundation

Architectural decisions နဲ့ design patterns တွေကို အစောပိုင်းမှာ သတ်မှတ်နိုင်ပါတယ်။

```text
Component structure
Service layer
Dependency relationships
Technology stack
```

တွေကို စနစ်တကျတည်ဆောက်နိုင်ပါတယ်။

## 7.5 Success Metrics

Success criteria နဲ့ measurement framework တွေ သတ်မှတ်နိုင်ပါတယ်။

ဥပမာ—

```text
Feature works as expected
Performance meets target
Security requirements are satisfied
User acceptance criteria pass
```

## 7.6 Risk Assessment

Technical risks တွေကို ကြိုတင်သတ်မှတ်ပြီး mitigation strategy ထားနိုင်ပါတယ်။

```text
Integration risk
Performance risk
Security risk
Dependency risk
Timeline risk
```

---

# 8. Moving to the Next Step

Inception Phase ပြီးဆုံးတဲ့အခါ Construction Phase ကိုသွားဖို့ အောက်ပါအရာတွေ ready ဖြစ်လာပါတယ်။

```text
Validated requirements and user stories
Established technical architecture
Clear success criteria and acceptance tests
Risk assessment and mitigation strategies
Development roadmap and work plan
```

ဒါတွေပြင်ဆင်ပြီးသွားရင် actual code စတင်ရေးတဲ့ **Construction Phase** ကို ဆက်သွားနိုင်ပါတယ်။

---

# 9. Simple Example: Restaurant Table Order System

Inception Phase ကို Restaurant Table Order System နဲ့ ဥပမာကြည့်ပါ။

## User Request

```text
Build a table ordering system for a restaurant.
```

## Workspace Detection

AI က စစ်မယ်—

```text
Project အသစ်လား?
Existing project ရှိပြီးသားလား?
Frontend/backend ရှိပြီးသားလား?
Database ရှိပြီးသားလား?
```

## Requirements Analysis

AI က မေးမယ်—

```text
Customer က QR code နဲ့ order တင်မလား?
Waiter account လိုမလား?
Kitchen dashboard ပါမလား?
Payment system ပါမလား?
Menu search ပါမလား?
Order status tracking ပါမလား?
```

## User Stories

```text
As a customer,
I want to scan a QR code and view the menu,
so that I can order food from my table.
```

```text
As a kitchen staff,
I want to see incoming orders,
so that I can prepare food in order.
```

## Application Design

```text
Menu Component
Order Component
Payment Component
Kitchen Dashboard Component
Admin Component
```

## Units Generation

```text
Unit 1: Menu Management
Unit 2: Order Management
Unit 3: Payment Processing
Unit 4: Kitchen Dashboard
Unit 5: Admin Management
```

---

# 10. Final Summary

**Inception Phase** ဆိုတာ AI-DLC ရဲ့ ပထမဆုံး phase ဖြစ်ပြီး business objectives တွေကို clear requirements, user stories, architecture, development units တွေအဖြစ် ပြောင်းလဲတဲ့အဆင့်ဖြစ်ပါတယ်။

အဓိက stages တွေက—

```text
Workspace Detection
Requirements Analysis
Workflow Planning
Reverse Engineering
User Stories
Application Design
Units Generation
```

အရေးကြီးဆုံးမှတ်ရန်—

```text
Inception does not build code yet.
Inception prepares the project so Construction can build the right code.
```

မြန်မာလို—

```text
Inception က code မရေးသေးပါ။
Construction phase မှာ မှန်ကန်တဲ့ code ရေးနိုင်ဖို့ project ကို အရင်ပြင်ဆင်တဲ့အဆင့်ပါ။
```

Original Link => https://catalog.us-east-1.prod.workshops.aws/workshops/a1753e26-c705-4920-88f8-09ee62b203eb/en-US/01-introduction/12-inception#always-executed-stages
