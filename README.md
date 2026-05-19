# resume

Static HTML/CSS/JS resume site for Cal Hargis.

The site is intended to be published at:

```text
https://calhargis.github.io/resume/
```

## GitHub Pages

This repository includes a GitHub Actions Pages workflow at `.github/workflows/pages.yml`.
In the repository settings, set **Pages > Build and deployment > Source** to
**GitHub Actions**.

The `.nojekyll` file is included so GitHub Pages serves the `_astro` static asset
folder.

## Root GitHub.io redirect

The bare URL `https://calhargis.github.io/` is controlled by a separate repository
named `calhargis.github.io`. That repository is configured with this `index.html`
at its root so browsers are sent to the resume site:

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>Redirecting to Cal Hargis Resume</title>
    <link rel="canonical" href="https://calhargis.github.io/resume/" />
    <meta
      http-equiv="refresh"
      content="0; url=https://calhargis.github.io/resume/"
    />
    <script>
      window.location.replace("/resume/");
    </script>
  </head>
  <body>
    <p>
      <a href="https://calhargis.github.io/resume/"
        >Continue to the resume site</a
      >
    </p>
  </body>
</html>
```
