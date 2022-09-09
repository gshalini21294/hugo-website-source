# Source code for Shalini Gupta's website.

Based off the [Hugo Academic Theme](https://github.com/wowchemy/starter-hugo-academic), with light modifications.

Usage:
* Initial setup:
  * `brew install golang hugo`
  * `git clone git@github.com:gshalini21294/hugo-website-source.git`
  * `cd hugo-website-source/`
  * `git submodule add -f -b master git@github.com:gshalini21294/gshalini21294.github.io.git public`
  * `git rm --cached public`
* To develop locally: `hugo server --disableFastRender`. This will produce a link that you can navigate to in your browser. When you edit any file, the changes are reflected in your browser automatically.
* To deploy:
  * `hugo` (This command auto-generates the website code and places it in `public/`, which we then push to [the GitHub Pages repository](https://github.com/gshalini21294/gshalini21294.github.io).)
  * `cd public`
  * `sed -i'' -e 's/CV.pdf">/CV.pdf" target="_blank">/' index.html` (Hugo does not allow us to configure the CV button along the top to open in a new tab, so we hack the HTML directly via this command.)
  * `git add .`
  * `git commit -m "<YOUR COMMIT MESSAGE HERE>"`
  * `git push`
  * Wait ~5 minutes for the changes to be reflected on the live site, [gshalini.com](https://gshalini.com/).
  * Add, commit, and push the changes to the `hugo-website-source` repository as well!

Troubleshooting:
* If you get errors about "failed to resolve output format" when running Hugo: `sudo rm -rf $TMPDIR/hugo_cache/`, then try again.