# SEO Blog Writer: a Claude Skill

SEO Blog Writer is a Claude Skill that researches a keyword on the live web (Google SERP, People Also Ask, Reddit, Quora and AI answers), filters the best keywords by intent and business value, and writes a 3,000+ word blog optimized for semantic SEO, AEO and GEO. It finishes with ready-to-paste SEO fields (slug, title, meta description, image alt text, tags) and FAQ schema in JSON-LD, and it refuses to invent statistics, results or links.

## What it does

1. **Researches the keyword:** top 10 results, People Also Ask, Reddit and Quora questions, and how AI tools answer the topic.
2. **Filters keywords:** a table of focus, secondary and long-tail keywords with intent, estimated difficulty and business value.
3. **Finds the content gap:** what competitors miss, plus an H2/H3 outline before writing.
4. **Writes the blog:** quick answer first, question-style headings, tables, bullet lists, FAQs and a CTA.
5. **Gives SEO fields:** slug, H1, SEO title, meta description, keywords, image name, alt, title, description, tags and FAQ schema.

## Requirements

- **Web search:** The research step needs web search turned on in Claude. Without it, the skill still writes the blog but marks research findings as unverified.
- **Keyword data:** Difficulty and volume figures are estimates. Check final keywords in Google Keyword Planner, Ahrefs or Semrush.
- **No API keys** or environment variables are needed.

## Install

**Claude Code**

```bash
git clone https://github.com/<mobeenshahid-cloud>/seo-blog-writer.git ~/.claude/skills/seo-blog-writer
```

Restart Claude Code. The skill loads when you ask for an SEO blog.

**Claude apps**

Download this repository as a ZIP and upload the `seo-blog-writer` folder in Claude's Skills settings.

## Usage

Ask Claude something like:

> Write an SEO blog for the keyword "AI voice agents for dental clinics". Website: example.com. Audience: clinic owners. Location: none.

Only the keyword is required. Add your website to get internal links and examples from your own pages.

## Files

```
seo-blog-writer/
├── SKILL.md                  # The skill instructions
└── references/
    └── faq-schema.md         # JSON-LD FAQ schema template
```

## License

MIT. See [LICENSE](LICENSE).
