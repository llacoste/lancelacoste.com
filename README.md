# lancelacoste.com

Temporary professional landing page for Lance Lacoste while a fuller personal
site is developed. The site is plain HTML, CSS, and minimal JavaScript,
published from the repository root through GitHub Pages.

## Local Preview

From the repository directory, serve the static files with Python:

```bash
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000) in a browser.

## Deployment

The GitHub Actions workflow in `.github/workflows/deploy.yml` deploys the
repository root when commits are pushed to `main`.

For initial configuration:

1. Open the repository's **Settings** -> **Pages**.
2. Under **Build and deployment**, choose **GitHub Actions** as the source.
3. Under **Custom domain**, enter `lancelacoste.com` and save.
4. Push to `main` or manually run the **Deploy static site to Pages** workflow.
5. After DNS is active and GitHub issues a certificate, enable **Enforce HTTPS**.

The repository includes `CNAME` to record the intended custom domain. For a
custom Actions Pages deployment, the domain must also be configured in the
repository Pages settings.

## Namecheap DNS Setup

In Namecheap, open **Domain List** -> **Manage** for `lancelacoste.com` ->
**Advanced DNS** -> **Host Records**. In Namecheap, host `@` means the apex
domain (`lancelacoste.com`).

Add these records:

| Type | Host | Value | TTL |
| --- | --- | --- | --- |
| A Record | `@` | `185.199.108.153` | Automatic |
| A Record | `@` | `185.199.109.153` | Automatic |
| A Record | `@` | `185.199.110.153` | Automatic |
| A Record | `@` | `185.199.111.153` | Automatic |
| CNAME Record | `www` | `llacoste.github.io` | Automatic |

Remove conflicting `A`, `CNAME`, or URL redirect records for `@` and `www`.
Do not remove MX, TXT, DKIM, DMARC, or other records used for Proton Mail.

GitHub also recommends verifying the custom domain. In GitHub, open account
**Settings** -> **Pages**, add `lancelacoste.com` as a verified domain, then
add the TXT record GitHub provides in Namecheap before completing verification.

DNS changes commonly begin resolving within 30 minutes, but HTTPS certificate
provisioning can take longer.

## Content Updates

- Email is set to `lance.lacoste@proton.me`.
- Replace the placeholder LinkedIn profile URL in `index.html` once confirmed.
- Replace the temporary landing page files in place when the full portfolio is
  ready; the Pages workflow and domain configuration can remain unchanged.
