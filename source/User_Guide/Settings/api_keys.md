---
seo:
  title: Manage SendGrid API Keys
  description: Manage your SendGrid API Keys
  keywords: sendgrid API keys, email API Keys, mail API Keys, email credentials, send credentials
title: API Keys
weight: 0
layout: page
navigation:
  show: true
---

API Keys are used by your application, mail client, or website to authenticate access to SendGrid services. They are the preferred alternative to using a username and password because you can revoke an API key at any time without having to change your username and password. We suggest that you use API keys for connecting to all of SendGrid’s services.

There are two different types of API Keys:

2. **Billing API Keys** are used only to authenticate billing related API calls.
1. **General API Keys** are used to authenticate all other API calls.

We require that you create a separate API Key for making billing related API calls. This segmentation adds an extra level of security by giving you more control over who has access to the various areas of your account.

You may also assign an API Key specific permissions that further restrict which API calls it is capable of authenticating. For more detailed information about API Key Permissions, please visit our [Classroom]({{root_url}}/Classroom/Basics/API/api_key_permissions.html).

When viewing the API Keys page, you will see a list of your current API Keys along with the following information:

**Name** - The name you defined for your API key.

**API Key ID** - The way you would reference your API key for management through the API. (e.g. editing or deleting a key)

**Action** - Actions you can perform on your API keys, such as editing or deleting the key.

{% anchor h2 %}
Create an API Key
{% endanchor %}

When you click the “Create API Key” button, a dropdown menu will appear allowing you to choose the type of API Key you would like to create. After selecting either "General API Key" or "Billing API Key", you will be shown a page allowing you to give your new key a name and permissions.

The API Key name will follow your API key around through the SendGrid customer portal, so it is important that you choose a name that is meaningful to you. Please note that there is a limit of 100 API Keys per account.

{% warning %}
You will only be shown your API key one time. Please store it somewhere safe as we will not be able to retrieve or restore this generated token.
{% endwarning %}

{% anchor h3 %}
API Key Permissions
{% endanchor %}

During the API Key creation process, you will be given the option of selecting specific permissions, or scopes, that you would like to assign to your new API Key. These permissions restrict which areas of your account your API Key will be able to access.

When assigning permissions to your API Key, you will be given the option to select one of the following levels of access:

* **No Access** prevents the API Key from accessing any endpoint within the selected permission.
* **Read Access** allows the API Key to access GET endpoints within the selected permission.
* **Full Access** allows the API Key to access GET, PATCH, PUT, DELETE, and POST endpoints within the selected permission.

{% info %}
You may not give an API Key greater permissions than you currently have.
{% endinfo %}

After you click the “Save” button, you will be shown your API key. This key will only be shown here, so copy it down! Once you leave this page, you will not be able to see this key again.

{% anchor h2 %}
Edit an API Key
{% endanchor %}

Click the gear icon in the same row as the key you would like to edit. From here you can delete a key, making it completely inactive, or you can edit your key’s name and permissions.

{% anchor h2 %}
Inactivate an API Key
{% endanchor %}

{% warning %}
Once you delete a key, it can no longer be used to access SendGrid’s services.
{% endwarning %}

Click the gear icon in the same row as the key you want to inactivate. Choose “Delete.” This will delete the key permanently, making it inactive. Any subsequent API calls using this deleted API key will be rejected by SendGrid.

{% anchor h2 %}
Sending Email With an API Key
{% endanchor %}

You will need an API key to send email with SendGrid, we have provided [basic instructions for how to send emails with our API Keys]({{root_url}}/Classroom/Send/How_Emails_Are_Sent/api_keys.html) in case you need them.
