# Tool Minded

Roger's homepage powered by [Jekyll](https://jekyllrb.com), hosted on [GitHub Pages](https://pages.github.com).

## Install Locally

```bash
brew install ruby@2.7
cd ~ && sudo chown -R Roger .bundle;
sudo gem install bundler
sudo gem install jekyll -v 3.9.0
bundle install --system
bundle exec jekyll serve --watch

# Build inlcude drafts
bundle exec jekyll serve --drafts
```

## Manage Script

Usage: `./manage.py [-cgm] [input]`

```
-c:     create post
-g:     generate static templates
-m:     covert a normal markdown file to jekyll format
```

## Template Usage

Use global HTML header.

```
<head>
  {% include head_basic.html %}
<head>
```

## Dependencies Versions

https://pages.github.com/versions/
