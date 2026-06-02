# AI-DLC Construction Phase Note

# 1. Construction Phase ဆိုတာဘာလဲ?

**Construction Phase** ဆိုတာ Inception Phase မှာ သတ်မှတ်ထားတဲ့ **development units** တွေကို actual working software အဖြစ် ပြောင်းလဲတဲ့အဆင့်ဖြစ်ပါတယ်။

Inception Phase မှာ—

```text
ဘာလုပ်မလဲ?
ဘယ် requirement တွေရှိလဲ?
ဘယ် user stories တွေရှိလဲ?
ဘယ် development units တွေခွဲမလဲ?
```

ဆိုတာတွေကို သတ်မှတ်ပြီးသားဖြစ်ပါတယ်။

Construction Phase မှာတော့ အဲဒီ units တွေကို—

```text
Design လုပ်မယ်
Code ရေးမယ်
Test လုပ်မယ်
Build လုပ်မယ်
Production-ready ဖြစ်အောင်ပြင်မယ်
```

ဆိုတဲ့အဆင့်တွေကို ဆက်လုပ်ပါတယ်။

အလွယ်ပြောရရင်—

```text
Construction = Plan ထဲက development units တွေကို tested, production-ready code အဖြစ်ပြောင်းတဲ့အဆင့်
```

---

# 2. Construction Phase ရဲ့ Main Goal

Construction Phase ရဲ့ main goal က—

```text
Transform development units into tested, production-ready code.
```

မြန်မာလို—

```text
Development units တွေကို test လုပ်ပြီး production မှာသုံးနိုင်တဲ့ code အဖြစ်ပြောင်းခြင်း
```

ဒီ phase မှာ **Domain-Driven Design (DDD)** principle ကို အသုံးပြုပါတယ်။  
ဆိုလိုတာက code တန်းမရေးဘဲ business domain ကို အရင် design လုပ်ပါတယ်။

ဥပမာ—

```text
Order ဆိုတာဘာလဲ?
Order မှာ ဘယ် attributes တွေရှိလဲ?
Order creation rule ဘာလဲ?
Payment failed ဖြစ်ရင် order status ဘာဖြစ်မလဲ?
```

ဒီလို business logic ကိုအရင်ရှင်းပြီးမှ code generation လုပ်ပါတယ်။

---

# 3. Construction Phase Stage Summary

Construction Phase မှာ အောက်ပါ stages တွေပါဝင်ပါတယ်။

| Order | Stage | Description | Execution Condition | Key Deliverables |
|---:|---|---|---|---|
| 1 | Functional Design | Technology-independent business logic design | Conditional, per unit | `domain-entities.md`, `business-rules.md` |
| 2 | NFR Requirements | Non-functional requirements and technology stack selection | Conditional, per unit | `nfr-requirements.md`, `tech-stack-decisions.md` |
| 3 | NFR Design | Define NFR patterns and logical components | Conditional, per unit | `nfr-design-patterns.md`, `logical-components.md` |
| 4 | Infrastructure Design | Map logical components to infrastructure | Conditional, per unit | `infrastructure-design.md`, `deployment-architecture.md` |
| 5 | Code Planning | Establish detailed code generation plan | Always | `code-generation-plan.md` |
| 6 | Code Generation | Generate actual code according to the plan | Always | `src/`, `tests/` code |
| 7 | Build and Test | Build and run comprehensive tests | Always | `build-instructions.md`, test results |

---

# 4. Per-Unit Design Process

Construction Phase မှာ development unit တစ်ခုချင်းစီကို complexity အပေါ်မူတည်ပြီး လိုအပ်တဲ့ design stages တွေဖြတ်သန်းစေပါတယ်။

ဥပမာ—

```text
Simple unit → design stages တချို့ skip လုပ်ပြီး code generation သွားနိုင်တယ်
Complex unit → Functional Design, NFR, Infrastructure Design အပြည့်လုပ်နိုင်တယ်
```

---

# 5. Stage 1: Functional Design

## Purpose

**Functional Design** ဆိုတာ business logic ကို technology နဲ့မချိတ်ဆက်ခင် design လုပ်တဲ့အဆင့်ပါ။

ဆိုလိုတာက—

```text
React သုံးမလား?
Spring Boot သုံးမလား?
Node.js သုံးမလား?
Database ဘာသုံးမလဲ?
```

