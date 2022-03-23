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

## Tool logo size.

90x90 or 180x180 with alpha png format, file name should be lower case.

folder: assets/tool-icon

## Quotes

[goodreads](https://www.goodreads.com/search?page=1&q=tool&search_type=quotes&tab=quotes)

```js
var s = ""

document.querySelectorAll(".quoteText").forEach(e => {
	let innerString = e.innerText.trim()
	let arr = innerString.split("— ")
	
	if(arr[0].indexOf("tool") == -1) { return }
	assert(arr.length == 2, e)
	
	let quoteText = arr[0].trim().slice(1, -1)
	let authorAndBook = arr[1].trim()
	
	s += "- text: |\n"
	for(const ql of quoteText.split("\n")) {
		s += "    " + ql + "\n"
	}
	
	let dividerPos = authorAndBook.indexOf(" (")
	if(dividerPos != -1) {
		s += "  author: " + authorAndBook.slice(0, dividerPos).trim() + "\n"
		s += "  book: |\n    " + authorAndBook.slice(dividerPos+2, -1) + "\n"
	} else {
		s += "  author: " + authorAndBook + "\n"	
	}
})

console.log(s)
```

## Dependencies Versions

https://pages.github.com/versions/
