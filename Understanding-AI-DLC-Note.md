# AI-DLC Note  
## AI-Driven Development Lifecycle

## 1. AI-DLC ဆိုတာဘာလဲ?

**AI-DLC** ဆိုတာ **AI-Driven Development Lifecycle** ကို ဆိုလိုပါတယ်။  
Software တစ်ခုတည်ဆောက်တဲ့အခါ AI ကို assistant တစ်ယောက်လို အသုံးပြုပြီး requirement စဉ်းစားခြင်း၊ design ဆွဲခြင်း၊ code ရေးခြင်း၊ test လုပ်ခြင်း၊ deployment လုပ်ခြင်းတွေမှာ ကူညီခိုင်းတဲ့ development approach ဖြစ်ပါတယ်။

အဓိက idea က—

```text
AI asks questions, designs, and writes code.
You review, decide, and approve.
```

မြန်မာလိုဆိုရင်—

```text
AI က မေးခွန်းတွေ မေးပေးတယ်။
AI က design အကြံပြုပေးတယ်။
AI က code ရေးကူပေးတယ်။
လူက review လုပ်တယ်။
လူက ဆုံးဖြတ်တယ်။
လူက approve လုပ်တယ်။
```

AI-DLC မှာ AI က အရာအားလုံးကို အလိုအလျောက်ဆုံးဖြတ်တာ မဟုတ်ပါဘူး။  
AI က ကူညီပေးသူဖြစ်ပြီး လူက final decision maker ဖြစ်ပါတယ်။

---

## 2. Root Cause ①: Coding Speed ≠ Development Speed

