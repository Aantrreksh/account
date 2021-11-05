---

copyright:

  years: 2021

lastupdated: "2021-11-05"

keywords: trusted profile, compute resource, granting access, tutorial, IAM trusted profile, trust relationship, establish trust, trust policy, trusted entity, assume access, apply access

subcollection: account
content-type: tutorial
account-plan: lite 
completion-time: 15m
services: containers

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
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}
{:step-next: data-tutorial-type='step-next'}

# Managing access for apps in compute resources
{: #trustedprofile-compute-tutorial}
{: toc-content-type="tutorial"} 
{: toc-completion-time="15m"}

This tutorial guides you through the steps to centrally manage fine-grained authorization for all applications that are running in a compute resource without creating service IDs or managing the API key lifecycle for applications. By completing this tutorial, you learn how to create a trusted profile, establish trust with compute resources based on specific attributes, and define a policy to assign access to resources.
{: shortdesc}

By using trusted profiles, you can establish a flexible, secure way for apps that are running on a compute resource to access other {{site.data.keyword.cloud}} resources. All compute resource instances that share certain attributes, such as name, namespace, tags, or location, are mapped to a common profile and can share access to {{site.data.keyword.cloud_notm}} resources. This common identity makes it possible to give the applications within various compute resources access to an external resource one time, rather than cluster-by-cluster.

You must enable the "Service Account Token Volume Projection" on the Kubernetes cluster to apply the trusted profile identity. For more information, see [Authorizing pods in your cluster to IBM Cloud services with IAM trusted profiles](/docs/containers?topic=containers-pod-iam-identity&interface=ui)
{: note}

Let's say that you are the lead developer on a project for your team that is planning to run a new chatbot app on an {{site.data.keyword.containerfull}} cluster. You want the app to have access to IAM-enabled services but without storing credentials in the code. Your manager has given you an administrator access in the account to create trusted profiles and give your runtime environments access to the resources you need to build the chatbot app.

## Before you begin
{: #trusted-profile-compute-prereqs}

* This tutorial might incur costs. Use the [Cost Estimator](/estimator/review) to generate a cost estimate based on your projected usage.
* Make sure you have the following access:
   * Administrator role in the account to create a trusted profile
   * Administrator role on the specific resources to which you are assigning access
* Create a cluster that runs {{site.data.keyword.containerlong_notm}} Version 1.21 or later. For information about creating a cluster, see [Getting started with IBM Cloud Kubernetes Service](/docs/containers?topic=containers-getting-started).

## Create a trusted profile
{: #trusted-profile-compute-create}
{: step}

First, create your trusted profile:

1. Go to **Manage** > **Access (IAM)** in the {{site.data.keyword.cloud_notm}} console, and select **Trusted profiles**.
2. Click **Create profile**.
3. Name the profile `Chatbot Project`.
4. In the description, list the level of access you want to assign to the profile. This helps you quickly identify different profiles from the list of trusted profiles. In this case:
   1. Writer 
   2. Manager
5. Click **Continue**.

Make sure that your profile name is short and human readable. For compute resources, the name of the profile is required to get the compute resource token, so a simple name is easier for developers to use in the program.
{: note}

## Establish trust with the Kubernetes cluster 
{: #trusted-profile-compute-trust}
{: step}

Now that you created your trusted profile, you want to establish trust with the Kubernetes cluster you created for the project:

1. For trust entity type, select **Compute resources**.
2. For compute service, select **Kubernetes** from the list.
3. Select **Specific resources** to establish trust with one or more existing compute resource instances.
4. Click **Add another resource**.
5. Select the cluster that you created for this tutorial. 
6. Enter the value `default` in the namespace and service account fields. 

   A service account in {{site.data.keyword.containerlong_notm}} is identified by the namespace and service account name. For more information, see [Kubernetes service account token volume projection](https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/#service-account-token-volume-projection){: external} and [Kubernetes namespace](https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/){: external}. 
   {: note}

7. Click **Continue**.

## Assign access to other {{site.data.keyword.cloud_notm}} services
{: #trusted-profile-compute-access}
{: step}

Now, you can create an access policy to give your compute resource instance access to other IBM Cloud services you need for your team's chatbot project. 

1. Select **IAM services**.
2. Select **Watson Assistant** from the list of services. Make sure you have access on the service you want to give access to in this profile.
3. Scope the access to the option **Resources based on selected attributes**. 
4. Select **Service Instance** and input the service instance name to give permission to a specific instance.
5. Select Writer and Manager roles to define the scope of access, and click **Add**.
6. Review the profile summary and click **Create**.  

## Next steps
{: #iam-compute-next}

Now that you learned the basics of how to create a trusted profile, you can continue to establish trust with additional compute resources. For more information, see [Updating trusted profiles](/docs/account?topic=account-trusted-profile-update).
