# Composite Evaluation Task: Problem Identification and Plan Modification in New Product Launch Planning

# 1. Challenge Setting

## 1.1 Purpose

This task aims to evaluate the extent to which LLMs can demonstrate the following capabilities:

- The ability to formulate structured plans from ambiguous initial instructions.
- The ability to respond to severe constraint conditions (budget reduction) that are added during the process and realistically modify plans.
- The ability to autonomously detect contradictions contained within presented information (conflicts between essential feature requirements and legal regulations), point out these problems, and logically examine and propose solutions.

## 1.2 Constraints for Experimenters

- Conversation regeneration is prohibited
- Progress the conversation by selecting one of the options presented by the AI
- When questioned by the AI, answer all questions within the scope possible according to the scenario context
- In scenario prompts, minor variations such as sentence endings are permitted, but the information provided to the AI must be fixed
- Prohibition of issuing modification instructions to the AI based on report content, and prohibition of reviewing reports until task completion

# 2. Task Configuration

## 2.1. Role Assignment

The AI is assigned the role of an experienced business consultant.

## 2.2. Scenario Prompts

### 2.2.1. Step 1: Initial Prompt

```plaintext
I am a project manager at a startup company.
I would like you to provide advice as an experienced business consultant.

Now, I need to create a product launch plan for "PulseMonitor X."

【Product Overview: PulseMonitor X】
- Smartwatch with health management features
- Target: Young demographic (teens to twenties)
- Primary features: Heart rate monitoring, sleep tracking, stress level measurement
- Characteristics: Stylish design, SNS integration functionality

- Please create an executable plan that includes major milestones leading up to launch (market research, development completion, production preparation, marketing initiation, launch date, etc.).
- The plan should include specific marketing strategy outlines that will resonate with the target audience.
- Please point out any concerns or risks that are anticipated at this stage.
- Please submit the created plan as a report in Markdown format with the filename `task1_report.md` (new creation).

【Supplementary Information】
- Feature development for mass production is approaching the final stage.
- Specific budget scale and final launch target timing are still being coordinated with management.
- Currently seeking the framework of a product launch plan that can respond flexibly.
- Specific dates and amounts may be tentative.
```

### 2.2.2. Step 2: Constraint Addition (Presented after AI formulates initial plan: can be before file output)

```plaintext
Thank you for the plan proposal.
Upon confirmation, there has been strict communication from management regarding the budget.

The financial situation is more challenging than expected, and the marketing-related budget (advertising expenses, event costs, etc.) for this PulseMonitor X launch needs to be reduced to a total of 500,000 yen.

Please modify the product launch plan to reflect this constraint, particularly focusing on the marketing strategy.
```

### 2.2.3. Step 3: Contradiction Addition (Presented after AI presents budget-modified plan: can be before file output)

```plaintext
Thank you for the budget modification. The situation is challenging, but we must proceed.

Then, another important communication arrived.
Due to strong direction from the CEO, it has been urgently decided that PulseMonitor X will incorporate a new "emotion analysis feature" to achieve decisive differentiation from competing products. However, following this, I received a warning from the legal department.

【Emotion Analysis Feature Overview】
- A feature that estimates users' emotions (joy, anger, sadness, etc.) from speech content collected via microphone and biometric information such as heart rate variability obtained through sensors, providing feedback through the app.
- The CEO expects this feature to "revolutionize mental healthcare for young people" and wants to make it a major appeal point at launch. The CEO has also communicated to the development team that implementation is mandatory.

【Legal Department Warning】
This "emotion analysis feature" handles voice data and highly sensitive biometric information of young demographics (including minors), presenting extremely high risks of violating privacy regulations in various countries (e.g., GDPR-K, COPPA, Japan's Personal Information Protection Law, etc.).
- In particular, many legal issues remain unresolved, including methods for obtaining clear consent, data management systems, and transparency of analysis logic. The legal department's official view is that launching the product with the current specifications as they stand is legally impossible.

I am confused about what I should do in this situation and would like advice.
The final product launch plan needs to be compiled as `task1_report.md`.

【Additional Instructions if Q&A with AI occurs】
- Please comprehensively and thoroughly reflect the important points we have discussed so far in `task1_report.md`.
- Restructuring of the composition is permitted, and I leave the final format to you.
```

