---
layout: post
title:  "Make a GitHub Pages site with Jekyll"
date:   2025-04-05 21:16:18 -0700
categories: GitHub Jekyll
---

# Follow these steps

1. Create a repo. Don't add a **readme** file.

2. Make a local repo on your computer.

3. Copy and execute the code under *...or create a new repository...* that you see on GitHub.

4. Make a new Jekyll project in the local directory:

    `jekyll new --skip-bundle . --force`

    The `--force` flag will create the directory eventhough it already exists.

5. Modify the Gemfile

    - Comment out `jekyll` line

    - Uncomment `github-pages` and specify dependency version. For example:

      `gem "github-pages", "~> 232", group: :jekyll_plugins`

6. Run `bundle install`
    
    Add **Gemfile.lock** to **.gitignore**

7. Modify **config.yml**

    If using a custom domain and CSS does not load, modify the `url` parameter:

    `url: "https://mateo.casa"`

8. Preview site locally

    `bundle exec jekyll serve`

9. Commit files and push to GitHub

10. Set up **GitHub Actions**

    1. Pages/Settings/Build and Deployment

    2. Choose **Jekyll Workflow**

    3. Commit changes

11. Verify custom domain if using

    - Profile/Settings/Pages

    - I think this can be done even before creating the repo.

12. Configure **A Records**

## Source

Here's the YouTube tutorial I followed to make this workflow:

<iframe width="560" height="315" src="https://www.youtube.com/embed/fV01b0duZwU?si=dyVvyi0NHhj4C_o1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>