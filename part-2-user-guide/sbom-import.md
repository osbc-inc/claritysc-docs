---
description: Explains how to import an SBOM.
---

# How to Import SBOM

#### 1. Overview of the SBOM Import Feature

You can upload an external or internally generated SBOM file to register the component list and security information into the system and proceed with the verification workflow.



* SBOM Import is conducted as a **2-step workflow**.
* Developers can proceed together with administrators.
* Administrators can proceed with the workflow.
* Verification Flow: _Scan → Review → Ready_
* You can check the current step on the workflow bar.



#### 2. Scanning an SBOM File

Click the **\[SBOM Import\]** button to select the file to verify.

<figure><img src="../../.gitbook/assets/image (247).png" alt=""><figcaption></figcaption></figure>



**Supported File Formats and Specifications**

* Supported Extensions: .json, .txt, .jsonld, .xml, .rdf, .rdf.xml, .xlsx
* Guide to Using the Excel Template:
  * If you do not have a standard SBOM file, click the (DOWNLOAD EXCEL TEMPLATE) link at the bottom of the upload area to download the template.
  * After entering component and license information according to the **specified Excel template fields**, you can upload it as an .xlsx file.



**Upload and Automatic Format Detection**

* Registering a File: Click the Upload file area to select the target SBOM file, or drag and drop it. (To change the file, use the Change file button on the right.)
* Automatic Format Analysis (DETECTED FORMAT):
  * Once the file is uploaded, the system analyzes its internal structure and automatically recognizes the SBOM standard specification and version. ([Refer to SBOM Format Management Guide](../../undefined-1/sbom-1.md))

<div align="left"><figure><img src="../../.gitbook/assets/image (248).png" alt="" width="543"><figcaption></figcaption></figure></div>

#### 3. SBOM Detail Screen Overview

* The Clarity verification screen largely consists of the following three areas (plus the scanned component list below).

#### (1). Project Meta Information

* Project Name, Version, Verification Tool, Requester, Request Date, Actual File Name, Scan Type, Department, Modified Date, Re-verification Due Date \
  This is the area where you can check the main information of the project.

#### (2). SBOM Workflow

* The SBOM workflow consists of 2 steps in total, and you can check the current progress status on the screen. Developers can proceed with steps together with administrators, while administrators can proceed with all steps.

#### (3). Communication Feature

* Developers and administrators can communicate during the SBOM workflow process.
  * **Comments**: You can check comments left by developers and administrators at each verification step and exchange opinions.

<div align="left"><figure><img src="../../.gitbook/assets/clarity_section_yellow_4 (1).png" alt=""><figcaption></figcaption></figure></div>

#### (4). Scanned Component List

**Field Descriptions**

* <mark style="background-color:yellow;">CONFLICT: Displayed in red if the component violates the license policy, and in white if there is no conflict.</mark>
* COMPONENT (COMPONENT VERSION): Component name and component version information.
* COMPONENT LICENSE: License information for the component.
* OBLIGATION TYPE: Obligation type information for the license (based on the project license policy).
* USAGE TYPE: The default value is N/A, and it can be specified during the linking/binding type input step.
* DISCLOSE: Whether the component source code must be disclosed.
* MODIFICATION: Whether the component has been modified.
* NOTICE: Whether copyright/license notice is required for the component.
* PATENT: Whether patent rights apply to the component.
* VULNERABLE LEVEL: Displays the risk level of security vulnerabilities found in the component as a code according to the security vulnerability policy.
* SEVERITY: The severity rating of the vulnerability based on the CVSS score.
* SECURITY: Displays the list of CVEs (security vulnerabilities) found in the component.

***

<figure><img src="../../.gitbook/assets/컴포넌트　목록 (1).png" alt=""><figcaption></figcaption></figure>



**Pop-up Descriptions**

* Clicking item 1 displays the _license policy_ information applied to the component.&#x20;
  * Policy stage&#x20;
  * Approval status
  * Condition (attribute) details

<div align="left"><figure><img src="../../.gitbook/assets/image (77).png" alt="" width="344"><figcaption></figcaption></figure></div>



* Clicking item 2 displays license conflict information between components.&#x20;

<div align="left"><figure><img src="../../.gitbook/assets/image (78).png" alt="" width="429"><figcaption></figcaption></figure></div>



* Clicking item 3 displays component information corresponding to the _component name_ and _component version_. Nothing is displayed if it does not exist in the DB.

<div align="left"><figure><img src="../../.gitbook/assets/image (79).png" alt="" width="324"><figcaption></figcaption></figure></div>



* Clicking item 4 displays detailed information about the license. Nothing is displayed if it does not exist in the DB.

<div align="left"><figure><img src="../../.gitbook/assets/image (81).png" alt="" width="326"><figcaption></figcaption></figure></div>



* Clicking item 5 displays the fulfillment requirements for the license policy Obligation Type applied to the component.

<div align="left"><figure><img src="../../.gitbook/assets/image (82).png" alt="" width="396"><figcaption></figcaption></figure></div>



* Clicking item 6 displays the action items/requirements for the security vulnerability rating code.

<div align="left"><figure><img src="../../.gitbook/assets/image (84).png" alt="" width="416"><figcaption></figcaption></figure></div>



* Clicking item 7 displays the list of CVEs found in the component; clicking each CVE redirects you to its detailed page on the NVD.

<div align="left"><figure><img src="../../.gitbook/assets/image (86).png" alt="" width="416"><figcaption></figcaption></figure></div>





### 4. Detailed Explanation of the SBOM Workflow

Let's explain each of the 2 steps in detail.

{% stepper %}
{% step %}
**Step 1 - Review**

* Developers can upload the SBOM file they want to review.
* Administrators can re-verify or complete (approve) the verification.

<figure><img src="../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

* You can check missing SBOM items and unsupported SBOM items in the SBOM Result.

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>


{% endstep %}

{% step %}
**Step 2 - Ready**

* Administrators can cancel/release the verification.
* Both developers and administrators can compare Clarity verification results with Import SBOM results.

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>



* Click the \[Compare with Clarity Verif.\] button and select the Clarity verification to compare from the pop-up window below.

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>



* You can view the comparison results between the selected _**Clarity Verification**_ and the _**Imported SBOM**_.

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}