ဆိုတာတွေမစဉ်းစားခင် business rule ကို အရင်စဉ်းစားပါတယ်။

## Activities

Functional Design မှာ လုပ်တဲ့အရာတွေ—

```text
Define domain entities
Define entity attributes
Define entity behaviors
Define invariants
Specify business rules
Model business logic
Describe interactions between entities
```

## Deliverables

```text
domain-entities.md
business-rules.md
business-logic-model.md
```

## When to Execute

```text
When new business logic is required
```

Business logic အသစ်လိုအပ်တဲ့အခါ Functional Design ကို run လုပ်ပါတယ်။

## Example: Order Management

Order Management unit တစ်ခုရှိတယ်ဆိုပါစို့။

### Domain Entities

```text
Order
OrderItem
Customer
Payment
```

### Business Rules

```text
Order must have at least one item.
Order total must be calculated from item prices.
Out-of-stock item cannot be ordered.
Payment failed ဖြစ်ရင် order status ကို payment_failed လုပ်ရမယ်။
```

### Business Logic

```text
Customer creates order
System validates stock
System calculates total
System processes payment
System updates order status
```

---

# 6. Stage 2: NFR Requirements

## Purpose

**NFR Requirements** ဆိုတာ Non-Functional Requirements တွေကို သတ်မှတ်တဲ့အဆင့်ဖြစ်ပါတယ်။

**NFR** ဆိုတာ feature မဟုတ်ပေမယ့် software quality အတွက် အရေးကြီးတဲ့ requirements တွေပါ။

ဥပမာ—

```text
Performance
Security
Scalability
Reliability
Compatibility
Resource limits
```

ဒီ stage မှာ technology stack ကိုလည်းရွေးချယ်ပြီး ဘာကြောင့်ရွေးတယ်ဆိုတဲ့ rationale ကို document လုပ်ပါတယ်။

## Activities

```text
Define performance requirements
Define security requirements
Define scalability requirements
Select technology stack
Document rationale
```

## Deliverables

```text
nfr-requirements.md
tech-stack-decisions.md
```

## When to Execute

```text
When a new technology stack selection is needed
or
When NFRs are critical
```

## Example

Online shopping system အတွက် NFR requirements—

```text
Performance:
- Product search response time should be under 1 second.
- Checkout API should respond under 2 seconds.

Security:
- Passwords must be hashed.
- Admin APIs must require authorization.
- Payment data must be protected.

Scalability:
- System should support many concurrent users.
- Database should handle growing order data.
```

Technology stack decision example—

```text
Backend: Spring Boot
Reason: Good for enterprise backend and REST APIs

Database: PostgreSQL
Reason: Reliable relational database for transactions

Cache: Redis
Reason: Improve product search and session performance
```

---

# 7. Stage 3: NFR Design

## Purpose

**NFR Design** ဆိုတာ NFR requirements တွေကို ဖြည့်ဆည်းဖို့ specific design patterns နဲ့ logical components တွေကို သတ်မှတ်တဲ့အဆင့်ပါ။

NFR Requirement က “ဘာလိုချင်လဲ” ကိုပြောတယ်။  
NFR Design က “ဘယ်လိုလုပ်မလဲ” ကိုပြောပါတယ်။

## Activities

```text
Select performance optimization patterns
Apply security patterns
Apply resilience patterns
Define logical components and responsibilities
```

## Common Patterns

### Performance Patterns

```text
Caching
Batching
Async processing
Pagination
Database indexing
```

### Security Patterns

```text
Authentication
Authorization
Encryption
Role-based access control
Input validation
```

### Resilience Patterns

```text
Retry
Circuit breaker
Fallback
Timeout
Graceful degradation
```

## Deliverables

```text
nfr-design-patterns.md
logical-components.md
```

## When to Execute

```text
When NFRs are complex
or
When specific pattern application is needed
```

## Example

Requirement:

```text
Product search must be fast.
```

NFR Design:

```text
Use database index on product name.
Use Redis cache for popular search keywords.
Use pagination for search results.
```

Requirement:

```text
System must be resilient when payment provider fails.
```

NFR Design:

```text
Use retry pattern.
Use timeout for external payment API.
Use fallback status: payment_pending.
```

---

# 8. Stage 4: Infrastructure Design

## Purpose

**Infrastructure Design** ဆိုတာ logical components တွေကို actual cloud services / infrastructure တွေနဲ့ map လုပ်တဲ့အဆင့်ဖြစ်ပါတယ်။

