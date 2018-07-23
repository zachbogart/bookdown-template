# bookdown-template

This template should allow you to setup your own bookdown book that can be published with GitHub Pages and automate rendering using Travis CI.

## Create the Book
1. **Clone this repo**
2. **Create your book**: create new .Rmd files for your new chapters and add content.
3. **Check the render**: Once finished adding content, run `bookdown::render_book("index.Rmd", "all")` to render a draft of the book. This will appear in the newly-created `_book` folder. You can check its apprearance in your browser by opening one of the html files (Something like Chrome > File Open File... > Open ~/_book/index.html).

## Hookup Pages/Travis
1. **Confirm GitHub Pages Setup**: On your newly added GitHub repo, **go to Settings > Options > GitHub Pages**. Confirm that your site is being published using the gh-pages branch (you should see a green banner saying everything is up and running).
2. **Activate Travis CI**: Go to https://travis-ci.org/ and link your GitHub account. Then go to your profile and activate your new repo. 
3. **Create GitHub PAT**: Go to https://github.com/settings/tokens and generate a personal access token (PAT). Call it whatever (maybe "Travis CI Hookup") and check the first checkmark that says "repo" (to give it access to your public repos). Make sure to copy down the PAT; it will not be shown again.
4. **Add PAT to Travis**: On the Travis page for your repo, **go to Settings > Environment Variables**. Create a new variable with name **GITHUB_PAT** and value of your copied PAT your recently created.
