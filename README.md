# authentication-and-authorisation-with-expressjs
**Evaluating the Requirement: “This delete user functionality can be done after authentication”**
Is it a good or bad idea?

Bad Idea: Allowing deletion of users solely based on authentication without any further authorization checks is generally a bad idea. Here’s why:
Potential for Abuse:

Authenticated Users Aren’t Always Privileged Users: Authentication only confirms the identity of a user but doesn’t ensure they have the right to perform sensitive actions like deleting users. For example, a regular user should not be able to delete another user, especially not an admin or other critical accounts.
Havoc Scenario: As the challenge hints at a scenario where "every user can cause havoc," this setup could lead to chaos. A simple authenticated user could delete critical accounts, leading to severe security risks and data loss.
Lack of Authorization:

Need for Role-Based Access Control (RBAC): Proper systems should implement authorization mechanisms to ensure only users with specific roles or permissions (e.g., admins) can delete other users. This ensures that powerful actions are restricted to those with the authority to perform them.
Security Risks:

Insider Threats: Even trusted users could misuse their access if proper authorization controls are not in place.
Accidental Deletion: A user might accidentally delete accounts if they have unnecessary privileges, leading to unintentional data loss.
