# Enterprise Identity & Access Management (IAM) Lab

**Microsoft Entra ID | SAML SSO | MFA | User Management**

## Project Overview

I created this project to get hands-on experience with Identity and Access Management (IAM) and learn more about the work that IAM analysts do on a daily basis.

For this lab, I set up a fictional company called **DTS Technologies** using Microsoft Entra ID. I created eight employee accounts across four departments: HR, Finance, IT, and Sales.

Throughout the project, I practiced managing employee accounts, creating security groups, assigning application access, and setting up Single Sign-On (SSO) and multifactor authentication (MFA).

I also tested what happens when someone tries to access an application they aren't authorized to use. After that, I simulated an employee transferring departments and another employee leaving the company to practice updating and removing access.

My goal with this project was to get more comfortable using Microsoft Entra ID and better understand how companies manage employee identities and protect their applications.

## Technologies Used

- Microsoft Entra ID
- Microsoft Azure Portal
- Microsoft Entra SAML Toolkit
- SAML 2.0
- Microsoft Authenticator
- Microsoft Entra Sign-in Logs
- Microsoft Entra Audit Logs

## Lab Environment

| Component | Setup |
|---|---|
| Company | DTS Technologies (fictional) |
| Identity platform | Microsoft Entra ID Free |
| Employee accounts | 8 |
| Security groups | 4 |
| Departments | HR, Finance, IT, Sales |
| Authentication | SAML SSO and Microsoft Authenticator |

## What I Worked On

### 1. User and Group Management

- Created eight fictional employee accounts in Microsoft Entra ID.
- Added employee information such as job titles, departments, and employee IDs.
- Created separate security groups for HR, Finance, IT, and Sales.
- Assigned employees to their appropriate departmental groups.
- **Security Groups Created**

This screenshot shows the four security groups I created in Microsoft Entra ID to organize employees by department.

![Security Groups](screenshots/01-security-groups.png)

**Employee Account Creation**

This screenshot shows an employee account I created in Microsoft Entra ID. I added their job title, department, company name, and employee ID to simulate onboarding a new employee.

![Sarah Miller Employee Account](screenshots/user-details-sarah-miller.png)

**HR Security Group Membership**

I added Sarah Miller and John Carter to the HR security group to practice organizing employees by department. This screenshot shows their original group memberships before I transferred John to Finance later in the lab.

![HR Group Members](screenshots/hr-group-members.png)

### 2. Application Access Management

- Created a test enterprise application called DTS Finance Portal.
- Assigned Finance employees to the application.
- Configured the application to require users to be assigned before signing in.

### 3. Single Sign-On (SSO) and MFA

- Set up SAML SSO using the Microsoft Entra SAML Toolkit.
- Configured the SAML URLs, signing certificate, and NameID attribute.
- Registered Microsoft Authenticator for a test employee.
- Successfully tested signing in through Microsoft Entra ID.

### 4. Access Control Testing

- Tested signing in with an employee who was assigned to the SAML Toolkit.
- Attempted to sign in with an employee who wasn't assigned.
- Confirmed Microsoft Entra blocked the unassigned employee with error **AADSTS50105**.
- Reviewed sign-in logs to verify the authentication results.

### 5. Employee Lifecycle Management

- Simulated an employee transferring from HR to Finance.
- Updated their department, job title, and security group memberships.
- Simulated an employee leaving the company.
- Disabled their account, revoked sign-in sessions, and removed group access.
- Reviewed audit logs to confirm the changes were recorded.

## What I Learned

This project helped me better understand how IAM works beyond just learning the concepts in class.

I got experience working directly in Microsoft Entra ID and saw how user accounts, security groups, application assignments, and authentication all work together.

One of the most useful parts was testing SAML SSO and seeing the difference between a user successfully signing in and another user being denied access because they didn't have permission.

I also learned why it's important to remove old access when employees change roles or leave a company.

Overall, this lab gave me a better understanding of the responsibilities of an IAM analyst and helped me build practical skills I can continue developing in future projects.

---

*This is a personal learning project. DTS Technologies and its employee accounts are fictional.*
