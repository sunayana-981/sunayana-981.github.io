# Sunayana Samavedam — Academic Homepage

A minimal, typography-driven academic personal website.

## Structure

```
site/
├── index.html    ← The complete website (single file, static)
├── data.json     ← Structured resume data (reference for updates)


README.md
```

Site lives at `https://sunayana-981.github.io`

## Customization

**Accent color**: Change `--c-accent` in the `:root` CSS block  
**Fonts**: Swap the Google Fonts `<link>` and update `--font-serif` / `--font-sans`  
**Max width**: Adjust `--max-w` (default: 780px)  
**Add a publication**: Copy an existing `.research-entry` block and edit the content

## Interpretability design

Introduction seeds a shared residual stream. Career sections read from it and
write contributions back into it; Contact receives the accumulated representation.
The stream advances with navigation and scrolling, with motion disabled when the
visitor requests reduced motion.

`CAREER_STAGES` in `index.html` contains authored, illustrative concept weights
grounded in each section's work. Each state sums all contributions through that
layer. The logit-lens metaphor displays the top four concepts, compares ranks with
the preceding layer, and computes the displayed norm from the accumulated vector
(scaled by 100). These are portfolio illustrations, not measured neural logits or
activations. Contact preserves the final vector. Direct links and backward
navigation use the same precomputed states.

When changing contributions, update both `CAREER_STAGES` and the visible
`.layer-annotation` copy. Research spans publications (L1) and working papers (L2).
