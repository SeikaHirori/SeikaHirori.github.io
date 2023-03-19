
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
    - https://talk.jekyllrb.com/t/exposing-information-of-all-repositories-through-site-built-with-github-pages/4403/2

- Note #4| Obtaining stats of langages used in personal repo:
    - API: https://github.com/anuraghazra/github-readme-stats
        - Found via https://github.com/MichaelCurrin/MichaelCurrin.github.io/blob/master/_includes/interests.html