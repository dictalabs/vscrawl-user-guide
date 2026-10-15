# vScrawl Integration Guide

This guide explains how to Integrate **vScrawl** into your website or application, so you can prepare and sign documents without leaving your app. It covers business application registration, credential generation, access token creation, and iFrame implementation.

Once a document workflow is created, the signing/preparation experience runs entirely inside your own interface.
## Register a Business Application

To use the vScrawl Integration, you must first register a **Business Application** in vScrawl.

1. Log in to your **vScrawl** account.
2. Navigate to **Organization** from the left panel, then click on **Business Apps**.
3. Click **Add App**.
4. Fill in the required fields — **Client ID**, **App Name** and **Callback URL** — and optionally a **Description**. Set **Status** to **Active**; an inactive app cannot be used to request an access token.
5. Click **Add App** again to save.

![vScrawl Signup](images/adding-new-app.png)
Once created, your application will appear in the **App List**, and a **Client secret** dialog shows the app's secret. Copy the **Client Secret** immediately and store it securely.
## Generate Client Secret

If the secret is lost or you want to replace it, generate a new one:

1. Locate your application in the **App List**.
2. Click the **three dots (options menu)**.
3. Select **Generate Secret**.

Copy the new **Client Secret** immediately and store it securely. The previous secret stops working. **Generate Secret** is not available while the app is disabled.

![vScrawl Signup](images/iframe-client-secret.png)
**Important:** The Client Secret is shown only once. If lost, you must regenerate it.

## Generate an Access Token

An **Access Token** is required to authenticate and load the vScrawl .

**API Details**

- **Method:** POST
- **Endpoint:**  
    https://api.yourdomain.com/auth/v1/signin

**Request Body (JSON)**

```json
{
  "grant_type": "CLIENT_CREDENTIALS",
  "clientId": "{{client_id}}",
  "clientSecret": "{{client_secret}}",
  "email": "{{user_email}}"
}
```

- **clientId** – the **Client ID** of your business app (not the app name).
- **email** – the email address of a member of the organization that owns the business app. The document opens for this user, so they must be the document's owner or one of its recipients.

**Response**

On success, the API returns an **access token** (`accessToken`). Save this token and use it in the URL.

## Integrate vScrawl Using an iFrame

Once you have the access token and workflow ID, Integrate the vScrawl editor in your application using an iFrame.

**Sample HTML**

```html
<!DOCTYPE html>

<html>
  <body>
    <h1>My vScrawl Integration </h1>
    <iframe
      src="https://app.yourdomain.com/client-embed?wId={{WORKFLOW_ID}}&clientToken={{ACCESS_TOKEN}}"
      width="100%"
      height="800px"
      frameborder="0"
      allow="clipboard-read; clipboard-write; fullscreen"
      title="vScrawl Document Editor">
    </iframe>
  </body>
</html>
```

**Parameters**

- **WORKFLOW_ID**: The workflow ID for the document signing process.
- **ACCESS_TOKEN**: The access token generated from the sign-in request above.

## Returning to Your Application

When the user finishes signing, declines, or closes the document, the embedded page sends them back to your app's **Callback URL**. When the document was signed or declined, `docId` and `status` (`SUCCESS` or `DECLINED`) are added to the URL. The embedded page also posts a `vscrawl:iframe-exit` message (with the full return URL in `url`) to the parent window, so your page can handle the navigation itself if the browser blocks the redirect.

## Best Security Practices

- Never expose **Client Secret** in frontend code.
- Always generate the **Access Token** from a secure backend service.
- Rotate secrets periodically.
- Use HTTPS for all API and iframe integrations.

For any issues or questions, contact the vScrawl support team.
