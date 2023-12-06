---

copyright:
  years: 2023
lastupdated: "2023-12-06"
keywords: access policy, access, policy, restriction, resource attribute, conditions

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Limiting access with resource attribute-based conditions
{: #iam-resource-based}

When using a policy with resource attribute-based conditions, you can avoid creating multiple access policies to meet your access needs. Instead, you can create a single policy by using the combination of `OR`/`AND` conditions that are applied on resource attributes with literal or wildcard values. For example, with resource attribute-based conditions, you can create a single policy that allows access based on `Service instance: abc`, **OR** `attribute-1: xyz`, **OR** **(**`attribute-2: def` **AND** `attribute-3: hij`**)**.
{: shortdesc}

You must have a minimum of 2 conditions to use `OR`/`AND` and resource attribute-based conditions. If you need to add a single condition, see [Assigning access to resources in the console](/docs/account?topic=account-assign-access-resources&interface=ui#access-resources-console) and add the condition after selecting **Specific resources**.
{: note}

## Condition patterns
{: #attribute-condition-patterns}

The following patterns represent the allowed condition permutations:

| Pattern | Example |
|---------|---------|
| `attribute-based-condition:resource:literal-and-wildcard` |	Conditions based on resource attributes with literal or wildcard values (based on the operator used) |
{: caption="Table 1. Allowed condition patterns for resource attribute-based conditions." caption-side="top"}

## Before you begin
{: #before-you-begin-resource-based-api}
{: api}

Make sure that you call the `v2/policies` URI, which is `https://iam.coud.ibm.com/v2/policies`, so that you can use conditions in your access policies. For more information, see the [IAM Policy Management API](/apidocs/iam-policy-management) and [change log](/docs/account?topic=account-api-change-log).

## Creating resource attribute-based conditions
{: #create-resource-attribute-conditio-api}
{: api}

You can assign access with a resource attribute-based condition by specifying a prefix, delimiter, or path that determines when the condition grants access. For example, you might have a user that needs to present a demonstration on your account by using specific resources.

THe following examples show you how to create a resource attribute-based condition. In the `v2` policy with the `rule`, a user is given access to everything under the `dev/David/` folder and any path that begins with the `devA` or specifically `devA/` folder.

For more information and examples about available operators, see [Resource attribute-based conditions](/docs/account?topic=account-iam-condition-properties&interface=ui#resource-based-conditions).

You can have up to 10 conditions and nesting up to 2 levels by using `OR`.
{: important}

```json
"pattern": "attribute-based-condition:resource:literal-and-wildcard",
"rule": {
    "operator": "or",
    "conditions": [
      {
        "key": "{{resource.attributes.prefix}}",
        "operator": "stringMatchAnyOf",
        "value": [
          "dev/David/*",
          "devA*"
        ]
      },
      {
        "key": "{{resource.attributes.path}}",
        "operator": "stringMatchAnyOf",
        "value": [
          "dev/David/*",
          "devA/*"
        ]
      },
      {
        "operator": "and",
        "conditions": [
          {
            "key": "{{resource.attributes.prefix}}",
            "operator": "stringMatchAnyOf",
            "value": [
              "dev/David/*",
              "devA/*"
            ]
          },
          {
            "key": "{{resource.attributes.delimiter}}",
            "operator": "stringEquals",
            "value": "/"
          }
        ]
      }
    ]
  }
```

## Creating a resource attribute-based condition
{: #create-resource-attribute-condition}
{: ui}

You can assign access with a resource attribute-based condition such as a prefix, delimiter, or path that determines when the condition grants access. For example, you might have a user that needs to present a demonstration in your account by using specific resources.

You can have up to 10 conditions and nesting up to 2 levels by using `OR`.
{: important}

Complete the following steps to assign an access policy with an attribute resource-based condition:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**
1. Select **Users**, **Trusted profiles**, **Service IDs**, or **Access groups**, depending on the entity to which you want to assign access.
1. Click the entity's name from the list and go to **Access**.
1. Click **Assign access**.
1. Select a service, and click **Next**.
   Not all services support resource attribute-based conditions. To continue, select a service that supports resource attribute-based conditions. For example, **Cloud Object Storage**.
   {: important}

1. Select the resource that you want to assign the user access to, or select **All resources**. Click **Next**.
1. (Optional) Select a resource group access role. Click **Next**.
1. Select any combination of service access and platform access roles, and click **Next**.
1. Click **Add condition** and select **Advanced condition builder** > **Next**.
1. Add the resource conditions and click **Create**.

As an example, let's say that you're creating a conditional policy for a developer that needs access to everything under the `dev/David/` and the `dev/Secret/` folders OR any path that begins with the `devOps/` or `cicd/`. In this case, select **Prefix**, **string matches any of**, and add `dev/David/*` and `dev/Secret/`. Then, add an OR condition and select **Path**, **string matches any of**, and add `devOps/` and `cicd/*`.
{: tip}

1. Click **Create**> **Review** > **Add** to add your access configuration to your access summary.
1. Click **Assign**.

For more information about resource-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#resource-based-conditions).

