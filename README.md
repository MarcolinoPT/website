# Marco's website

A personal website built with [Hugo](https://gohugo.io/) and deployed through Azure Static Web Apps.

## Run locally

1. Install Hugo Extended (the build workflow currently pins Hugo `0.147.9`).
2. Clone this repository.
3. Initialise the existing theme submodule while it remains in the repository:

   ```sh
   git submodule update --init --recursive
   ```

4. Start the local server:

   ```sh
   hugo server
   ```

5. Create a production-style build:

   ```sh
   hugo --gc --minify --destination public
   ```

The site's custom layouts and stylesheet live in `layouts/` and `static/css/site.css`. The previous theme submodule is intentionally retained during the redesign so it can be removed only after the new site has been validated.

## Deployment

Changes should be made on a feature branch and reviewed through a pull request. The Hugo build workflow validates the generated site; the existing Azure Static Web Apps workflow remains in place for deployment and pull-request previews.