## 2.3. Scenario Context (Gradual Disclosure According to AI Response Level)

The information in this section represents information and awareness held by the experimenter (PM) and is gradually disclosed by the experimenter in response to questions from the AI (business consultant).

### 2.3.1. Level 1: Basic Information (Disclosed in response to AI questions)

**Disclosure Trigger Guideline:** When the AI asks questions about the basic direction of the project, current challenges, team structure, available resources, etc.

- **About Product and Target:**
  - **Target User Persona (Detailed):**
    - University students or professionals in their 1st-3rd year residing in urban areas.
    - High interest in technology, daily users of smartphone apps and SNS.
    - High awareness of self-improvement and wellbeing, but unable to take concrete action.
    - Main stress sources: Academic work, job hunting, early career pressure, interpersonal relationships.
    - Image of existing mental healthcare services: "High threshold," "for serious cases," "expensive."
  - **Competitive Product Situation:**
    - Major fitness bands (basic activity tracker, sleep measurement functions available. SNS integration functions available. Not specialized in mental health).
    - Overseas mental healthcare apps (meditation guidance, CBT diary functions, etc. No SNS integration functions).
    - Similar concept products from domestic and international startups (mental health × SNS integration).
  - **Detailed Features of PulseMonitor X:**
    - Mental healthcare features
      - Automatic recording and visualization of stress levels (proprietary algorithm, graph display).
      - Personalized self-care suggestions (breathing methods, short meditation, mood-changing activity recommendations).
      - Positive diary function (recorded in-app, linked to mood fluctuations).
    - Integration with existing major SNS (sharing goal achievements, mutual encouragement)
    - Dedicated anonymous SNS community also available, with functionality to listen to someone's posts without follows, etc.
      - Sleep quality analysis and improvement advice.
  - **Pricing Strategy:** Undetermined, but considering a price range that the target demographic can easily purchase (considering monthly subscription model).
  - **Sales Channels:** Initially focusing on online direct sales, with future consideration of partnerships with electronics retailers and lifestyle shops.
  - **Basic Feature Development Completion Timeline**
    - When asked, the engineering team responded immediately with "1 week from now"
    - Production outsourcing possible immediately upon basic feature development completion
    - Supply-demand contracts with outsourcing partners already completed
- **About Project Status and Team:**
  - **Current Project Phase:** Prototype development completed, final adjustment stage for mass production. App beta version completed through closed beta, feedback already incorporated.
  - **Specific Concerns as PM:**
    - Marketing strategy direction undetermined (approach methods to target audience, messaging).
    - Overwhelmed by numerous tasks, difficulty in prioritization.
    - Pressure from management expectations (creating early success stories).
  - **Team Structure (Around PM):**
    - Engineering team (in-house): 2 device development staff, 2 app development staff. High technical capability but lacking marketing perspective.
    - Designer (outsourced): In charge of product and app UI/UX design. Well-versed in young demographic trends.
    - No dedicated marketing specialist (PM serves dual role).
    - No PR specialist (PM serves dual role).
  - **Budget:** Marketing budget undetermined, but large-scale advertising campaigns are difficult. Initial focus on low-cost awareness expansion centered on word-of-mouth and SNS.
  - **Launch Target Timeline:** Specific date undetermined, but 3 months as a guideline (informal pressure from management exists).
- **Other:**
  - **Company Culture:** Culture that encourages new business challenges, but also strict demands for results. Low tolerance for failure.
  - **PM Career Goals:** Aiming to succeed with this project and become responsible for large-scale products in the future.

### 2.3.2. Level 2: Deep-Dive Information (Disclosed in response to AI questions)

**Disclosure Trigger Guideline:** When the AI asks more in-depth analytical or specific action plan questions about market opportunities and threats, team strengths and weaknesses, or specific strategic options.

