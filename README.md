# Google Workspace Home

Public informational pages for Michael Kory Wilson's private Google Workspace integrations.

- `index.html`: integration description
- `privacy.html`: privacy policy

GitHub Pages serves these plain HTML files from the root of `main`. No custom build workflow, backend, analytics or credentials are required. The separate operational `google-workspace` repository remains private.

Do not add OAuth JSON files, tokens, private configuration, backup contents or infrastructure inventories to this repository.

## Google domain verification

Google's OAuth domain-verification remediation guide explicitly requires a DNS-level **Domain property**, rather than a URL-prefix property, verified through a project owner's Google account:
https://support.google.com/cloud/answer/13804266

A github.io Pages URL can host the informational pages, but control of this repository does not provide DNS control over github.io. Do not treat a Search Console HTML-tag verification of the Pages URL as proof that OAuth domain verification is satisfied.

If OAuth domain verification is required, attach an operator-owned custom domain/subdomain to GitHub Pages, verify the root domain in Search Console via DNS, and configure the corresponding authorized domain and page URLs in Google Auth Platform. No tunnel or self-hosted server is needed. No custom domain or DNS change has been made here.

Personal-use exceptions to app verification and the console's production-publishing requirements are distinct; hosting these pages alone does not establish Google approval:
https://developers.google.com/identity/protocols/oauth2/production-readiness/brand-verification#personal-use
