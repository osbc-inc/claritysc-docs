---
slug: "/manager-guide/writing-a-notice"
sidebar_label: "Writing a Notice"
sidebar_position: 6
description: "This section explains how to write a notice."
---
# Writing a Notice {#writing-a-notice}

<p class="doc-lead">This section explains how to write a notice.</p>

#### 1. Notice Overview {#1-notice-overview}

* A Notice serves as an official document provided to users to inform them of the license and copyright information of the open-source components included in the software.

#### 2. How to Draft a Notice {#2-how-to-draft-a-notice}

* Administrators can generate a notice using the following two methods

**(1). Generation During the Verification Workflow**

* After the SBOM report distribution is complete, click the \[Request Notice] button to generate the notice information.

![](/img/clarity-sc-en/image-71.png)

* Clicking \[Send Notice] creates a notice information workflow.

![](/img/clarity-sc-en/image-194.png)

**(2). Direct Generation via Menu**

* You can generate a notice or open-source disclosure by clicking the \[Add Notice] button in the **Project > Notice Information List** menu.

![](/img/clarity-sc-en/image-139.png)

#### 3. Notice Information Screen Layout {#3-notice-information-screen-layout}

* The Notice Information screen is composed of five main areas.

![](/img/clarity-sc-en/image-6.png)

**(1). Notice Meta-Information Area**

* Notice ID: Unique ID for the notice information.
* Write Completion Expected Date: The estimated date for completing the draft.
* Notice Information Write: The current drafting status of the notice information.
* Disclosed Code Information Write: The current drafting status of the disclosed code information.

**(2). Notice Workflow Area**

* This area manages the progression through the stages of drafting, reviewing, and distributing the notice information.

**(3). Project Information Area**

* This area displays the basic information of the target project for which the notice information was generated.

**(4). SBOM Report Information Area**

* This area displays the basic information of the source SBOM report used to generate the notice.

**(5). OSS Used Information Area**

This area allows you to review the list of open-source components used in the target file and their corresponding verification results.

* Component Name and Version
* License Information
* Obligation Type
* Usage Type
* Status of Disclosure, Modification, Notice, and Patent
* Security Vulnerability Levels (Vulnerability Level / Severity / Security)

***
