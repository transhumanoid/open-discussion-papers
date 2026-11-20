# Medium Formatting Conventions

Rules for markdown that pastes cleanly into Medium's editor.

## Headers

Medium uses its own heading styles. Use ATX headers (`#`, `##`, `###`) — Medium maps them automatically on paste. Do not use HTML heading tags.

## Bold and Italic

- Bold: `**text**` → Medium renders as bold.
- Italic: `*text*` or `_text_` → Medium renders as italic.
- Do not nest bold inside italic or vice versa on paste; Medium's importer can mangle it.

## Images

Medium requires images to be hosted. Upload directly in the editor rather than embedding URLs in markdown — pasted image URLs from external hosts often break.

## Links

Standard markdown links `[text](url)` paste correctly.

## Blockquotes

`>` lines become pull quotes in Medium. Use sparingly.

## Code

Inline code with backticks works. Fenced code blocks (` ``` `) paste as code blocks but Medium may strip syntax highlighting.

## Things to Avoid

- Tables: Medium does not render markdown tables. Convert to bullet lists before pasting.
- Footnotes: not supported. Move references inline or to a final section.
- Embedded HTML: stripped or mangled on paste.
- Very long lines: Medium wraps at its own width; keep paragraphs under ~100 words for readability.

## Recommended Paste Order

1. Copy the full markdown.
2. Paste into a blank Medium draft.
3. Check headings mapped correctly.
4. Re-apply bold/italic where the importer dropped them.
5. Add a cover image if desired.
6. Set tags and publish settings manually — Medium's API does not cover these.