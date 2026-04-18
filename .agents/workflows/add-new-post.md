---
description: How to add a new blog post to the Hugo website
---
Follow these steps to create, write, and preview a new blog post for the site:

1. Scaffold the New Post
Use the Hugo CLI to generate a new post from the default archetype. This ensures your post automatically contains the correct frontmatter (date, title, draft status).

`hugo new posts/your-post-title.md` 
*(Replace `your-post-title.md` with a hyphenated, lowercase file name)*

2. Write Your Content
Open the newly created file located at `content/posts/your-post-title.md`. 
Update the frontmatter parameters at the top of the file:
- **title**: "Your Post Title"
- **draft**: Keep this as `true` while you are writing.

Write the rest of your blog post using standard Markdown below the `---` frontmatter block.

3. Preview Locally
To preview your post as you write, start the Hugo server. You must pass the `-D` flag so that Hugo includes files marked as `draft: true`.

// turbo
`hugo server -D`

4. Publish
Once you are completely done writing and reviewing your post, change `draft: true` to `draft: false` in the file's frontmatter. The post will now be included in the production build.
