# cvoya-com.github.io

The root of <https://oss.cvoya.com/> redirects to the canonical
[CVOYA software catalog](https://cvoya.com/software).

It is a static redirect in `index.html`; the catalog itself lives in the
[`cvoya-com/web`](https://github.com/cvoya-com/web) repository. GitHub Pages serves `main` at the
repository root, so a merge to `main` is a deploy.

The `CNAME` file binds the organization Pages domain to `oss.cvoya.com`. Do not delete it:
project Pages sites, including the CVOYA Graph documentation under `/graph/`, depend on that domain.

## Local development

```bash
npx http-server . -p 8765 -c-1     # then open http://localhost:8765/
```

## Validation

CI runs the same two checks on every push and pull request. Run them locally before pushing:

```bash
npm install
npm run validate                   # html-validate + stylelint
```

Both are bugs-only rulesets — structural HTML errors and real CSS faults, not formatting.

## Conventions

- Keep the root a redirect. Do not duplicate the software catalog here.
- Do not remove `CNAME`; project Pages sites rely on the custom organization domain.
- `.nojekyll` is deliberate — it stops Pages running the files through Jekyll.
