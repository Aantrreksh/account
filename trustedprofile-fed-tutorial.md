---

copyright:

  years: 2021

lastupdated: "2021-09-22"

keywords: trusted profile, federated users, granting access, tutorial, IAM trusted profile, trust relationship, establish trust, trust policy, trusted entity, assume access, apply access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Managing access for federated users by using trusted profiles
{: #trustedprofile-fedusers-tutorial}

This tutorial guides you through the steps to automatically grant federated users access to your account based on external identity provider specifications. By completing this tutorial, you learn how to create a trusted profile, establish trust with federated users based on attributes that are defined in your corporate user directory, and define a policy to assign access to resources.
{: shortdesc}

By using trusted profiles, you can establish a flexible, secure way for federated users to access the {{site.data.keyword.cloud}} resources they need to do their job. All federated users that share certain attributes that are defined in your corporate user directory are mapped to a common profile and can share access to {{site.data.keyword.cloud_notm}} resources. This common identity makes it possible to give the members of your organization that share access requirements automatic access to resources one time, rather than having to add each user to an account and then grant them access directly or by using access groups.

Let's say that Marla is the manager of a dev team at an airline company. The team is planning to run a new chatbot app for their HR website on an {{site.data.keyword.containerlong_notm}} cluster. Marla wants the team to have access to IAM-enabled services in test environments so developers can do their daily work. Marla also wants to make sure that the team isn't unintentionally doing operations work in production environments. In this case, Marla would create two trusted profiles: one called `Chatbot Dev (test)` and one called `Chatbot Ops (prod)`. Marla manages many developers and it usually takes significant time out of her day to assign access to team members individually. With trusted profiles, Marla can automatically grant federated users access to the resources they need without having to invite them to an account and assign access one at a time. This tutorial uses fictitious identity provider attributes that might be different from your corporate user directory. 

## Before you begin
{: #trusted-profile-federated-prereqs}

* Make sure you're assigned the following access: 
   * Administrator role in the account to create a trusted profile
   * Administrator role on the specific resources to which you are assigning access
* Enable authentication from an external identity provider. For more information, see [Enabling authentication from an external identity provider](/docs/account?topic=account-idp-integration).
* Create an instance of the following services and add them to a resource group for this tutorial.
   * {{site.data.keyword.containerlong_notm}}
   * {{site.data.keyword.toneanalyzerfull}}

## Create a trusted profile
{: #trusted-profile-federated-create}
{: step}

First, Marla creates the trusted profile for the test environment:

1. Go to **Manage** > **Access (IAM)** in the {{site.data.keyword.cloud_notm}} console, and select **Trusted profiles**.
2. Click **Create profile**.
3. Name the profile `Chatbot Dev (test)`.
4. In the description, list the level of access you want to assign to the profile. The description helps your team quickly identify different profiles from the list of trusted profiles. In this case:
   1. Platform: Viewer
   2. Services: Reader
5. Click **Continue**.

## Establish trust with federated users 
{: #trusted-profile-federated-trust}
{: step}

Now that Marla created a trusted profile, she wants to establish criteria for the federated users that can apply this profile. To do this, she creates conditions based on the attributes in her company's corporate user directory. Marla and half of the team members are based in the Ireland, and the other half are based in the United States. 

1. For trusted entity type, select **Federated users**.
2. For authentication method, select **Users federated by [{{site.data.keyword.cloud_notm}} App ID** from the list.
2. Select the default identity provider (IdP) URL associated with the identity provider you created.
3. Click **View your identity provider (IdP) data**. Marla uses this in the following steps to see which attributes she can leverage to create conditions.
5. Click **Add a condition**.
6. Click **Filter attributes** and select `country`.
    * These are the attributes available from personal data.
7. Set **Qualifier** to `Equals`.
8. For the **Value**, click **Add manually** and enter `us`.

    This way, Marla can enter attribute values that she isn't assigned in the personal identity provider data.
    {: note}

9. Click **Add a condition** and repeat steps 6-8. Instead of `us`, enter `ire`.
10. Click **Add a condition** again and click **Add manually**. 
    1. Let's say there's an attribute that is called `team` in the corporate user directory that identifies an employee's team by manager. Enter the condition `team` equals `marla`.
11. Click **Add a condition** again and click **Add manually**. 
    1. Let's say there's an attribute that is called `job-role` in the corporate user directory that identifies an employee's job role. Enter the condition `job-role` equals `dev`.
13. Set the session duration to 8 hours.
12. Click **Continue**.

## Assign access
{: #trusted-profile-federated-access}
{: step}

Marla created narrow conditions that authenticate only the developers on the team that are working in the chatbot test environment. Now she can create a policy to give them the [{{site.data.keyword.cloud_notm}} service and platform access they need for the project. 

1. Select **IAM services**.
2. Select **{{site.data.keyword.containershort}}** from the list of services. 
3. Scope the access to the option **Resources based on selected attributes**. 
4. Select **Resource group**. Marla can select or input the name of the resource group that's created for the chatbot project.
5. Select Viewer and Reader roles to define the scope of access, and click **Add**.
6. Select **{{site.data.keyword.toneanalyzerfull}}** from the list of services. 
7. Scope the access to the option **Resources based on selected attributes**. 
9. Select **Resource group**. Marla can select or input the name of the resource group that's created for the chatbot project.
10. Select Viewer and Reader roles to define the scope of access, and click **Add**.
11. Review the profile summary and click **Create**.  

## Next steps
{: #iam-federated-next}

Now that you learned the basics of how to create a trusted profile, you can create the `Chatbot Ops (prod)` trusted profile that gives employees who need broader privileges more access. To do so, repeat step 1. In step 2.11.1, enter the condition `job-role` equals `dev-lead`. Assign this profile Editor and Writer access. For more information, see [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile&interface=ui).
