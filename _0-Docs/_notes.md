
- Note #1
    - If you're adding a new list of entries (i.e. Portfolio of projects), you need to follow how the "authors" collection was setup on the Jekyll's tutorial:
        - https://jekyllrb.com/docs/step-by-step/09-collections/
    - This is not automatically like the blog, so manual setup is needed.

- Note #2 | Importing blogger to jekyll
    - Link: https://import.jekyllrb.com/docs/blogger/
    - Template:
        `jekyll import blogger --source NAME --no-blogger-info --replace-internal-link --comments`
    - Example:
        `bundle exec jekyll import blogger --source blog-03-11-2023.xml --no-blogger-info --replace-internal-link`
        - This is if you gemfile'd the follow things:
            `gem "jekyll-import", "~> 0.21.0"`
            `gem "rexml", "~> 3.2"`
            `gem "safe_yaml", "~> 1.0"`

- Note #3 | Possible way to grab repo information directly from GitHub
    - Discussion:
        - https://talk.jekyllrb.com/t/exposing-information-of-all-repositories-through-site-built-with-github-pages/4403/2
    - Plugin: 
        - https://talk.jekyllrb.com/t/exposing-information-of-all-repositories-through-site-built-with-github-pages/4403/2#:~:text=jekyll/github%2Dmetadata,26

- Note #4 | Obtaining stats of langages used in personal repo:
    - API: https://github.com/anuraghazra/github-readme-stats
        - Found via https://github.com/MichaelCurrin/MichaelCurrin.github.io/blob/master/_includes/interests.html

- Note #5 | How GitHub meta data is structured
    - this is when looping through "site.github.github_repositories"
    - Example of an object:
        - https://github.com/doowb/github-metadata#results
    - Full examples of JSON object:
        - https://github.com/doowb/github-metadata/blob/master/docs/results.json
    - GitHub API Docs:
        - https://developer.github.com/v3/

- Note #6 | Adding code comments when using Liquid language
    - https://shopify.github.io/liquid/tags/template/