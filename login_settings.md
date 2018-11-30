---


copyright:

  years: 2018
lastupdated: "2018-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# Setting up login security
{: #login-settings}

With authorized access, you can set up extra security for your login. You can set security questions and answers, select a password expiration, set up time-based one-time passcode (TOTP) multifactor authentication (MFA), and set up external authentication options.  
{:shortdesc}

An account owner can require IBMid MFA on an account that you're a member of. IBMid MFA overrides any other user MFA setting. For example, when IBMid MFA is set, you're prompted for a TOTP MFA associated with your IBMid instead of security questions or one of the external authentication methods.
{: note}

You can view the following security options, and enable or disable them, only if your administrator gives you access. Go to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) > **Profile and settings**, and select **Login settings**.

## Setting up security questions
{: #security-questions}

To set up your security questions:
1. From the console, go to Go to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) > **Profile and settings**, and select **Login settings**.
2. Click **Edit**. 
3. Select the questions that you want to have and answer them. You must use three security question options.
4. Click **Save** when you're finished.  
5. To make sure the `Yes` box is checked for the security questions to be enabled. Checking the `Yes` box might prompt you to sign in to your account again.  

You can set up answers to three security questions for extra authentication at login. You must set up your security questions and answers before your administrator can enable this MFA requirement for you.

You must be the account owner or have the User-managed login setting enabled for you by your account administrator to turn security questions on and off.
{: note}

## Setting a password expiration
{: #password-expiration}

To set the length of time you would like to use your current password, select an option for your password to expire in the **Password expiration** section.

The password expiration is set to never by default. When you sign up for an account, you're never required to change your password. When you set a password expiration period, you're notified of your password expiration by email 14 days before, 7 days before, and the day the password is set to expire.

This option is available only to users that log in with a SoftLayer ID. To update your password expiration, you must be an account owner or have the User-managed login setting enabled for you by your account administrator on your IAM User details page.
{: note}

## Setting up TOTP authentication
{: #MFA}

To set up your TOTP authentication, click **Set up**. 

TOTP MFA adds an extra layer of security to your account by requiring a TOTP passcode in addition to the standard ID and password during login. You must set up your TOTP authentication before your account administrator can enable this MFA requirement for you.

You might also be prompted for a time-based one-time passcode if the user TOTP setting isn't set up and enabled. This is because an account owner might turn on IBMid MFA for an account that you have access to. This type of MFA applies to every user in the account when this setting is turned on, and you're required to use it. For more information, see [Types of multifactor authentication](/docs/iam/mfatypes.html#types).


## Setting up external authentication options
{: #third-party-MFA}

You or your account administrator can order Symantec or phone-based authentication for you for a monthly cost. For you to order external authentication, you have to have the add services infrastructure permissions. To find out if external authentication is enabled, go to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg) > **Profile and settings**, and select **Login settings**. If Phone-based MFA is disabled, click **Go to User details**. This link will take you to the same page as the steps for setting up your symantec authentication and setting up your phone-based authentication.  

### Setting up Symantec authentication

If your account administrator chooses to order Symantec identity protection, you must work with your administrator to help them complete the order by providing your credential ID:

1. Go to [Symantec VIP](https://vip.symantec.com/).
2. Click **Download**. 
3. Get your credential ID and provide the ID to your administrator to complete the order. 

After your administrator orders and enables the option, you can use the app for login authentication.

### Setting up phone-based authentication

If your account administrator chooses to order phone-based identity protection, you must set it up after your administrator orders it. Then, your administrator can enable it for you to use. After your administrator orders phone-based authentication, complete the following steps to set it up:

1. Go to **Manage** > **Access (IAM)**.
2. Click **Users**, and select your name from the list.
3. From the **User details** page in the **Manage user's login** section, click the **Edit** icon ![Edit icon](../icons/icon_write.svg) for the **Phone-based authentication** row.
4. Follow the prompts to set up your phone-based authentication.

After you have set up your phone-based authentication, the account administrator can enable the option for you to be prompted for this MFA type at login.


 

