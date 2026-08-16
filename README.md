# JPC Systems Ltd website

Static company website for [jpcsystems.co.uk](https://www.jpcsystems.co.uk), hosted by GitHub Pages.

## Local preview

```sh
python3 -m http.server 8000
```

Then open <http://127.0.0.1:8000/>.

## Deployment

GitHub Pages publishes the root of the `main` branch. The `CNAME` file configures `www.jpcsystems.co.uk` as the canonical custom domain. GitHub Pages redirects the apex domain to `www` when both sets of DNS records are present.

The required web DNS records are:

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `megakid.github.io` |

Mail-related MX and TXT records are independent of GitHub Pages and must be preserved when web DNS is changed.
