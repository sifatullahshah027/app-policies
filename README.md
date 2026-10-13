# app-policies

Privacy policies for our iOS and Android apps, published with GitHub Pages at
**https://sifatullahshah027.github.io/app-policies/**.

Each app has its own directory, and its policy URL is the one entered in App
Store Connect, the Play Console and the app itself:

| App | Policy URL |
| --- | --- |
| Perfin | https://sifatullahshah027.github.io/app-policies/perfin/privacy-policy.html |

**Never rename or move a published file.** The URL is set in both store
listings and compiled into shipped builds, so a moved page breaks it in every
installed copy.

## Layout

```
index.html                 lists every app
assets/policy.css          shared styles (light and dark)
<app>/privacy-policy.html  that app's policy, covering both stores
<app>/support.html         support page: contact, cancelling, restoring
<app>/index.html           redirects to the policy
.nojekyll                  serve files as-is, without Jekyll
```

## Naming

Policies name **the app** and refer to its maker as **"we, the developer"**.
They never name the store account (AppsFirst Studio) or any company, and
never Hivesoft — that name belongs only to the shared Firebase project.

## Adding an app

1. Copy `perfin/` to `<app-slug>/` (lowercase, no spaces; it becomes part of
   the URL for good).
2. Rewrite the policy against **that app's code**, not Perfin's. Check each
   section: what the app sends and to whom, which Firebase products it uses,
   which permissions it declares, what stays on the device, and any AI
   provider it uses. A policy copied without checking is a false statement
   to both stores.
3. Update the title, effective date and footer, and add a row to `index.html`
   and to the table above.
4. Keep the app's App Store privacy answers, its Play Data safety form and its
   `PrivacyInfo.xcprivacy` consistent with the page.
5. Commit and push. Pages republishes within a minute or two.

## Changing a policy

Edit the page, update its effective date, and push **before** the release
containing the change ships.

## Publishing (one-time)

GitHub → this repository → Settings → Pages → Source: *Deploy from a branch*,
branch `main`, folder `/ (root)`.
