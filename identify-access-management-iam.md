# Identify Access Management \(IAM\)

## Tick off five marks on Security Status:

1. Delete root access keys

    ○ We can skip this as a new user

2. Enable MFA \(multi-factor authentication\)

    ○ Set up MFA with Google Authenticator

3. Create individual IAM users:
   * Access types:
     * Programmatic access: Access via command line
     * AWS Management Console access: Login to AWS console and make changes
     * AWS Software Development Kit \(SDK\) access:
4. Create IAM groups

    ○ Once you decide access, you need to add to a Group

    ○ Choose a policy access type \(or multiple types\) and add the group name

5. IAM password policy

    ○ A password policy is a set of rules that define the type of password an IAM user can set

    ○ Change upper/lowercase required, number required, min password length, etc.

## Policies

* How to define permissions to users, groups, role.
* You can click on a policy to get details about what it gives people access to
* Detailed JSON allows you to define a statement comprised of an effect \(Allow, Disallow\), Action \(what will happen\), and Resource \(to what resource\)

## Exam Tips 

3 ways to access AWS platform: 

1. Via AWS Console 
2.  Programmatically using command line 
3. Using Software Development Kit \(SDK\) 

**Root account** 

* Account = Email address you registered with
* Full admin access
* Should never give away
* Instead, create a user for each individual in your organization and secure root account with MFA 

**User Account**

* No privileges from the start. 
* Use least privilege model Groups
* Place to store your users
* Users will inherit all permissions that group has
* To set permissions for a group, need to set policies for that group using JSON

**Groups**

* Place to store your users
* Users will inherit all permissions that group has
* To set permissions for a group, need to set policies for that group using JSON

