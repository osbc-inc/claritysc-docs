---
description: You can configure VEX for CVEs detected in components.
---
sidebar_position: 5

# VEX Guide

#### 1. What is VEX (Vulnerability Exploitability eXchange)?

VEX is a standard security specification that defines the analysis results and status regarding **whether a known vulnerability (CVE) is actually exploitable (impactful) in your actual product/service environment** when discovered in open-source libraries or other software components.

* Even if a library version containing a vulnerability is used, there may be no actual impact if the vulnerable code or function is not called, or if defensive logic has been implemented.
* VEX allows you to systematically classify and manage this actual exploitability (impact level).



#### 2. Screens Where VEX Can Be Configured

<table><thead><tr><th width="145.75">Menu Category</th><th>Screen/Menu Location</th><th>VEX Configuration Conditions & Behavior</th></tr></thead><tbody><tr><td>Project</td><td><ol><li>COMPONENT LIST at the bottom of the project's <strong>Clarity, FossID, or ClarityAIR</strong> verification tool detail screen</li><li>Click the icon under the SECURITY column</li></ol></td><td><p>Verification Workflow</p><ul><li><strong>In Progress</strong>: Only CVE details can be viewed</li><li><strong>Ready</strong>: The VEX configuration panel (REVIEW) is activated and editable</li></ul></td></tr><tr><td>In Project > SBOM Import</td><td><ol><li>SBOM Import detail screen within a project</li><li>Click the icon under the SECURITY column</li></ol></td><td><p>Workflow</p><ul><li><strong>Under Review</strong>: Only CVE details can be viewed</li><li><strong>Ready</strong>: The VEX configuration panel (REVIEW) is activated and editable</li></ul></td></tr><tr><td>SBOM Report</td><td><ol><li>SBOM Report detail screen</li><li>Click the icon under the SECURITY column</li></ol></td><td><ul><li>VEX can be configured for each component's CVE in the generated report</li></ul></td></tr><tr><td>Product Management</td><td><ol><li>Click the [Merged View] or [Merged Group Component] button</li><li>Merged component screen in the product</li><li>Click the icon under the SECURITY column</li></ol></td><td><ul><li>VEX can be configured for CVEs of components merged into the product</li></ul></td></tr><tr><td>SBOM Merge Details</td><td><ol><li>SBOM Merge detail screen</li><li>Click the icon under the SECURITY column</li></ol></td><td><ul><li>VEX can be configured for CVEs in the merged SBOM</li></ul></td></tr></tbody></table>





#### 3. How to Configure VEX

a. Navigate to a location listed in [**2. Screens Where VEX Can Be Configured**](vex.md#id-2.-vex) and click the icon in the **SECURITY column**.

<div align="left"><figure><img src="../.gitbook/assets/image (237).png" alt="" width="563"><figcaption></figcaption></figure></div>





b. Once the VEX configuration panel (REVIEW) is activated, you can configure and edit the settings.&#x20;

* **Default**: Affected
  * When a CVE is detected, it is set to "Affected" by default.
* **Status Options**
  * Affected: When there is an actual security impact in the current environment requiring remediation (e.g., patching, configuration changes).
  * Not Affected: When a vulnerable component is included, but there is no risk of actual exploitation due to the absence of a call path, built-in defensive logic, etc.
  * Fixed: When remediation has been completed through patching, version upgrades, etc.
  * Under Investigation: When impact analysis is still in progress.

<div align="left"><figure><img src="../.gitbook/assets/image (240).png" alt="" width="563"><figcaption></figcaption></figure></div>





c. Required Input Criteria When Setting Status to **Not Affected**

When changing the status to "Not Affected," you must enter clear justification.

* Justification (Required Selection):
  * You must select a standard reason from the dropdown list explaining why the component is judged to be unaffected (e.g., vulnerable code not executed, no execution path, inline mitigations applied).
* Additional Notes (Detailed Comments):
  * Provide detailed explanations and review comments, such as internal analysis results, evidence of non-invocation, or details of applied defensive logic.

<div align="left"><figure><img src="../.gitbook/assets/image (238).png" alt="" width="563"><figcaption></figcaption></figure></div>





#### 4. Importing VEX Settings from a Previous Project Version&#x20;

* You can load VEX review history (Status, Justification, etc.) from a previously completed verification version into the current verification and apply it in bulk to the same components and CVEs. Click the **\[Import Data from Previous Version]** button.

<div align="left"><figure><img src="../.gitbook/assets/image (241).png" alt="" width="563"><figcaption></figcaption></figure></div>







* Select the project version from which to import the VEX data.

<div align="left"><figure><img src="../.gitbook/assets/image (242).png" alt="" width="563"><figcaption></figcaption></figure></div>







* Review the precautions and click the **\[Import]** button to retrieve the data.

<div align="left"><figure><img src="../.gitbook/assets/image (243).png" alt="" width="563"><figcaption></figcaption></figure></div>







* Once the data import is successfully completed, **a notification will appear in the upper-right corner of the screen**.

<div align="left"><figure><img src="../.gitbook/assets/image (245).png" alt="" width="563"><figcaption></figcaption></figure></div>





#### 5. Including VEX Information When Exporting SBOM (Export SBOM)

* When exporting a generated SBOM file, you can extract and include the reviewed VEX (vulnerability impact analysis results) information within the file.



* **Configuration Option Descriptions:**
  * Export Type: Select the specification to export (e.g., SPDX 3.0, CycloneDX 1.6).
  * Format: Select the file format (e.g., JSON, XML, RDF, Excel).
  * VEX (Include VEX information):
    * Selecting (checking) this checkbox includes the configured VEX analysis information (Status, Justification, Notes, etc.) in the exported SBOM metadata.

<div align="left"><figure><img src="../.gitbook/assets/image (246).png" alt="" width="485"><figcaption></figcaption></figure></div>
