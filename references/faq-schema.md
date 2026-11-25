# FAQ schema template

Use one `Question` object per FAQ in the blog. The question and answer text must match the visible FAQ on the page word for word.

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "Question 1 exactly as written in the blog?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Answer 1 exactly as written in the blog."
      }
    },
    {
      "@type": "Question",
      "name": "Question 2 exactly as written in the blog?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Answer 2 exactly as written in the blog."
      }
    }
  ]
}
```

Notes:
- Wrap it in `<script type="application/ld+json"> ... </script>` if the CMS needs raw HTML. Rank Math and Yoast FAQ blocks generate it for you.
- Do not mark up FAQs that are not visible on the page.
- Validate with Google's Rich Results Test before publishing.
