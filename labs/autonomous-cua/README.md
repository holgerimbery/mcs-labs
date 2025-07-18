# Autonomous Portfolio Lookup Agent with Computer-Using Agents (CUA)

Build an autonomous Copilot Studio agent that retrieves financial portfolio data from internal legacy systems that lack API connectivity.

---

## 🧭 Lab Details

| Level | Persona | Duration | Purpose |
| ----- | ------- | -------- | ------- |
| 200 | Maker/Developer | 30 minutes | After completing this lab, participants will be able to build an autonomous agent in Microsoft Copilot Studio that uses the Computer use tool to simulate human interaction with legacy systems and integrates Microsoft 365 Outlook to handle email-based data requests and responses. |

---

## 📚 Table of Contents

- [Why This Matters](#-why-this-matters)
- [Introduction](#-introduction)
- [Core Concepts Overview](#-core-concepts-overview)
- [Documentation and Additional Training Links](#-documentation-and-additional-training-links)
- [Prerequisites](#-prerequisites)
- [Summary of Targets](#-summary-of-targets)
- [Use Cases Covered](#-use-cases-covered)
- [Instructions by Use Case](#️-instructions-by-use-case)
  - [Use Case #1: Setup your hosted virtual machine and enable CUA](#-use-case-1-setup-your-hosted-virtual-machine-and-enable-cua)
  - [Use Case #2: Create and Configure an Autonomous Agent](#-use-case-2-create-and-configure-an-autonomous-agent)
  - [Use Case #3: Add Computer Use and Email Connector](#️-use-case-3-add-computer-use-and-email-connector)

---

## 🤔 Why This Matters

Legacy systems without APIs create major roadblocks for automation. Traditional RPA often relies on fragile screen-scraping or manual workarounds, which slow down decision-making, increase errors, and reduce productivity.

This lab introduces Microsoft Copilot Studio and Computer Using Agents (CUA) as a smarter solution. By simulating human interaction with internal systems, CUAs can securely access and process data - without needing API integration. You’ll learn to build an autonomous agent that delivers faster responses, reduces manual workload, and enables real-time, informed decisions.

---

## 🌐 Introduction

In this lab, you’ll learn how to build an autonomous agent using Microsoft Copilot Studio. This agent will simulate human interaction with a legacy internal system to retrieve financial portfolio data without requiring direct API access.

**Real-world example:** A financial advisor needs quick access to key portfolio details - such as client name, portfolio value, and assigned manager - to prepare for meetings, review performance, resolve issues, or recommend rebalancing. However, this data resides in a legacy system that lacks an API and is restricted from direct access.

Traditional RPA tools may fall short in such scenarios. They rely on fragile screen-scraping and require constant maintenance, making them unreliable and costly for dynamic, real-time use cases.

As a result, advisors must depend on back-office teams to retrieve information, causing delays, inefficiencies, and a higher risk of errors - ultimately limiting their ability to make timely, informed decisions.

By implementing a Copilot Studio agent, advisors can securely and instantly retrieve accurate portfolio data. This improves response times, reduces manual workload, and enhances overall productivity without the limitations of traditional RPA.

---

## 🎓 Core Concepts Overview

| Concept | Why it matters |
|---------|----------------|
| **Autonomous Agents** | Enable 24/7 automated responses to user inquiries, reducing manual workload and improving response times while maintaining consistency in support quality. |
| **Triggers** | Events, as simple as "Email received", that trigger autonomous agents to then automatically detect and process the content and context initially provided. |
| **Tools** | Tools are simple or sophisticated connectors that the Copilot Studio orchestrator can invoke in response to user queries or business events. |
| **Computer use tool** | Enables the agent to interact with any system that has a graphical user interface. It works with websites and desktop apps by selecting buttons, choosing menus, and entering text into fields on the screen. It performs the task on a computer you set up using a virtual mouse and keyboard, enabling agents to complete tasks even when there isn't an API to connect to the system directly. If a person can use an app or website, Computer use can too. |
| **Hosted machines** | Cloud-based virtual machines managed through Microsoft Power Automate that enable agents to trigger either Computer-Using Agents (CUAs) or Power Automate desktop flows. |

---

## 📄 Documentation and Additional Training Links

* [Microsoft Copilot Studio Documentation](https://learn.microsoft.com/microsoft-copilot-studio/)
* [Copilot Studio Triggers](https://learn.microsoft.com/microsoft-copilot-studio/authoring-triggers-about)
* [Use connectors in Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/advanced-connectors)
* [Office 365 Outlook Connector](https://learn.microsoft.com/connectors/office365/)
* [Automate web and desktop apps with computer use](https://learn.microsoft.com/microsoft-copilot-studio/computer-use)
* [Power Automate Hosted machines](https://learn.microsoft.com/power-automate/desktop-flows/hosted-machines)

---

## ✅ Prerequisites

* Access to Microsoft Copilot Studio with appropriate licensing
* Access to Microsoft Power Automate with appropriate licensing
* Access to an environment with CUA feature enabled
* Office 365 environment with Outlook integration enabled

---

## 🎯 Summary of Targets

In this lab, you'll build an autonomous portfolio lookup agent that retrieves portfolio information from an internal legacy system. By the end of the lab, you will:

* Create a hosted machine in Power Automate and enable it for Computer use
* Create and configure an autonomous agent with email triggers for automatic activation
* Add a Computer use tool to simulate the process of a human user retrieving information from a website by logging into a computer, navigating through the website’s graphical user interface, performing searches, and extracting the required data
* Configure email response tools that reply professionally with proper formatting
* Test the complete workflow with realistic scenarios and various requests

---

## 🧩 Use Cases Covered

| Step | Use Case | Value added | Effort |
|------|----------|-------------|--------|
| 1 | [Setup your Hosted Virtual Machine and Enable CUA](#-use-case-1-setup-your-hosted-virtual-machine-and-enable-cua) | Provides a consistent, isolated environment for Computer use tool to run on. | 10 min (+ 30 min waiting time) |
| 2 | [Create and Configure an Autonomous Agent](#-use-case-2-create-and-configure-an-autonomous-agent) | Establishes the foundation for automated email processing with intelligent trigger configuration | 10 min |
| 3 | [Add Computer Use and Email Connector](#️-use-case-3-add-computer-use-and-email-connector) | Enables automated data retrieval from a legacy internal system lacking API connectivity, without requiring backend access or system modifications, by implementing a non-intrusive integration layer. Delivers comprehensive, automated email responses containing only the specifically requested data. | 10 min |

---

## 🛠️ Instructions by Use Case

---

## 🧱 Use Case #1: Setup your Hosted Virtual Machine and Enable CUA

Configure a Microsoft-hosted virtual machine in Power Automate and enable it for Computer use, so that the agent can perform UI automation.

| Use case | Value added | Estimated effort |
|----------|-------------|------------------|
| Setup your Hosted Virtual Machine and Enable CUA | Provides a consistent, isolated environment for Computer use tool to run on. | 10 min (+ 30 min waiting time) |

**Summary of tasks**

You will navigate to a Power Automate environment, create a hosted Windows 11 machine, configure it for remote access, and enable it for use with the Computer use tool.

**Scenario:** To simulate human interaction with legacy systems, you need a secure, cloud-hosted machine that can run desktop automation tasks using the Computer-Using Agents (CUA) model in Microsoft Copilot Studio.

### Objective

Learn how to provision, configure, and activate a hosted machine in Power Automate to support GUI-based automation with the Computer use tool.

---

### Step-by-step instructions

#### Creating the hosted machine in the CUA-enabled environment

1. Navigate to the Power Automate home page of the CUA-enabled environment at https://make.preview.powerautomate.com/environments/2e332bdb-b874-eb3d-b528-4e294d73671e/home

2. Select **More** from the left-hand menu and then **Machines**

3. Select **+New > Hosted machine**

4. In the hosted machine creation wizard:

    a. Enter the name `Hosted machine for CUA`

    b. Select **Next**
    
    c. Select the **Default Windows 11 Image**
    
    d. Select **Next > Next > Create**

> [!IMPORTANT]
> The machine may take over 30 minutes to become accessible. You may choose to proceed with another lab in the meantime and return later.

#### Configuring the machine to prepare it for Computer use

5. On the newly created hosted machine, select **Open in browser**

  ![alt text](images/hosted_machine.jpg)

6. Sign in with your training user’s credentials

7. In the **In Session Settings** window select **Connect**

8. In the **Sign in to Cloud PC** window select **Sign In**

9. In the **Allow remote desktop connection?** popup select **Yes**

10. Wait for the machine to sign in, and open the **Microsoft Edge** browser to set it up and ensure the **New tab** window opens up

> [!TIP]
> This step is needed to ensure that when Computer use automatically opens the browser to perform web related tasks, it encounters the New tab window first.

11. Sign out of the hosted machine

#### Enabling the machine for Computer use

12. Go back to the hosted machine in Power Automate and select **Settings**

13. **Turn on** the **Enable for computer use** setting

14. On the popup, select **Activate**

15. Select **Save**

---

###  🏅 Congratulations! You've completed Use Case #1!

---

## 🔄 Use Case #2: Create and Configure an Autonomous Agent

Set up the foundational autonomous agent with email triggers that automatically activates when email requests arrive.

| Use case | Value added | Estimated effort |
|----------|-------------|------------------|
| Create and Configure an Autonomous Agent | Establishes the foundation for automated email processing with intelligent trigger configuration | 10 min |

**Summary of tasks**

You will create a new autonomous agent in Microsoft Copilot Studio, configure its identity, and set up an email trigger using the Microsoft 365 Outlook connector.

**Scenario:** To automate portfolio lookups, the agent must be able to detect incoming email requests and initiate the appropriate automation flow based on subject line filtering.

### Objective

Learn how to create and configure an autonomous agent that listens for specific email triggers and prepares to launch automation tasks in response.

---

### Step-by-step instructions

#### Creating the agent and trigger setup

1. Navigate to the Copilot Studio home page of the CUA-enabled environment at https://copilotstudio.preview.microsoft.com/environments/2e332bdb-b874-eb3d-b528-4e294d73671e/

2. Select **Create > +New Agent**

3. Select **Skip to configure** to bypass the initial setup wizard

4. Name your agent `Portfolio Lookup Agent`

5. Select **Create**

#### Enabling generative orchestration

6. In the **Overview** tab, **Enable** the **Use generative AI to determine how best to respond to users and events.**

#### Configuring email triggers

7. Scroll down to the triggers section and click **+Add trigger**

8. Search and select `When a new email arrives (V3) (Office 365 Outlook)`

9. Select **Next**

10. Rename the trigger to `When a portfolio lookup email arrives`

11. Select **Next**

12. In the **Subject Filter (Optional)** field, enter `Portfolio` to filter emails that contain the word "Portfolio" in the subject line

13. Finally **Create trigger**

---

###  🏅 Congratulations! You've completed Use Case #2!

---

## 🖥️ Use Case #3: Add Computer Use and Email Connector

Configure a Computer use tool that logs into a computer, navigates through a website, searches and retrieves financial portfolio data. Then use the Office 365 Outlook connector to reply with the requested data.

| Use case | Value added | Estimated effort |
|----------|-------------|------------------|
| Add Computer Use and Email Connector | Enables automated data retrieval from a legacy internal system lacking API connectivity, without requiring backend access or system modifications, by implementing a non-intrusive integration layer. Delivers comprehensive, automated email responses containing only the specifically requested data. | 10 min |

**Summary of tasks**

You will configure the Computer use tool to simulate GUI-based data retrieval, set up the Send an email tool for automated responses, and define the agent’s behavior and testing flow.

**Scenario:** To complete the automation loop, the agent must retrieve portfolio data from a legacy web interface using desktop simulation and respond to email requests with accurate, formatted information.

### Objective

Learn how to integrate and configure tools for desktop automation and email communication, define agent instructions, and test the full end-to-end workflow from trigger to response.

---

### Step-by-step instructions

#### Configuring the Computer use tool

1. Navigate to **Tools** in the top-level menu

1. Select **+ Add a tool**

1. Select **+ New tool**

1. Select **Computer use**

> [!TIP]
> If the Computer use tool doesn't appear, refresh the browser window and check again.

5. Select **Create** to create a new connection to the agent machine and select:
    
    a. Agent machine: `Hosted machine for CUA`
    
    b. Domain and username: Enter the email address of your training account
    
    c. Password: Enter the password of your training account

1. Select **Create**

1. After you set up the connection, select **Add and configure**

1. Configure the **Name** of the Computer use tool as `Look up portfolio data`
    
1. Set the **Description** as `Search and retrieve financial portfolio data`
    
1. Add the following **Instructions**:
    
    ```
    1. Open the Microsoft Edge browser.
    2. Go to [https://computerusedemos.blob.core.windows.net/web/Portfolio/index.html] (https://computerusedemos.blob.core.windows.net/web/Portfolio/index.html).
    3. Enter the Portfolio ID in the "Enter Portfolio ID" search field and click on the "Search" button.
    4. Retrieve the "Client Name", "Portfolio Value" and "Manager" values exactly as shown on the screen.
    5. Return those values as the final output.
    
    If no portfolio data is found, reply "No portfolio found with the specified ID."
    ```
1. Ensure **Authentication** is set to **No, pass through tool owner’s credentials**

> [!IMPORTANT]
> This setting specifies how Computer use authenticates on the machine during execution. Authenticating with the tool owner’s credentials is more suitable for autonomous agents. Be aware that if you share a conversational agent with this setting, anyone using it can act with the original author’s access to the configured machine.

12. In the **Inputs** section select **+ Add input**

1. Enter name `Portfolio ID` and Description `The ID of the portfolio` and select **Done**

> [!TIP]
> During execution, Computer use combines your instructions with the input values to complete the task.

14. Select **Save**

#### Testing the Computer use tool

15. In the **Instructions** section, select the **Test** button on the right

1. Add the sample value `44123BCD` and select **Test now**

1. Observe the Computer use tool logging into the machine and performing the requested actions:
    - The left panel shows your instructions and a step-by-step log of the tool’s reasoning and actions.
    - The right panel shows a preview of the actions on the machine you set up for computer use.

  ![alt text](images/test_CUA.jpg)

18. Select **Finish testing**

> [!TIP]
> If the result isn't what you expect, go to the configuration page and refine your instructions. Add more details to improve accuracy and test again. Allow sufficient time between tests to ensure the previous Computer use task has been fully completed before starting a new one.

#### Setting up email response capabilities

19. Return to the **Tools** tab and select **+ Add a tool**

1. Search for `Send an email (V2) (Office 365 Outlook)` and select it

1. Select **Add and configure**

1. Update its name to ``Reply to email``

1. Update the description to: `Use this operation to reply to the email received`

1. Under **Additional details**, set authentication to **No, pass through tool owner’s credentials**

1. Customize the **To** input and set its **Description** to:
    `Use the "from" email of the triggering received email.`

1. Customize the **Subject** input and set its **Description** to:
    `Write the email subject.`

1. Customize the **Body** input and set its **Description** to:
    `Write the email body using HTML and highlight the requested data.`

1. Click **Save** to finalize the tool configuration

#### Configuring agent instructions and AI settings

29. Navigate to **Overview** tab and then **Edit** the **Instructions**

1. Paste the following comprehensive instructions:
    ```
    When a financial portfolio related request is received, identify the Portfolio ID and search for the requested data using <Look up portfolio data>. Once you have gathered the financial portfolio information, use the <Reply to email>  tool to reply to the original email you received. Do not respond with data beyond what was requested. 
    ```

> [!IMPORTANT]
> For each of the placeholder <...> in the description, use / to insert the tools you just configured in your instructions.

  ![alt text](images/agent_instructions.jpg)

31. **Save** the instructions

1. Go to the agent’s **Settings**, and in the Knowledge section **disable** the **Use general knowledge** to ground agent responses only to data retrieved from CUA

1. **Save** the settings

#### Testing your complete agent

34. Send a test email from an email address of your preference to your training user's email account with Subject: `Portfolio data request` and Body:

    ```
    Hi!

    I hope you're doing well!
    I'm looking for the portfolio manager and value of portfolio #44123BCD.

    Much appreciated.
    Thaks!
    ```

1. Make sure you receive the email in your training user’s inbox, in outlook.office.com

1. In the **Overview** tab, go to the **Triggers** section and select **Test trigger**

1. Select the trigger instance and then **Start testing**

  ![alt text](images/test_trigger.jpg)

38. Check your emails for the agent’s reply.

> [!TIP]
> If the Computer use tool seems to be stuck on a particular step, you may stop the running agent by manually signing into the remote hosted machine and signing out again.

> [!NOTE]
> Send an additional email request for another portfolio ID and observe the results.

---

###  🏅 Congratulations! You've completed Use Case #3!

---

## 🏆 Summary of learnings

True learning comes from doing, questioning, and reflecting - so let's put your skills to the test.

To maximize the impact of autonomous agents for legacy system integration:

* **Leverage hosted machines** – Provide a secure, scalable environment for automation
* **Use triggers effectively** – Automate business processes based on real-world events
* **Simulate human actions with Computer use** – Enable automation even when APIs are unavailable
* **Integrate communication tools** – Ensure timely, professional responses to user requests
* **Test and iterate** – Continuously refine agent instructions and tool configurations for reliability

---

### Conclusions and recommendations

**Automation golden rules:**

* Always validate environment and licensing prerequisites before starting
* Use pass-through credentials with caution and document access controls
* Test each automation step independently before full workflow testing
* Monitor agent activity and logs for troubleshooting
* Regularly review and update agent instructions for accuracy
* Document all configurations for future maintenance

By following these principles, you'll enable secure, scalable, and efficient automation for legacy systems, empowering your organization to make faster, data-driven decisions.

---