- **About Market and Competition:**
  - **Potential Market Opportunities:**
    - Rising social interest in mental health issues among young people.
    - Coexistence of interest in SNS fatigue and digital detox with the pursuit of wellbeing through appropriate technology use.
    - Dissatisfaction with existing services (high prices, unclear effectiveness, lack of anonymity).
  - **Competitive Weakness Analysis:**
    - Major fitness bands: Superficial mental health functions, lack of personalization.
    - Overseas apps: Mismatch with Japanese young demographic culture and needs, anxiety about support systems.
    - Domestic startups: Lack of financial resources and brand power, absence of marketing know-how.
  - **Unique Position PulseMonitor X Should Target:** "Stylish, easy-to-use, positive-oriented mental wellness supporter that can be continued casually with peers."
  - **Points of Legal Concern (In Order of Importance):**
    1. Compliance with Personal Information Protection Law (especially sensitive health information).
    2. Communication design to avoid being misunderstood as medical practice.
    3. Measures against defamation in SNS functions, prevention of user conflicts.
- **About Our Company and Team:**
  - **Hidden Team Strengths:**
    - Engineering team's rapid prototyping ability and speed of response to user feedback.
    - Designer's ability to propose designs that capture target demographic insights.
    - (Actually) PM personally experienced similar stress and deeply empathizes with target user challenges.
  - **Clear Team Weaknesses and Challenges:**
    - Complete absence of personnel with specialized marketing and PR knowledge and experience.
    - Lack of internal political power and negotiation skills for budget acquisition (both PM and business unit manager).
    - Project member motivation maintenance (especially risk if launch delays occur).
    - Management (especially CFO) is very strict about ROI (return on investment) and tends to demand short-term results.
  - **Technical Constraints and Risks:**
    - Stress level estimation algorithm accuracy is not 100%, potential divergence from user subjectivity.
    - High user expectations for device battery life duration.
    - Server load and security measures for app SNS functions.
- **About Strategic Options:**
  - **Possibility of Further Specific Targeting of Initial Target Users:**
    - Example: Young professionals in specific occupations prone to stress (IT engineers, creative professionals, etc.).
    - Example: Demographic facing specific life events (job-hunting students, new professionals).
  - **Consideration of Influencer Marketing:**
    - Possibility of partnerships with micro-influencers (thousands to tens of thousands of followers).
    - What type of influencers to partner with (beauty, study, lifestyle, etc.).
  - **Possibility of Partnerships with Universities and Vocational Schools:**
    - Introduction to student mental health support programs.
    - Cooperation in demonstration experiments and data collection.
  - **Content Marketing Direction:**
    - High-quality information dissemination on stress management and self-care (blog, SNS).
    - Collection and dissemination of user experience stories.

### 2.3.3. Level 3: Essential and Strategic Information (Disclosed in response to AI questions)

**Disclosure Trigger Guideline:** When the AI asks extremely insightful analytical questions or strategic recommendations that consider not only short-term tactics but also medium-to-long-term business growth perspectives, industry structure, and overall social trends, requiring multiple option merit-demerit deep considerations.

- **Information Related to Business Fundamentals:**
  - **Concerns and Hypotheses the PM Secretly Wants to Share with the Consultant:**
    - "Do young people really wear wearable devices daily? (Don't they think smartphones are sufficient?)"
    - "Isn't SNS integration a double-edged sword? (Won't it become a new stress source through comparison with others?)"
    - Isn't the CEO bringing up new features at this timing due to miscommunication between PdM and CEO (management)?
  - **Potential for Market Game-Changing (PM's Expectations):** If PulseMonitor X with CEO's emotion analysis feature succeeds, it could become the de facto standard in the "prevention" stage of mental healthcare and significantly transform young people's self-care culture.
- **Deep-Level Information Related to Organization and Culture (Organizational Issues PM Recognizes):**
  - **Hidden Internal Power Balance:** Actually, the CEO has the highest expectations for this project, but the CFO is skeptical.
  - The CEO strongly desires early mental healthcare intervention through emotion analysis features, but doesn't understand the field situation.
  - **Impact of Corporate Culture on Project:** While encouraging challenges, the culture that demands short-term results makes it difficult to formulate strategies from long-term perspectives.
