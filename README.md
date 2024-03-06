# hugo-mock-landing-page-autodeployed -> Spotify Landing Page
Melanie Chen (chenmel 21042266)

I automated the deployment of a Hugo Website (hugo-mock-landing-page)

I imported my hugo-mock-landing-page repository as hugo-mock-landing-page-autodeployed and then adjusted the baseURL in the config.toml file. Then I reconfigured the repository settings and added a GitHub Actions Workflow to automate the deployment.

The added GitHub Actions workflow is designed to automatically build and deploy a Hugo-based website to GitHub Pages whenever changes are pushed to the main branch of the repository. It works by performing the following steps:

The workflow is triggered by a push event on the main branch.
It checks out the repository code, including submodules (like Hugo themes) and fetches the entire commit history.
It sets up the Hugo environment by installing a specific version of Hugo with extended functionality.
It compiles the static files for the website using the hugo command with draft content included, garbage collection enabled, and HTML/CSS/JS minification.
Finally, it publishes the compiled static files to the gh-pages branch, which is used by GitHub Pages to serve the website.

Finally, I double checked that the deployment of the website was working properly by editing content/contact.md.

You can access the published site at: https://melaniechen912.github.io/hugo-mock-landing-page-autodeployed/contact/