Application ကို production မှာ run ဖို့—

```text
Compute
Storage
Network
Database
Deployment strategy
Monitoring
Cost optimization
```

တွေကို design လုပ်ပါတယ်။

## Activities

```text
Select compute resources
Select storage services
Design networking
Establish deployment strategy
Estimate and optimize cost
```

## Example Cloud Resources

### Compute

```text
EC2
Lambda
ECS
Fargate
```

### Storage

```text
S3
RDS
DynamoDB
ElastiCache
```

### Networking

```text
VPC
Load Balancer
API Gateway
```

### Deployment Strategies

```text
Blue/Green Deployment
Canary Deployment
Rolling Deployment
```

## Deliverables

```text
infrastructure-design.md
deployment-architecture.md
```

## When to Execute

```text
When cloud deployment is required
```

## Example

Food delivery app infrastructure design—

```text
Frontend: S3 + CloudFront
Backend: ECS Fargate
Database: RDS PostgreSQL
Cache: ElastiCache Redis
API entry: Application Load Balancer
Deployment: Blue/Green deployment
Monitoring: CloudWatch
```

---

# 9. Code Generation and Verification

Construction Phase မှာ design ပြီးသွားရင် **Code Planning → Code Generation → Build and Test** ကို ဆက်လုပ်ပါတယ်။

ဒီ stages ၃ ခုက always run လုပ်ရတဲ့ core stages တွေဖြစ်ပါတယ်။

```text
Code Planning
Code Generation
Build and Test
```

---

# 10. Stage 5: Code Planning

## Purpose

**Code Planning** ဆိုတာ ဘာ files တွေ generate လုပ်မလဲ၊ ဘယ် order နဲ့ generate လုပ်မလဲဆိုတာ plan ဆွဲတဲ့အဆင့်ပါ။

Code တန်းမရေးခင် AI က code generation plan တစ်ခု အရင်ထုတ်ပါတယ်။

## Activities

```text
Create a list of files to generate
Determine dependency order between files
Define role and responsibility of each file
Map user stories to files
```

## Deliverable

```text
code-generation-plan.md
```

## Example

Order Management unit အတွက် code generation plan—

```text
1. Generate Order entity
2. Generate OrderItem entity
3. Generate OrderRepository
4. Generate OrderService
5. Generate OrderController
6. Generate OrderService unit tests
7. Generate Order API integration tests
```

---

# 11. Stage 6: Code Generation

## Purpose

**Code Generation** ဆိုတာ code-generation-plan.md အပေါ်မူတည်ပြီး actual code generate လုပ်တဲ့အဆင့်ပါ။

## Activities

```text
Execute each step of the plan in order
Convert domain models to code
Implement business rules as logic
Auto-generate test code
Track progress with checkboxes
```

## Output Locations

```text
Actual code: workspace root, src/, tests/
Code documentation: aidlc-docs/construction/
```

## Example

AI က generate လုပ်ပေးနိုင်တဲ့ files—

```text
src/domain/Order.ts
src/domain/OrderItem.ts
src/services/OrderService.ts
src/controllers/OrderController.ts
tests/OrderService.test.ts
tests/OrderController.test.ts
```

AI က code ရေးပေးနိုင်ပေမယ့် လူက review လုပ်ရပါမယ်။

စစ်ရမယ့်အရာ—

```text
Code compile ဖြစ်လား?
Business rule မှန်လား?
Security issue ရှိလား?
Naming convention ကိုက်လား?
Test cases လုံလောက်လား?
```

---

# 12. Stage 7: Build and Test

## Purpose

**Build and Test** ဆိုတာ generated code ကို build လုပ်ပြီး comprehensive tests run တဲ့အဆင့်ပါ။

ဒီအဆင့်က production-ready ဖြစ်/မဖြစ် စစ်တဲ့အတွက် အရေးကြီးပါတယ်။

## Activities

```text
Build all units and resolve dependencies
Run unit tests
Run integration tests
Run performance tests
Run security scans
Analyze test coverage
```

## Test Types

| Test Type | Meaning |
|---|---|
| Unit Test | Class/function တစ်ခုချင်းစီကို test လုပ်ခြင်း |
| Integration Test | Units တွေကြား interaction ကို test လုပ်ခြင်း |
| Performance Test | NFR compliance ကိုစစ်ခြင်း |
| Security Scan | Vulnerability checks လုပ်ခြင်း |
| Coverage Analysis | Test coverage ကိုစစ်ခြင်း |

