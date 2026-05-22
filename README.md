# Shinylive-test


First test with {shinylive}. This demo app is the result of a workshop on shiny, details here: [A Shiny start](https://github.com/JoachimGoedhart/A_Shiny_start)

### Code to test locally

To test whether conversion works from the app.R to a shinylive app:
- First set working directory to 'To Source File Location'
- run `shinylive::export(".", "site")`

This will create a site that can be run locally by typing: `httpuv::runStaticServer("site")`

### Workflow to deploy

To deploy the shinylive app on github pages:
- make the app available as repo.
- make a folder `.github/workflows` that contains the `deploy-app.yaml` (this file contains the instructions for github actions to convert the app.R file into a site that can be hosted on github pages). This can be done in the RStudio IDE when the working directory is set to the folder that contains app.R and using this command: `usethis::use_github_action(url="https://github.com/posit-dev/r-shinylive/blob/actions-v1/examples/deploy-app.yaml")`
-  On the github repo page choose navigate to "Settings -> Pages" and choose under "Build and deployment" source: Github actions
-  Navigate to "Actions" and start the workflow "Deploy app to gh-pages"
-  If successful you can navigate to deployments to find the link to the page, or go to the About section and navigate to settings. Select the checkbox `Use your GitHub Pages website` to add a link to the app.

To see the app in action use this link [https://joachimgoedhart.github.io/Shinylive-test/](https://joachimgoedhart.github.io/Shinylive-test/)
