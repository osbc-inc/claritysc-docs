---
slug: "/manager-guide/product-management"
sidebar_label: "Product Management"
sidebar_position: 4
description: "This section explains the product management functions and how to use them."
---
# Product Management {#product-management}

<p class="doc-lead">This section explains the product management functions and how to use them.</p>

#### 1.   Product Function Overview {#1-product-function-overview}

* Individual projects are integrated and managed at the product level, allowing you to check project statistics for each product provided by the dashboard.

※ The **Product Management** menu will be deactivated if the user does not have Manager, Product Creator, or Product Manager **roles**. For detailed information on assigning permissions, please refer to the [\[How to Set Product Roles\]](./user-role-management.md) section.

#### 2. Product Creator Permissions {#2-product-creator-permissions}

**2.1. Creating a New Product**

* Log in with an account that has Product Creator or Manager permissions.
* Click the **\[Add New Product]** button in the Product Management menu on the left to create a new product.

![](/img/clarity-sc-en/image-109.png)

1. Select the required values: **Product Name** and **Product Manager**.
2. Only accounts with **Product Manager permissions** will be displayed in the Product Manager list.

![](/img/clarity-sc-en/image-198.png)

* **Product Name**: Enter the name of the new product to be registered.
* **Product Manage**r: Select the administrator in charge of the product. The selected user will have product management permissions.
* **Applied Model**: Enter the model or product type applied to the product (e.g., Service Model, Deployment Model, etc.).
* **Usage Scope**: Enter the usage scope or purpose of the product (e.g., Internal Use, External Distribution, etc.).
* **Inspection Date**: Select the scheduled inspection date for the product.
* **Release Date**: Select the scheduled release date for the product.
* **Development Department**: Select the department that developed the product.
* **Main Contact**: Enter the contact information for the main person in charge of the product.

**1.2. Editing Product Information**

You can click the **\[Edit Information]** button to change the Product Manager and modify product information.

**1.3. Cloning a Product**

Click the **\[Clone Product]** button to clone the product.

![](/img/clarity-sc-en/image-199.png)

![](/img/clarity-sc-en/image-200.png)

* A new product is created by copying the existing product's groups and project list as they are.

![](/img/clarity-sc-en/image-127.png)

***

#### 3. Product Manager Permissions {#3-product-manager-permissions}

**3.1. Creating a New Project from a Product**

Click the \[Add New Project] button on the product details page.

![](/img/clarity-sc-en/image-201.png)

* Enter the required values marked in red, and assign a Project Manager for this project. (Only accounts with Project Manager permissions will be displayed)
* The Product Name will be locked to the current product.

![](/img/clarity-sc-en/image-202.png)

* A new project is added, and clicking on it redirects you to the project details page.

![](/img/clarity-sc-en/image-203.png)

![](/img/clarity-sc-en/image-204.png)

**3.2. Assigning a Project to a Product**

* Click the \[Assign Project] button and select the project you want to add.

![](/img/clarity-sc-en/image-205.png)

1. When you select a project from the project list, a list of all versions for which verification has been completed within that project will be displayed.
2. Only versions that are in the "Ready" stage, indicating completed verification, will be displayed.
3. Selected projects will be marked with a checkbox.

![](/img/clarity-sc-en/image-206.png)

* The added project is automatically included in the Default Group.

![](/img/clarity-sc-en/image-207.png)

**3.3. Adding and Managing Product Groups**

* Click \[Add New Group] to add a new group.

![](/img/clarity-sc-en/image-208.png)

* Enter a group name and select a color to complete creating the group.

![](/img/clarity-sc-en/image-209.png)

* You can assign projects from the Default Group to any group by simply dragging and dropping them.

![](/img/clarity-sc-en/image-210.png)

**3.4. Exporting the Entire Product**

* Click the \[Merged Product Components] button at the top to display a list of all components from the projects included in that product, and download them in your preferred SBOM format.

![](/img/clarity-sc-en/image-211.png)

* 해당 프로덕트의 프로젝트에 포함된 컴포넌트를 목록을 확인할 수 있습니다. \[Export] 버튼을 클릭해서SBOM 포맷을 선택해서 다운로드할 수 있습니다.

![](/img/clarity-sc-en/image-212.png)

**3.5. Exporting by Product Group**

* Click the \[Merged Group Component] button to display the integrated component list of the projects included in the selected group. You can then click the \[Export] button to select an SBOM format and download it.

![](/img/clarity-sc-en/image-213.png)
