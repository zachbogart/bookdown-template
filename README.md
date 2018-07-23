# bookdown-template

This template should allow you to setup your own bookdown book that can be published with GitHub Pages and automate rendering using Travis CI.

## Create the Book
1. **Clone this repo**
2. **Create your book**: create new .Rmd files for your new chapters and add content.
3. **Check the render**: Once finished adding content, run `bookdown::render_book("index.Rmd", "all")` to render a draft of the book. This will appear in the newly-created `_book` folder. You can check its apprearance in your browser by opening one of the html files (Something like Chrome > File > Open File... > Open ~/_book/index.html).
4. **Push to GitHub**: Push your work to a new repo on GitHub.

## Hookup Pages/Travis
1. **Confirm GitHub Pages Setup**: On your newly added GitHub repo, **go to Settings > Options > GitHub Pages**. Confirm that your site is being published using the gh-pages branch (you should see a green banner saying everything is up and running).
2. **Activate Travis CI**: **Go to https://travis-ci.org/** and link your GitHub account. Then **go to your new Travis profile** and activate your repo. 
3. **Create GitHub PAT**: **Go to https://github.com/settings/tokens** and generate a personal access token (PAT). Call it whatever (maybe "Travis CI Hookup") and check the first checkmark that says "repo" (to give it access to your public repos). Make sure to copy down the PAT; it will not be shown again.
4. **Add PAT to Travis**: On the Travis page for your repo, **go to Settings > Environment Variables**. Create a new variable with name **GITHUB_PAT** and value of your copied PAT your recently created.
5. Now whenever you make a change and commit it to your repo, Travis should render the book for you and publish it to your GitHub Pages site using the gh-pages branch.

**Notes**:
- You can track builds by visiting https://travis-ci.org/
- You can also check things are working by looking at the [commits for the repo](https://github.com/zachbogart/bookdown-template/commits/master) (there should be a yellow dot when a Travis build is in progress and a checkmark if it passes).

## Having Trouble?
This template is a side-addition to a resource I created with [Joyce Robbins](https://github.com/jtr13) called [edav.info/](https://jtr13.github.io/EDAV) (Link to [GitHub repo](https://github.com/jtr13/EDAV)). Checkout [our page on Hooking up Travis](http://edav.info/publish.html#hooking-up-travis) for more info if you are feeling lost. 

If all goes well, you can sit back, relax, and watch Travis do the work for you.

![Lazy Homer](https://media.giphy.com/media/lPdn5MOabkgCY/giphy.gif)
