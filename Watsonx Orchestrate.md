# Getting Started with watsonx Orchestrate

## Create an IBM Cloud Account¶
**New Users:**  Register at [https://cloud.ibm.com/registration?utm_content=academicsb](https://cloud.ibm.com/registration?utm_content=academicsb)

**Existing Users:**  If you already have an IBM Cloud account, simply log in at [https://cloud.ibm.com](https://cloud.ibm.com/) to continue with the setup.

For more information, see [IBM Cloud – Getting Started](https://cloud.ibm.com/docs/account?topic=account-account-getting-started)

## Set Up watsonx.ai Account
* Visit: [https://www.ibm.com/products/watsonx-ai](https://www.ibm.com/products/watsonx-ai)
* Click **Start your free trial**

## Set Up watsonx Orchestrate
* Go to the official IBM Watsonx Orchestrate trial page: [https://www.ibm.com/products/watson-orchestrate](https://www.ibm.com/products/watson-orchestrate)
* Locate and click the **Free 30-day trial** or similar button.
* After completing the sign-up, you'll be redirected to the Watsonx Orchestrate workspace. You may receive a welcome email with getting started resources.

## Create and Configure Projects in watsonx.ai
* Log in to the [IBM Watsonx.ai](https://dataplatform.cloud.ibm.com/wx/home?context=wx) platform with your credentials.

* **Option 1: Sandbox Project** (Recommended for New Users)
  * If no project exist, click Create sandbox project.
  * It sets up a preconfigured environment with a watsonx.ai Runtime service instance automatically associated

* **Option 2: Custom Project**
  * Go to the Projects section (in the sidebar or home page)
  * Click Create Project
  * Enter a project name and optional description
  * Select an IBM Cloud Object Storage instance when prompted

### Enable watsonx.ai Runtime
* Sandbox projects come with the runtime service pre-associated.
* For **custom projects**, after creation:
  * The project must have an associated watsonx.ai Runtime service instance. Otherwise, you might be prompted to associate the service when you open the Prompt/Agent Lab.
  * For detailed instructions on how to associate the runtime service manually, see the official docs: [Associate watsonx.ai Runtime service to your project](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/assoc-services.html?context=wx&audience=wdp&locale=en)
* Without this, features like Prompt Lab and Agent Builder will be inaccessible.

## Understanding IBM watsonx Orchestrate
IBM watsonx Orchestrate is an AI-powered digital worker platform that helps automate repetitive, multi-step tasks across different business tools—without requiring coding. It allows employees to offload tasks to AI "digital workers" that act like virtual assistants.

### Key Concepts
1. **Tools** - Think of these as mini-automation or actions (e.g., “Schedule a meeting,” “Generate a report”). They can connect to business apps like Slack, Microsoft Teams, SAP, Salesforce, and more.
2. **Digital Workers** - AI-driven personas that perform tasks on your behalf. You can interact with them using natural language (chat-style interface).
3. **Orchestration** - Watsonx Orchestrate coordinates multiple apps and services to complete workflows. It handles multi-step tasks, like hiring a candidate, updating a CRM, or creating a support ticket.
4. **Integration** - Built-in connectors and APIs allow integration with third-party systems. Skills can be customized to match your business processes.

### How It Works
User types a task in plain language (e.g., "Send an offer letter to John Smith"). Watsonx Orchestrate interprets the request using natural language understanding (NLU). Digital worker executes the task by calling the appropriate skills and tools. Results are delivered back to the user in a conversational interface or integrated platform.

## Use Cases
- HR automation (e.g., onboarding, offer letters)
- Sales and CRM updates
- IT ticket resolution
- Financial reporting
- Document processing
- and many more.

## Benefits
- Reduces manual, repetitive work
- Speeds up business processes
- Increases accuracy and compliance
- Frees up employee time for strategic work

## How to go about building
1. Start with ~[Knowledge](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-uploading-files-knowledge)~ (content to ask questions against a.k.a. RAG) 
2. ~[Customize](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-customizing-welcome-message-starter-prompts)~ the agent **welcome message & starter prompts** to give an idea of what it can do  
3. Then think about **what to do** once we got the info you looked for (this is only the first step!)
   * E.g., email the info to self / fellow student(s), or inquire for more info by submitting a ticket
   * Which (likely **productivity**) **~[tools](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=catalog-prebuilt-tools)~** you would want to ~[add](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agent-adding-from-catalog)~ to your agent for that?
   * Note most tools from our catalog might still be tricky to connect (more an enterprise setup; WIP), so we suggest the following:
     * For your (big picture) story: **think of the use-case** based on any app you can think of (even beyond what we have in our ~[catalog](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=catalog-prebuilt-tools)~)
     * For your (start small) implementation: look at those tools we are providing
       * Tool to get a [list of department contacts and their information](https://jaymig.github.io/wxo-agents/examples/department-contacts/tools/email-department-contact.json) (from the ~[tutorial](https://jaymig.github.io/wxo-agents/wxo-agents/department-contact/)~ you may have done already)
       * Gmail & Google Search custom tools we will upload to your instances on the day of the hackathon. You can refer them here - ~[https://github.com/shrinaththube/watson-orchestrate-search-toolkit](https://github.com/shrinaththube/watson-orchestrate-search-toolkit)~ 
4. [Instructions/guidelines](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-configuring-behavior) is where the “magic" happens
   * The "code“ which happens to be **plain English** (or another language if you wish:), hence no/low-code.
   * This is where/how you control the user experience, ensure the tools accomplish what the user needs, within the necessary boundaries.
   * Think of it as you are talking to a 5-year old and spell every instructions clearly so nothing can be up for interpretation. 
5. Break down your agents in several [collaborator agents](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-adding-orchestration) (their description will help orchestrator/parents agent to triage across them)
   * If you see an opportunity to **re-use** across multiple agents/use-cases long term
   * If the instructions become **too large/complex to manage** in one agent  
6. If you have time, you can ~[test your agent](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-testing-analyzing)~ to see if the instructions & the knowledge are robust enough


## Further Reading
* [watsonx Orchestrate Tutorials](https://jaymig.github.io/wxo-agents/)
* [Official watsonx Orchestrate product page](https://www.ibm.com/products/watson-orchestrate)
* [watsonx Orchestrate Documentation](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base)
* [watsonx Orchestrate Community](https://community.ibm.com/community/user/groups/community-home?communitykey=3ad46381-9535-462e-85c9-568b21f4b067)
* [Help us improve watsonx Orchestrate, submit your ideas](https://watson-orchestrate.ideas.ibm.com/)
* [Official watsonx.ai product page](https://www.ibm.com/products/watsonx-ai)
* [watsonx.ai Documentation](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/welcome-main.html?context=wx&audience=wdp)
- Connecting to watsonx Orchestrate through ~[3rd party channels](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-connecting-channels)~
* Connecting to a [live agent](https://www.ibm.com/docs/en/watsonx/watson-orchestrate/base?topic=agents-connecting-live-agent)
