# Source code for Shalini Gupta's website.

Based off the [Hugo Academic Theme](https://github.com/wowchemy/starter-hugo-academic), with light modifications.

Usage:
* Initial setup: `brew install golang hugo`.
* To develop locally: `hugo server --disableFastRender`. This will produce a link that you can navigate to in your browser. When you edit any file, the changes are reflected in your browser automatically.
* To deploy: `hugo && cd public && git add . && git commit -am "<YOUR COMMIT MESSAGE HERE>" && git push && cd -`.
  * The `hugo` command auto-generates the website code and places it in `public/`, which we then push to [the GitHub Pages repository](https://github.com/gshalini21294/gshalini21294.github.io).
* After deploying, also make sure to push the changes to this repository!