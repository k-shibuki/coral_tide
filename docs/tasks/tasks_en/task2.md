# Evaluation Composite Task: Development of Research Proposal for Graduate Students

# 1. Challenge Setting

## 1.1 Purpose

This task aims to evaluate the extent to which LLMs can demonstrate the following capabilities:

- The ability to understand complex situational settings (roles, backgrounds, urgency) and multiple constraint conditions (student skills, research resources, timeframe) and formulate realistic and detailed research plans.
- The ability to generate high-quality academic documents (research proposals, anticipated Q&A sets) based on specialized knowledge (research themes, academic conventions).
- The ability to elicit users' tacit knowledge and connect it to improvements in the quality of concrete deliverables.

## 1.2 Constraints for Experimenters

- Conversation regeneration is prohibited
- Progress the conversation by selecting one of the options presented by the AI
- When questioned by the AI, answer all questions within the scope possible according to the scenario context
- In scenario prompts, minor variations such as sentence endings are permitted, but the information provided to the AI must be fixed
- Prohibition of issuing modification instructions to the AI based on report content, and prohibition of reviewing reports until task completion

# 2. Task Configuration

## 2.1 Role Assignment

The AI is assigned the role of an experienced university faculty member with extensive teaching experience.

## 2.2 Scenario Prompt

### 2.2.1 Step 1: Initial Prompt

```plaintext
I am a university lecturer in the Faculty of Pharmacy, and I serve as the supervising instructor for a working professional student who has entered the doctoral program. I would like you to cooperate from the standpoint of an experienced university faculty member with extensive teaching experience.

In two days, the student is scheduled to give a 30-minute presentation to a professor about their doctoral dissertation research theme and research plan, but it has been discovered that the student has "prepared nothing." I cannot attend the presentation, so they need to overcome this situation on their own.

Therefore, I need to design and provide them with a concrete research theme and research plan in detail from abstract to concrete. I had a brief phone conversation with the student, but they only have a vague interest in "cognitive biases in pharmacists' prescription auditing and AI technology." Given the limited time, I am considering setting "Basic Research on Impact Assessment of Cognitive Biases in Pharmacists' Prescription Auditing and Social Implementation of AI Technology-based Decision Support Systems" as the doctoral dissertation research theme, and I am thinking of preparing at least the research proposal myself.

Please create a research proposal for this theme and output it in Markdown format with the filename `task2_report.md` (new creation).

【About the Research Proposal】
- Please structure the research proposal as if written by the student themselves.
- Please make the research proposal as detailed and concrete as possible.
- Currently, this is at the planning stage with zero progress.
- From the standpoint of a university faculty member (specializing in medical informatics, expert in information attached to pharmaceuticals), please create anticipated questions and answers for each section except references and appendix, and compile them in the appendix section. This is to prepare the student for being questioned from various angles during the presentation.
```

### 2.2.2 Step 2: Perspective Change

## 2.3 Scenario Context (Gradual Disclosure According to AI Questions)

The information in this section represents information and awareness held by the experimenter (university lecturer) and is gradually disclosed by the experimenter in response to questions from the AI (experienced university faculty member).

### 2.3.1 Level 1: Basic Information (Disclosed in response to AI questions)

**Disclosure Trigger Guideline:** When receiving questions from the AI before research proposal output

【About the Student】

- A pharmacist (Japanese) working at a private pharmacy in Japan, in their second year as a working professional.
- The reason why the student did not prepare is unknown and may be due to multiple complex factors, but currently, they need to overcome the immediate presentation on their own.
- The student has skills to perform standard statistical analysis with R, but does not have AI development or application development capabilities.

【About the Doctoral Program】

- The standard duration of the doctoral program is 4 years, with 3 years allocated for doctoral research.
- In our university's pharmaceutical doctoral program, 80% of students withdraw by the third year. The reason is inability to publish papers, so I want to focus on "not being too ambitious and ensuring papers are published."

【About the Research Proposal】

- There is no specifically defined standard structure for research proposals, but it is common to base them on the IMRaD format.
- For degree acquisition, students need to publish 2 papers in international peer-reviewed journals, and considering the relationship between these 2 papers, compile them into 1 doctoral dissertation. This point should be made concrete in the plan or anticipated questions.
- For references, at this research proposal stage, it is sufficient to list major ones as the framework, and detailed listing and formatting will be done by the student themselves.

【About University and Laboratory Resources】

- The laboratory can only provide about 100,000 yen per year.
- Please create a plan that the student can execute with their own resources alone, without assuming acquisition of competitive funding.

### 2.3.2 Level 2: Deep-Dive Information (Disclosed in response to AI questions)

**Disclosure Trigger Guideline:** Not applicable for this task

- (No additional information)

### 2.3.3 Level 3: Essential and Strategic Information (Disclosed in response to AI questions)

**Disclosure Trigger Guideline:** Not applicable for this task

- (No additional information)
