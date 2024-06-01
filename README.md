# hugo-mock-landing-page

This is my hugo mock landing page for a product that I came up with called "TasteCase". The product is meant to be a protable way to transport seasonings and sauces so that you can better seson your food no matter where you are. Please refer to the User Stories file to read a little bit more about the problem I was trying to solve with the product, and examine some key features and user stories. 

The site contains features on the homepage, and a contact page with my information. 


Summary of Workflow: 
This GitHub Actions workflow builds and deploys a Hugo website to GitHub Pages. It is triggered by pushes to the main branch and involves checking out the repository, setting up the Hugo environment, compiling the static files, and publishing them to the gh-pages branch. The entire commit history is fetched, and the extended Hugo version is used for improved performance and additional features. (ask Claude and ChatGPT for help) 

Extended Description of Workflow: 
This GitHub Actions workflow is designed to build and deploy a Hugo website to GitHub Pages. It is triggered whenever code is pushed to the main branch of the repository.
The workflow consists of a single job named deploy that runs on an Ubuntu 22.04 runner. The job performs the following steps:

Checks out the repository code, including submodules (e.g., Hugo themes) and fetches the entire commit history for accurate Git information and last modification dates.
Sets up the Hugo environment using version 0.123.4 with the extended features enabled for improved performance and additional functionality.
Builds the Hugo website, generating the static files with draft content included, garbage collection enabled, and HTML/CSS/JS minification applied.
Publishes the generated static files to the gh-pages branch, which is used by GitHub Pages to host the website. The publish step authenticates with GitHub using the GITHUB_TOKEN secret and configures the commit user information.

The workflow includes comments for an optional step to configure a custom domain for the GitHub Pages site, which can be uncommented if needed.
Overall, this workflow automates the process of building a Hugo website from the source code and deploying it to GitHub Pages, ensuring that the live website is always up-to-date with the latest changes pushed to the main branch.

