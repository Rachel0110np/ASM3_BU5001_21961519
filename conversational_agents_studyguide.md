## Experiment: Study Guide Generation
**Prompt:**  
Create a structured study guide that summarises the main concepts, frameworks, and chatbot design principles from my uploaded BUS5001 lecture

**AI Response:**  
This structured study guide summarizes the main concepts, frameworks, and chatbot design principles covered in the BUS5001 lecture excerpts.
## BUS5001 Study Guide: Conversational Agents and Chatbot Design

### I. Core Concepts and Definitions

| Concept | Definition/Purpose | Key Details |
| :--- | :--- | :--- |
| **Conversational Systems** | Systems that interact with people through language with the goal of fulfilling a specific function or purpose. | They leverage language to achieve utility. |
| **Conversational UX (CUX)** | The incorporation of chat, voice, or other technologies to mimic natural human conversation. | The principle suggested by the movie "Her" is that human and technology interactions can be deep, meaningful, and human. |
| **Chatbot (Oracle)** | A computer program that simulates and processes human conversation (written or spoken), enabling interaction with digital devices as if communicating with a real person. | This definition focuses on simulation and processing of conversation. |
| **Chatbot (IBM)** | A computer program utilizing Artificial Intelligence (AI) and Natural Language Processing (NLP) to understand customer questions and automate responses, simulating human conversation. | This definition highlights the role of AI and NLP in automating responses. |
| **Benefits of CUX** | Six primary advantages gained by using conversational user experience. | **Efficiency, Accessibility, Intuitiveness, Empathy, Trust, Personalisation**. |
| **Evaluating Intelligence (Turing Test)** | Alan Turing addressed the question, "Can machines think?" but ultimately deemed it "too meaningless" to discuss. | The test (Imitation Game) involves a human questioner trying to distinguish between a human respondent and a computer respondent. A computer that is indistinguishable from the human is considered intelligent. (A chatbot named Eugene Goostman passed the test in 2014). |

### II. Chatbot Frameworks and Architectural Components

#### A. Architecture and Frameworks
The lecture touches upon various models and architectures relevant to building and deploying conversational agents:

*   **Models and Architectures:** Chatbot Conceptual Model, A Simple Chatbot Architecture with RASA, and Enterprise Grade Chatbot Architecture are mentioned.
*   **Frameworks:** Examples include the Microsoft Bot Framework / Platform.
*   **Context:** The material provides context regarding advancements in AI, citing technologies like GPT-3, Bunji, Cooee, Watson, AlphaGo, and mainstream apps.

#### B. Anatomy of Dialog and Language Understanding
Conversational systems rely on specific components to process and respond to user input:

*   **Utterances:** These are the inputs provided by users.
*   **Intents:** These are categories or classifications representing the user's intentions (e.g., recognizing that "Turn on the kitchen light" is a `TurnOnDevice` intent).
*   **Entities:** A collection of objects consisting of data extracted from an utterance, such as places, times, and people.
*   **Recognizers:** When a dialog is invoked, the recognizer processes the message to extract the primary intent and any entity values. This information is then passed onto the dialog's triggers.

#### C. Triggers
Triggers are essential for defining what actions a bot performs based on an event:

*   The basic concept is: **"When (event) happens, do (actions)"**. A trigger acts as a conditional test on an incoming event.
*   **Intent Triggers:** Include events like Intent recognized, QnA Intent recognized, Unknown intent, or Duplicated intents recognized.
*   **Dialog Event Triggers:** Include events like Dialog started (Begin dialog event), Dialog cancelled (Cancel dialog event), Error occurred (Error event), or Re-prompt for input (Reprompt dialog event).

### III. Chatbot Design Principles and Process

#### A. Designing a Chatbot: High-Level Process
The design process follows a standard software engineering lifecycle:

1.  **Define your Context:** Define User Personas and Identify User Stories.
2.  **Service Discovery and Mapping**.
3.  **Script your Conversational UX**.
4.  **Build your Chatbot:** This involves iterations, Design, Build, Deploy, and Evaluate.

#### B. Defining Context (User Personas and Stories)
User Personas are critical for designing the automation process:

*   **Purpose:** Identify for whom the automation process is designed to cater.
*   **Research:** Conduct research and speak to all involved stakeholders.
*   **Understanding Users:** Understand who users are and how they interact with your processes.
*   **Establish:** Personas should establish user actions, motivations, pains, values, and context. They must adequately represent a user group.
*   **User Story Mapping:** User Stories (WHO, WHAT, WHY) are mapped to the services that provide them. This mapping aids in prioritizing and scheduling services (Discover vs. Acquire vs. Build).

#### C. Scripting Conversational UX
Conversational UX design is the vehicle used to chart and navigate interactions between humans and technology through language.

*   **Scripting Focus:** Finding the persona needs within the user journey, identifying the necessary outcome, and crafting the narrative first.
*   **Tools:** Tools like Excel and Lucid Charts can be used for scripting.

##### Key Scripting Principles:

*   Remember your **Personas and User Stories**.
*   Maintain **Clarity** in the context.
*   Ensure **Consistency** in language (e.g., emojis, punctuation).
*   Keep responses **Concise and brief** (ideally 1 or 2 lines).
*   **Vary responses** (maintain a collection).
*   Use **Natural** language.
*   Incorporate **Pauses**.

#### D. Handling Complexity: Intent and Flow Management

*   **Disambiguation of User Intent:** This is the process of narrowing down a user's intent. Approaches include asking more questions, narrowing down through options, or using targeted questions. Designers must also prepare for out-of-scope questions.
*   **Handling Interruptions:** While conversational flows are designed to be linear, users rarely follow this path. Strategies include:
    *   **Keep the flow:** Insist that the user answer the original question first.
    *   **Reset the flow:** Disregard previous actions, reset the dialog stack, and start over by addressing the user's new question.
    *   **Store the flow:** Attempt to answer the user's current question and then return to the original flow.

#### E. Common Pitfalls in Conversational Interface Design

These pitfalls are described in terms of "five personalities" that designers should avoid:

1.  **The "stubborn bot":** Insists on maintaining the current conversation course even when the user tries to change direction. *Prevention:* Specify a maximum number of retry attempts for each question.
2.  **The "clueless bot":** Responds nonsensically when it fails to understand a user's attempt to access functionality.
3.  **The "mysterious bot":** Delays response, potentially due to an outage or processing input. *Mitigation:* Send a "typing" message or follow up with a proactive message to indicate the bot is working.
4.  **The "captain obvious bot":** Provides unsolicited information that is completely obvious and useless to the user.
5.  **The "bot that can't forget":** Inappropriately integrates information from past conversations into the current one.

#### F. Graceful Fallbacks and Ending Conversations

*   **Graceful Fallbacks:** Necessary when the agent is insufficient.
    *   Set clear expectations up front.
    *   Provide clarity in the fallback, such as, "Sorry, I didn't get that. I can help you [X] or [Y]. Do you want to try one of those things?".
    *   Redirect the user toward the tasks the bot *can* handle.
    *   Seek understanding and establish domain expertise.
    *   Have variations in fallback language to avoid repetition.
*   **Hand-Off:** If necessary, limit fallbacks to no more than two questions. The user must know what is happening, whether they are connecting to a human or another resource, and what the next required steps are. It is essential to **carry over context** during the hand-off.
*   **Ending Conversations:** Don't just say goodbye; this is an opportunity to add value or gather feedback. Ask follow-up questions.
*   
**Citations:**  
[1] BUS5001-Wk10-ConversationalAgents.pdf
 