![Root Cause 1: Coding Speed is not Development Speed](https://static.us-east-1.prod.workshops.aws/public/23768ace-c53e-436b-af8e-bdcda7ccf7be/static/images/aidlc/01-01-en.png)

ဒီပုံရဲ့ အဓိကအဓိပ္ပါယ်က—

> **Code ရေးတာ မြန်လာတာနဲ့ project တစ်ခုလုံး မြန်လာတာ မတူပါဘူး။**

Software development မှာ coding က အရေးကြီးပေမယ့် coding တစ်ခုပဲ မဟုတ်ပါဘူး။  
Design, analysis, testing, validation, communication, coordination စတဲ့အပိုင်းတွေလည်း ပါဝင်ပါတယ်။

ပုံထဲမှာ software development work ကို ဒီလိုခွဲပြထားပါတယ်။

| Area | Percentage | Meaning |
|---|---:|---|
| Coding | 20% | Code ရေးတဲ့အပိုင်း |
| Design / Analysis | 30% | Requirement စဉ်းစားခြင်း၊ system design ဆွဲခြင်း |
| Test / Validation | 30% | Test လုပ်ခြင်း၊ quality စစ်ခြင်း |
| Communication / Coordination | 20% | Team နဲ့ညှိနှိုင်းခြင်း၊ communication လုပ်ခြင်း |

AI coding tools တွေက coding ကို 50% ပိုမြန်စေတယ်ဆိုရင်တောင် overall productivity က 10% လောက်ပဲ တိုးနိုင်ပါတယ်။  
ဘာလို့လဲဆိုတော့ coding က software development တစ်ခုလုံးရဲ့ 20% လောက်ပဲ ပါဝင်လို့ပါ။

---

## 3. နားလည်လွယ်တဲ့ ဥပမာ

### Example: Online Shopping Website

Online shopping website တစ်ခုလုပ်မယ်ဆိုပါစို့။

AI က code ရေးတာကို မြန်စေနိုင်ပါတယ်။ ဥပမာ—

```text
Create product API.
Create cart API.
Create login page.
Create checkout page.
Create database schema.
```

ဒါပေမယ့် project တစ်ခုမှာ code ရေးတာပဲ မဟုတ်ပါဘူး။

Project မစခင် စဉ်းစားရမယ်—

```text
Customer က ဘာလုပ်နိုင်ရမလဲ?
Product search ပါမလား?
Cart feature ဘယ်လိုလုပ်မလဲ?
Payment ပါမလား?
Admin dashboard ပါမလား?
Order history ပါမလား?
```

Code ရေးပြီးရင် test လုပ်ရမယ်—

```text
Price calculation မှန်လား?
Stock quantity မှန်လား?
Payment fail ဖြစ်ရင် ဘာလုပ်မလဲ?
User တစ်ယောက်ရဲ့ cart ကို တခြား user မမြင်ရဘူးလား?
```

Team နဲ့လည်း ညှိရမယ်—

```text
Frontend developer က API ကို ဘယ်လိုသုံးမလဲ?
Backend API ready ဖြစ်ပြီလား?
Designer ရဲ့ UI နဲ့ ကိုက်လား?
Client requirement ပြောင်းသွားလား?
```

ဒါကြောင့် **AI က code ရေးတာကို မြန်စေပေမယ့် software development တစ်ခုလုံးကို မြန်စေဖို့ coding တစ်ခုတည်းနဲ့ မလုံလောက်ပါဘူး**။

---

## 4. AI-DLC ရဲ့ Major Phases ၃ ခု

AI-DLC မှာ အဓိက phase ၃ ခုရှိပါတယ်။

```text
1. Inception
2. Construction
3. Operations
```

---

## 5. Phase 1: Inception  
### Requirements Analysis and Design

**Inception** ဆိုတာ software မဆောက်ခင် plan ဆွဲတဲ့အဆင့်ပါ။  
ဒီအဆင့်မှာ “ဘာလုပ်မလဲ?”, “ဘာ feature တွေပါမလဲ?”, “ဘယ်လို design လုပ်မလဲ?” ဆိုတာတွေကို စဉ်းစားပါတယ်။

### AI က ဘာကူညီနိုင်လဲ?

AI က—

```text
Requirement မရှင်းလင်းတာတွေကို မေးခွန်းမေးပေးနိုင်တယ်။
User stories ရေးပေးနိုင်တယ်။
Feature list ထုတ်ပေးနိုင်တယ်။
System design idea ပေးနိုင်တယ်။
Database design draft လုပ်ပေးနိုင်တယ်။
API design အကြံပြုပေးနိုင်တယ်။
```

### General Example

Food Delivery App တစ်ခုလုပ်မယ်ဆိုရင် AI က ဒီလိုမေးနိုင်ပါတယ်။

```text
Customer account လိုမလား?
Restaurant account လိုမလား?
Delivery rider account လိုမလား?
Payment system ပါမလား?
Order tracking ပါမလား?
Review and rating ပါမလား?
```

AI က design idea ပေးနိုင်ပါတယ်။

```text
Customer can browse restaurants.
Customer can add food to cart.
Customer can place an order.
Restaurant can accept or reject orders.
Rider can update delivery status.
Admin can manage users and restaurants.
```

ဒါပေမယ့် လူက final ဆုံးဖြတ်ရပါမယ်။

```text
Version 1 မှာ ဘာ feature ထည့်မလဲ?
Version 2 မှာ ဘာ feature ထည့်မလဲ?
Budget နဲ့ timeline ကိုက်လား?
Business requirement နဲ့ ကိုက်လား?
```

### Simple Meaning

> **Inception = Software မဆောက်ခင် စဉ်းစားပြီး plan ဆွဲတဲ့အဆင့်**

---

## 6. Phase 2: Construction  
### Code Generation and Implementation

**Construction** ဆိုတာ actual code ရေးပြီး software ကို တည်ဆောက်တဲ့အဆင့်ပါ။

### AI က ဘာကူညီနိုင်လဲ?

AI က—

```text
Code generate လုပ်ပေးနိုင်တယ်။
API controller ရေးပေးနိုင်တယ်။
Database model ရေးပေးနိုင်တယ်။
Frontend UI code ရေးကူနိုင်တယ်။
Unit test ရေးပေးနိုင်တယ်။
Bug fix အကြံပြုပေးနိုင်တယ်။
Documentation ရေးပေးနိုင်တယ်။
```

### General Example

Online shopping website အတွက် AI ကို ဒီလိုခိုင်းနိုင်ပါတယ်။

```text
Create a product listing API.
Create a cart API.
Create a checkout page.
Create an order database table.
Write unit tests for order creation.
```

AI က code ရေးပေးနိုင်ပါတယ်။  
ဒါပေမယ့် လူက ပြန်စစ်ရပါမယ်။

```text
Code run လို့ရလား?
Bug ရှိလား?
Security issue ရှိလား?
Logic မှန်လား?
Performance ကောင်းလား?
```

ဥပမာ payment calculation ကို AI ရေးပေးတယ်ဆိုရင် လူက သေချာစစ်ရပါမယ်။

```text
Discount calculation မှန်လား?
Tax calculation မှန်လား?
Total price မှန်လား?
Payment failed ဖြစ်ရင် order status ဘယ်လိုဖြစ်မလဲ?
```

### Simple Meaning

> **Construction = AI က code ရေးကူတယ်၊ လူက စစ်ပြီး ပြင်တဲ့အဆင့်**

---

## 7. Phase 3: Operations  
### Deployment and Monitoring

**Operations** ဆိုတာ software ကို user တွေသုံးနိုင်အောင် online ပေါ်တင်ပြီး စောင့်ကြည့်တဲ့အဆင့်ပါ။

### AI က ဘာကူညီနိုင်လဲ?

AI က—

```text
Dockerfile ရေးပေးနိုင်တယ်။
Deployment steps ရေးပေးနိုင်တယ်။
CI/CD pipeline draft လုပ်ပေးနိုင်တယ်။
Monitoring checklist ပေးနိုင်တယ်။
Error logs တွေကို ရှင်းပြပေးနိုင်တယ်။
Rollback plan အကြံပြုပေးနိုင်တယ်။
```

### General Example

Food delivery app ကို deploy လုပ်ပြီးနောက် လူက စောင့်ကြည့်ရမယ်။

```text
Server down ဖြစ်နေလား?
Order API slow ဖြစ်နေလား?
Payment error ဖြစ်နေလား?
User login fail ဖြစ်နေလား?
Database full ဖြစ်နေလား?
```

Error တက်လာရင် AI ကို log ပြပြီး မေးနိုင်ပါတယ်။

```text
Why is this order API failing?
Suggest possible causes and fixes.
```

AI က possible reasons တွေ ပြောပေးနိုင်ပါတယ်။  
ဒါပေမယ့် production မှာ ဘာပြင်မလဲ၊ rollback လုပ်မလဲဆိုတာကို လူကဆုံးဖြတ်ရပါမယ်။

### Simple Meaning

> **Operations = Software ကို online တင်ပြီး error ရှိ/မရှိ စောင့်ကြည့်တဲ့အဆင့်**

---

## 8. AI-DLC Workflow Summary

AI-DLC ကို flow အနေနဲ့ ကြည့်ရင်—

```text
Inception
↓
Requirements + Design
↓
Construction
↓
Code + Test + Implementation
↓
Operations
↓
Deploy + Monitor + Improve
```

အလွယ်မှတ်ရင်—

```text
Think with AI
Build with AI
Run with AI
```

---

## 9. Traditional SDLC vs AI-DLC

| Topic | Traditional SDLC | AI-DLC |
|---|---|---|
| Requirement Analysis | လူက manually လုပ် | AI က question မေးပြီး assist လုပ် |
| Design | Developer/Architect ဆွဲ | AI က design draft အကြံပြု |
| Coding | Developer ရေး | AI generate + Developer review |
| Testing | QA/Developer ရေး | AI က test case generate ကူညီ |
| Deployment | DevOps setup လုပ် | AI က deployment config draft ကူညီ |
| Decision | Human | Human |
| Approval | Human | Human |

အဓိကကွာခြားချက်က—

> **AI-DLC မှာ AI က lifecycle တစ်လျှောက်လုံးမှာ active assistant အဖြစ် ပါဝင်လာတာပါ။**

---

## 10. Human Role in AI-DLC

AI-DLC မှာ AI က ကူညီပေးသူဖြစ်ပြီး လူက decision maker ဖြစ်ပါတယ်။

လူက လုပ်ရမယ့်အရာတွေ—

```text
Requirement ကို confirm လုပ်ရမယ်။
AI output ကို review လုပ်ရမယ်။
Code quality စစ်ရမယ်။
Security risk စစ်ရမယ်။
Test result စစ်ရမယ်။
Final approval ပေးရမယ်။
Production decision ချရမယ်။
```

AI ကို blindly မယုံသင့်ပါဘူး။  
AI က မှားနိုင်ပါတယ်။

AI က—

```text
မရှိတဲ့ library/function ကို သုံးနိုင်တယ်။
Requirement ကို နားလည်မှုလွဲနိုင်တယ်။
Security issue ပါတဲ့ code ရေးနိုင်တယ်။
Business context ကို မသိနိုင်ဘူး။
```

ဒါကြောင့် AI-DLC ရဲ့ principle က—

```text
AI generates.
Human validates.
```

---

## 11. AI-DLC ရဲ့ အကျိုးကျေးဇူးများ

AI-DLC သုံးရင်—

```text
Development speed မြန်လာနိုင်တယ်။
Requirement analysis ပိုစနစ်ကျလာနိုင်တယ်။
Boilerplate code ရေးရတာ လျော့နိုင်တယ်။
Testing idea တွေ ပိုရနိုင်တယ်။
Documentation ရေးရတာ လွယ်နိုင်တယ်။
Developer productivity တိုးနိုင်တယ်။
Design decision တွေကို ပိုစနစ်တကျ စဉ်းစားနိုင်တယ်။
```

---

## 12. AI-DLC မှာ သတိထားရမယ့်အချက်များ

AI-DLC သုံးတဲ့အခါ—

```text
AI output ကို တန်းမသုံးသင့်ပါ။
Code ကို test မလုပ်ဘဲ merge မလုပ်သင့်ပါ။
Secret key/API key တွေ AI prompt ထဲ မထည့်သင့်ပါ။
Sensitive data တွေ မပေးသင့်ပါ။
Security review မလုပ်ဘဲ deploy မလုပ်သင့်ပါ။
AI ရေးပေးတဲ့ architecture ကို human developer/architect က review လုပ်သင့်ပါတယ်။
```

---

## 13. Final Summary

AI-DLC ဆိုတာ—

> **AI ကို software development lifecycle တစ်လျှောက်မှာ assistant အဖြစ်အသုံးပြုပြီး requirements analysis, design, code generation, testing, deployment, monitoring တွေကို ပိုမြန်ပြီး စနစ်တကျလုပ်နိုင်အောင် ကူညီတဲ့ development methodology ဖြစ်ပါတယ်။**

အဓိက phase ၃ ခုက—

```text
Inception    = ဘာဆောက်မလဲ စဉ်းစားခြင်း
Construction = Code ရေးပြီး ဆောက်ခြင်း
Operations   = Online တင်ပြီး စောင့်ကြည့်ခြင်း
```

အရေးကြီးဆုံး မှတ်ရန်—

```text
Coding Speed ≠ Development Speed
```

Code ရေးတာမြန်လာတာနဲ့ project တစ်ခုလုံးမြန်လာတာ မတူပါဘူး။  
Development တစ်ခုလုံးမြန်ဖို့ AI ကို coding တစ်ခုတည်းမှာမဟုတ်ဘဲ design, analysis, testing, validation, deployment, monitoring အဆင့်တိုင်းမှာ အသုံးချသင့်ပါတယ်။

နောက်ဆုံးမှတ်ရန်—

```text
AI helps.
Human checks.
Human decides.
Human approves.
```
