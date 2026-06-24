# Ministry Harbor Public Placeholder Site

This repository hosts the public static placeholder website for
`ministryharbor.com`.

The private product planning and application work should remain in the private
`fridaymerge/ministry-harbor` repository. Do not add private roadmap details,
partner church details, internal planning notes, or private issue content here.

## Files

- `index.html` - public placeholder page
- `styles.css` - responsive styling
- `404.html` - static not-found page for GitHub Pages
- `CNAME` - custom domain configuration for `ministryharbor.com`
- `.nojekyll` - disables Jekyll processing for this static site
- `assets/ministry-harbor-background.jpg` - generated public hero background artwork

## GitHub Pages

Publish this repository with GitHub Pages using:

- Source: Deploy from a branch
- Branch: `main`
- Folder: `/ (root)`
- Custom domain: `ministryharbor.com`

The public GitHub Pages URL should be:

`https://fridaymerge.github.io/ministryharbor.com/`

The custom domain should resolve after DNS is configured and propagated:

`https://ministryharbor.com/`

## DNS Records Needed

DNS is not complete until these records are configured with the domain provider
and verified after propagation.

For the apex domain `ministryharbor.com`, create four `A` records:

| Host | Type | Value |
| --- | --- | --- |
| `@` | `A` | `185.199.108.153` |
| `@` | `A` | `185.199.109.153` |
| `@` | `A` | `185.199.110.153` |
| `@` | `A` | `185.199.111.153` |

Optional `www` record:

| Host | Type | Value |
| --- | --- | --- |
| `www` | `CNAME` | `fridaymerge.github.io` |

GitHub Pages can redirect between the apex and `www` domain when the custom
domain and DNS records are configured correctly.

`ministryharbor.org` can redirect to `ministryharbor.com` through the domain
provider for now. A second GitHub repository is not needed for that redirect.

Current GitHub Pages DNS documentation:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Local Preview

Open `index.html` directly in a browser, or run a simple static server from this
directory:

```sh
python3 -m http.server 8080
```
