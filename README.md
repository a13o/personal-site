# a13o.com

* Written locally using [Jekyll](https://jekyllrb.com/)
* Pushed to GitHub remote
* Built automatically by [GitHub Pages](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll)
* [Hosted on a custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site) via GitHub Pages

# How to set up a local environment

```pwsh
# unelevated
git clone https://github.com/a13o/personal-site.git
winget install RubyInstallerTeam.RubyWithDevKit.3.1
# as administrator
Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope LocalMachine
ridk install 3
Set-ExecutionPolicy -ExecutionPolicy AllSigned -Scope LocalMachine
# unelevated
gem update
cd personal-site
bundle install
```

# How to maintain dependencies

```pwsh
bundle update
# pray
```

# How to local dev
```pwsh
bundle exec jekyll serve
```