## Deliverables

```text
build-instructions.md
test-instructions.md
test-results.md
```

## Example Commands

Node.js project—

```bash
npm install
npm run build
npm test
```

Java project—

```bash
mvn clean package
mvn test
```

Python project—

```bash
pip install -r requirements.txt
pytest
```

---

# 13. Easy Maintenance and Rapid Iteration

AI-DLC ရဲ့ အားသာချက်တစ်ခုက **change request တွေကို မြန်မြန်ဆန်ဆန် တုံ့ပြန်နိုင်ခြင်း** ဖြစ်ပါတယ်။

Testing လုပ်နေစဉ် issue တွေ့ရင် AI ကိုပြန်ခိုင်းပြီး update လုပ်နိုင်ပါတယ်။

---

## 13.1 Issues Found During Testing

Example issue—

```text
Error handling during login is insufficient.
```

AI-DLC flow—

```text
Request from AI
→ Add error handling
→ Test
→ Verify
```

မြန်မာလို—

```text
Login error handling မလုံလောက်တာတွေ့တယ်
AI ကို ပြင်ခိုင်းတယ်
Test ပြန်လုပ်တယ်
Verify လုပ်တယ်
```

---

## 13.2 New Requirements

Example new requirement—

```text
Password reset functionality is needed.
```

AI-DLC flow—

```text
Request from AI
→ Design
→ Code generation
→ Test
→ Verify
```

မြန်မာလို—

```text
Password reset feature အသစ်လိုတယ်
AI က design လုပ်ကူတယ်
Code generate လုပ်တယ်
Test လုပ်တယ်
Verify လုပ်တယ်
```

---

## 13.3 Performance Improvements

Example issue—

```text
Response time is slow.
```

AI-DLC flow—

```text
Request from AI
→ Root cause analysis
→ Optimization
→ Test
→ Verify
```

မြန်မာလို—

```text
Response time နှေးနေတယ်
AI က root cause analysis ကူလုပ်တယ်
Optimization လုပ်တယ်
Test ပြန်လုပ်တယ်
Verify လုပ်တယ်
```

---

# 14. Your Role in Construction Phase

AI က changes တွေကို မြန်မြန် implement လုပ်နိုင်ပေမယ့် လူက အောက်ပါအရာတွေကို မဖြစ်မနေစစ်ရပါမယ်။

```text
Review the changes
Confirm business requirements are met
Confirm quality standards are satisfied
Approve and decide on deployment
```

မြန်မာလို—

```text
Code changes တွေကို review လုပ်ပါ
Business requirements ပြည့်မပြည့် စစ်ပါ
Quality standards ကိုက်မကိုက် စစ်ပါ
Deploy လုပ်မလုပ် approve ပေးပါ
```

အရေးကြီးဆုံး principle—

```text
AI generates quickly.
Human verifies carefully.
```

---

# 15. Benefits of Rapid Iteration

AI-DLC Construction Phase မှာ rapid iteration လုပ်နိုင်ခြင်းကြောင့် အောက်ပါအကျိုးကျေးဇူးတွေ ရပါတယ်။

## 15.1 Time Reduction

```text
Changes reflected in hours to days
```

အပြောင်းအလဲတွေကို နာရီပိုင်းကနေ ရက်ပိုင်းအတွင်း ပြန်ထည့်နိုင်ပါတယ်။

## 15.2 Quality Maintenance

```text
Quality assured through testing and verification every time
```

အကြိမ်တိုင်း test နဲ့ verification လုပ်တဲ့အတွက် quality ကိုထိန်းနိုင်ပါတယ်။

## 15.3 Document Synchronization

```text
Related documents automatically updated when code changes
```

Code ပြောင်းတဲ့အခါ related documents တွေကိုလည်း update လုပ်နိုင်ပါတယ်။

## 15.4 Traceability

```text
All change history recorded in Git and documentation
```

Change history တွေကို Git နဲ့ documentation ထဲမှာ track လုပ်နိုင်ပါတယ်။

---

# 16. Key Deliverables

Construction Phase ရဲ့ key deliverables တွေကို category ၃ ခုခွဲနိုင်ပါတယ်။

```text
Design Documents
Code
Verification Results
```

---

## 16.1 Design Documents

