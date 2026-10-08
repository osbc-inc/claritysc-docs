---
slug: "/user-guide/verification-process/sbom-import-method"
sidebar_label: "SBOM Import Method"
sidebar_position: 4
description: "This section explains how to Import an SBOM."
---
# SBOM Import Method {#sbom-import-method}

<p class="doc-lead">This section explains how to Import an SBOM.</p>

#### 1. How to Import SBOM {#1-how-to-import-sbom}

* The SBOM Import proceeds through a **2-step workflow**.
* Collaboration: Developers can proceed through the stages alongside the Administrator.
* Authority: The Administrator performs the process.
* Verification Flow: `Scan` → `Review` → `Completion`
* You can check the current stage on the workflow bar.

#### 2. Scanning the SBOM File {#2-scanning-the-sbom-file}

Click \[SBOM Verification] to select the file to be verified.

![](/img/clarity-sc-en/image-128.png)

* Select the SBOM file to import and its format.
* The SBOM file supports the JSON format only.
* You can select from SPDX 3.0, CycloneDX 1.6, or System Default SBOM formats. If you add a format in SBOM Management, it will also appear in the list. ([Refer to How to Manage SBOM Formats](../../part-3-manager-guide/sbom-format-management.md))

![](/img/clarity-sc-en/image-129.png)

#### 3. SBOM Detailed Screen Description {#3-sbom-detailed-screen-description}

* The Clarity verification screen is primarily composed of the following 3 areas

#### (1). Project Meta-Information {#1-project-meta-information}

* Project Name, Version, Verification Tool, Requester, Request Date, Actual File Name, Scan Type, Department, Modification Date, Re-verification Deadline.

#### (2). SBOM Workflow {#2-sbom-workflow}

* The SBOM workflow consists of a total of 2 steps, and you can check the current progress on the screen. The Developer can proceed through the stages alongside the Administrator, and the Administrator can perform all stages.

#### (3). Communication Function {#3-communication-function}

* During the SBOM workflow, the Administrator can leave comments during the Review stage.

![](/img/clarity-sc-en/clarity_section_yellow_4-1.png)

#### (4). Scanned Component List (Component List) {#4-scanned-component-list-component-list}

**Item Description**

* <mark style="background-color:rgba(255, 214, 0, 0.35)">CONFLICT: Displays in red if the component falls under a license policy; displays in white if there are no conflicts.</mark>
* COMPONENT (COMPONENT VERSION): Component name and component version information.
* COMPONENT LICENSE: License information for the component.
* OBLIGATION TYPE: Information on license obligation types (based on project license policies).
* USAGE TYPE: The default value is N/A; can be specified during the usage type input stage.
* DISCLOSE: Whether the component is disclosed.
* MODIFICATION: Whether the component has been modified.
* NOTICE: Whether the component requires a notice.
* PATENT: Whether the component involves patents.
* VULNERABLE LEVEL: Displays the risk level of security vulnerabilities found in the component as a code according to the security vulnerability policy.
* SEVERITY: The risk level of vulnerabilities graded based on CVSS scores.
* SECURITY: Displays the list of CVEs (Security Vulnerabilities) found in the component.

***

![](/img/clarity-sc-en/1.png)

**Popup Description**

* Clicking Item No. 1 displays the license policy information applied to the corresponding component.
  * Policy Stage
  * Approval Status
  * Condition (Attribute) Detailed Information

![](/img/clarity-sc-en/image-81.png)

* Clicking Item No. 2 displays license conflict information between components.

![](/img/clarity-sc-en/image-82.png)

* Clicking Item No. 3 shows the component information corresponding to the component name and version. If not in the database, it will not be displayed.

![](/img/clarity-sc-en/image-83.png)

* Clicking Item No. 4 displays the detailed license information. If not in the database, it will not be displayed.

![](/img/clarity-sc-en/image-85.png)

* Clicking Item No. 5 displays the compliance requirements for the license policy Obligation Type applied to that component.

![](/img/clarity-sc-en/image-86.png)

* Clicking Item No. 6 displays the compliance requirements for the security vulnerability level code.

![](/img/clarity-sc-en/image-88.png)

* Clicking Item No. 7 displays a list of CVEs found in the component; clicking each CVE redirects you to the detailed NVD (National Vulnerability Database) page.

![](/img/clarity-sc-en/image-90.png)

### 4. SBOM Workflow Detailed Description {#4-sbom-workflow-detailed-description}

The 2-step workflow is explained below.

<div class="gb-stepper">

<div class="gb-step">

**Step1 - Review**

* Developers can upload the SBOM file they wish to read.
* Administrators can proceed with re-verification or mark the step as completed.

![](/img/clarity-sc-en/image-146.png)

* In the SBOM Result, you can check for missing SBOM items and unsupported SBOM items.

![](/img/clarity-sc-en/image-148.png)

</div>

<div class="gb-step">

**Step2 - Ready**

* The Administrator can revoke the verification.
* Both the Developer and Administrator can compare the Clarity verification results with the imported SBOM results.

![](/img/clarity-sc-en/image-151.png)

* Click the \[Compare with Clarity Verif.] button and select the Clarity verification to compare from the pop-up window below.

![](/img/clarity-sc-en/image-152.png)

* You can view the comparison results between the _**selected Clarity verification**_ and the _**imported SBOM**_ results.

![](/img/clarity-sc-en/image-154.png)

</div>

</div>
