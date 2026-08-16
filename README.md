# JPC Systems Ltd website

Static single-page company website for [jpcsystems.co.uk](https://jpcsystems.co.uk), hosted on GitHub Pages.

No build step and no dependencies: `index.html`, `styles.css` and `favicon.svg` are served as-is.

## Local preview

```sh
python3 -m http.server 8000
```

Then open <http://127.0.0.1:8000/>.

## Deployment

GitHub Pages publishes the root of the `main` branch. Pushing to `main` deploys.

`CNAME` sets `jpcsystems.co.uk` as the canonical custom domain. GitHub Pages redirects `www` to the apex domain when both sets of DNS records are present.

The required web DNS records are:

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `megakid.github.io` |

Mail-related MX and TXT records are independent of GitHub Pages and must be preserved when web DNS is changed.

GitHub issues the TLS certificate automatically once those records resolve, after which "Enforce HTTPS" can be enabled in the repository's Pages settings.

## Content

Company facts on the page (company number, VAT number, registered office) are hard-coded in `index.html`. Update them there if they change at Companies House or HMRC.