```text
Domain models
Business rules
NFR requirements
Technology stack decisions
Design patterns
Infrastructure architecture
```

## 16.2 Code

```text
Application code: src/
Test code: tests/
Build scripts: package.json
```

## 16.3 Verification Results

```text
Build success confirmation
Test coverage reports
Performance benchmarks
```

---

# 17. Value of This Phase

Construction Phase ပြီးဆုံးတဲ့အခါ အောက်ပါ value တွေရရှိပါတယ်။

## 17.1 Working Software

```text
A functional application demonstrating core features
```

Core features တွေ အလုပ်လုပ်တဲ့ functional application တစ်ခုရလာပါတယ်။

## 17.2 Quality Codebase

```text
Well-tested, documented, and optimized code
```

Test လုပ်ထားပြီး documentation ပါတဲ့ optimized codebase ရလာပါတယ်။

## 17.3 CI/CD Pipeline

```text
Automated build, test, and deployment processes
```

Build, test, deployment process တွေကို automate လုပ်နိုင်ပါတယ်။

## 17.4 Development Expertise

```text
Hands-on experience with AI-assisted development
```

AI-assisted development ကို လက်တွေ့အသုံးချတဲ့ experience ရလာပါတယ်။

---

# 18. Moving to the Next Phase

Construction Phase ပြီးသွားရင် နောက် phase ဖြစ်တဲ့ **Operations Phase** ကို ဆက်သွားနိုင်ပါတယ်။

Construction Phase ရဲ့ output တွေက—

```text
Working application
Tested code
Build instructions
Test results
Deployment-ready artifacts
```

ဖြစ်တဲ့အတွက် Operations Phase မှာ application ကို deploy လုပ်ပြီး monitor/maintain လုပ်နိုင်ပါတယ်။

---

# 19. Simple Example: Online Shopping Website

Construction Phase ကို Online Shopping Website နဲ့ ဥပမာကြည့်ပါ။

## Development Unit: Order Management

### Functional Design

```text
Entities:
- Order
- OrderItem
- Customer
- Payment

Business Rules:
- Order must have at least one item.
- Payment must be completed before order is confirmed.
- Order total must be calculated correctly.
```

### NFR Requirements

```text
Performance:
- Order creation response time should be under 2 seconds.

Security:
- Only authenticated users can create orders.
- Payment information must be protected.

Scalability:
- System should handle many concurrent orders.
```

### NFR Design

```text
Use authentication middleware.
Use transaction for order creation.
Use retry logic for payment API.
Use database index for order lookup.
```

### Infrastructure Design

```text
Backend service runs on container service.
Database uses managed relational database.
Logs are sent to monitoring service.
```

### Code Planning

```text
Generate Order entity.
Generate OrderService.
Generate OrderController.
Generate OrderRepository.
Generate unit tests.
Generate integration tests.
```

### Code Generation

```text
src/entities/Order.ts
src/services/OrderService.ts
src/controllers/OrderController.ts
tests/OrderService.test.ts
```

### Build and Test

```bash
npm run build
npm test
```

---

# 20. Final Summary

**Construction Phase** ဆိုတာ AI-DLC ရဲ့ ဒုတိယအဆင့်ဖြစ်ပြီး Inception Phase မှာ သတ်မှတ်ထားတဲ့ development units တွေကို tested, production-ready code အဖြစ်ပြောင်းတဲ့ phase ဖြစ်ပါတယ်။

အဓိက stages တွေက—

```text
Functional Design
NFR Requirements
NFR Design
Infrastructure Design
Code Planning
Code Generation
Build and Test
```

အလွယ်မှတ်ရန်—

```text
Construction = Design → Code → Test
```

မြန်မာလို—

```text
Construction = Design လုပ်ခြင်း → Code ရေးခြင်း → Test လုပ်ခြင်း
```

အရေးကြီးဆုံး message—

```text
Do not only generate code.
Design the domain, define quality requirements, plan code generation, then build and test.
```

မြန်မာလို—

```text
Code တန်းမရေးပါနဲ့။
Domain ကို design လုပ်ပါ။
Quality requirements တွေသတ်မှတ်ပါ။
Code generation plan ဆွဲပါ။
ပြီးမှ build and test လုပ်ပါ။
```

Original Link => https://catalog.us-east-1.prod.workshops.aws/workshops/a1753e26-c705-4920-88f8-09ee62b203eb/en-US/01-introduction/13-construction
