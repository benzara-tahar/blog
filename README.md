# My Personal Blog

Welcome to my personal blog repository. This is where I share my thoughts, ideas, and experiences.

## Tech Stack

This blog is built with [Astro](https://astro.build) using the [Astro Cactus](https://github.com/chrismwilliams/astro-theme-cactus) theme, a simple and elegant starter for creating a fast, accessible, and SEO-friendly blog.

## Development

### Setup

```bash
# Clone the repository
git clone [your-repo-url]
cd blog

# Install dependencies
npm install
```

### Commands

| Command           | Action                                                        |
| :---------------- | :------------------------------------------------------------ |
| `npm install`     | Installs dependencies                                         |
| `npm run dev`     | Starts local dev server at `localhost:3000`                   |
| `npm run build`   | Build your production site to `./dist/`                       |
| `npm run preview` | Preview your build locally, before deploying                  |

### Adding Blog Posts

1. Create a new markdown file in the `src/content/post/` directory
2. Add frontmatter at the top of the file:
   ```markdown
   ---
   title: "Your Post Title" 
   description: "Brief description of your post (50-160 characters)"
   publishDate: "YYYY-MM-DD"
   tags: ["tag1", "tag2"]
   ---
   ```
3. Write your content in Markdown format below the frontmatter
4. Your post will automatically appear in the blog once built

## Analytics

This theme/template doesn't include a specific solution due to there being a number of use cases and/or options which some people may or may not use.

You may be asked to included a snippet inside the **HEAD** tag of your website when setting it up, which can be found in `src/layouts/Base.astro`. Alternatively, you can add the snippet in `src/components/BaseHead.astro`.

## Deploy

[Astro docs](https://docs.astro.build/en/guides/deploy/) has a great section and breakdown of how to deploy your own Astro site on various platforms and their idiosyncrasies.

By default the site will be built (see [Commands](#commands) section) to a `/dist` directory.

## Acknowledgment

This theme was inspired by [Hexo Theme Cactus](https://github.com/probberechts/hexo-theme-cactus)

## License

MIT
