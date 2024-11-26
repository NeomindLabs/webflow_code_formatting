# Syntax Highlighting Code Blocks in Webflow Blog Posts
For some reason, Webflow really likes to mess up the HTML markup of code blocks.

Here's how we work around this.

1. Write your post in Markdown in your favourite text editor.
2. Use your text editor's preview feature (VS Code has a nice one built in) and copy the rendered markdown from the preview. **Don't just copy the raw markdown**, you need to copy the **rendered and styled** content.
3. Paste this content into the Webflow form for making a blog post. Save it.

Now, go to your site's Webflow settings, and add [this HTML snippet](/webflow-code-highlighting.html) to your footer. It will do a few things:
- Load [`Highlight.js`](https://highlightjs.org/) and its style sheet from a CDN.
- Reformat Webflow's code block HTML elements to be single blocks of `<pre><code>` elements.
- *Then* apply Highlight.js.

Save this footer, and publish your site for these changes to take effect.
![Screenshot 2024-11-26 at 2 15 20 PM](https://github.com/user-attachments/assets/bc8545eb-808c-477c-938d-5fda7df51da3)

Without restructuring Webflows code block HTML elements to be single blocks of `<pre><code>` elements, Highlight.js will not pick them up at all.

Good luck!
