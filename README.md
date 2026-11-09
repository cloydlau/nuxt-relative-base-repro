# Nuxt 4 static relative base URL reproduction

```sh
pnpm install --frozen-lockfile
NUXT_APP_BASE_URL=./ pnpm generate
cat .output/public/index.html
```

With Nuxt 4.6.4, the generated `index.html`, `200.html`, and `404.html`
contain only `"Redirecting..."`. The expected output is HTML with a
`./_nuxt/` script URL.

To compare, run `NUXT_APP_BASE_URL=/ pnpm generate` and inspect the same files.
