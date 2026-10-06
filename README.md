# Canopod documentation publishing

This repository publishes the documentation at **https://docs.canopod.com/**.
The editable content, styles, and build scripts live in
[emidhun/canopod/website](https://github.com/emidhun/canopod/tree/main/website).

## Publish

1. In **Settings → Pages**, select **GitHub Actions** as the source.
2. Open **Actions → Publish documentation → Run workflow**.
3. Leave `source_ref` as `main`, or use a reviewed Canopod commit SHA.

The workflow reads the public source repository, builds both website and documentation,
checks links and metadata across both, and publishes only the docs output here.
No cross-repository access token or backend is required.

After a documentation update in `canopod/main`, run this workflow again. The product
website has its own automatic deployment in the source repository.

## Domain

Set **Settings → Pages → Custom domain** to `docs.canopod.com` before adding the
Namecheap DNS CNAME record: host `docs`, value `emidhun.github.io`.
Enable **Enforce HTTPS** after GitHub verifies DNS and issues the certificate.

[Full domain setup and Namecheap records](https://github.com/emidhun/canopod/blob/main/website/DEPLOYMENT.md)
