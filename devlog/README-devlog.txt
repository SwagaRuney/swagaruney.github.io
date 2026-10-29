DEVLOG SETUP (Claude until i get the time to remake from scratch, sorry :< )

Files
  index.html            the page
  posts/index.json       the list of posts
  posts/*.md             one Markdown file per post
  posts/img/             (optional) screenshots

Put devlog.html and the posts/ folder in your swagaruney.github.io repo, together.

ADD A POST (3 steps)
1. Create posts/my-post.md and write it in Markdown.
2. Add an entry to the top of posts/index.json:
   {
     "slug": "my-post",          <- short, lowercase, no spaces (used in the link)
     "title": "My post title",
     "date": "2026-11-02",       <- YYYY-MM-DD
     "tag": "music",             <- music, code, chart, or misc
     "summary": "One line shown in the list.",
     "file": "my-post.md"
   }
   Commas go between entries, not after the last one.
3. Commit and push. The site updates in a minute or two.

MARKDOWN YOU CAN USE
  ## Heading        - bullet list       **bold**   *italic*   `code`
  [link text](https://example.com)      ![alt](img/pic.png)
  ``` on its own line starts and ends a code block

Posts are sorted by date, so order in index.json does not matter.
Works fine for 10-15 posts and well beyond.

TESTING LOCALLY
Browsers block loading the posts when you double-click devlog.html.
Run "python -m http.server" in the folder and open http://localhost:8000/index.html
