# UBI Center analysis template
Template for UBI Center analyses, including GitHub Actions to merge into [ubicenter.org](http://ubicenter.org).

Instructions:
* Replace `reponame` with the name of the repo in `environment.yml` and `.github/workflows/deploy_website.yml`.
* Add data generation `.py` script and data files to `jb/data` folder.
Store files in `.csv.gz` format and load them as local files in analysis notebooks.
* Add all necessary packages to `environment.yml`.
* Use pull requests to make changes; the workflows will trigger and alert you of any errors.

## Website integration

In `website/`, there are two file:
- `post.ipynb` should contain all the content, including graphs, tables and markdown, of the website post.
- `metadata.yml` should contain the post metadata, including authorship, title, cover image and other fields.

On pushing changes to the repo, a fork of the `ubicenter.org` repo will be updated with the new post, under the branch with the same name as this repo. From there, a PR should be filed from the source repo `ubicenter-post-bot/repo-name` to `ubicenter/master`.
