# AI chatbot on a Hugo site

A Hugo blog with an AI chatbot in the corner of every post. It reads the post a visitor is on and answers questions from it. No backend, no Hugo module, no build step beyond `hugo`.

**Live demo:** https://fengyiqicoder.github.io/hugo-ai-chatbot/ (Crumb & Crust is a made-up sourdough blog.)

## Add it to your Hugo site

1. Get a free key at [onetagai.com](https://onetagai.com) (1,000,000 tokens one time, no credit card).
2. Open the template every page shares, `baseof.html` in your `layouts` folder (`layouts/baseof.html` on Hugo 0.146 and newer, `layouts/_default/baseof.html` on older sites like this demo), and add one line before `</body>`:

```html
<script async src="https://onetagai.com/widget.js" data-key="YOUR_ONETAG_KEY"></script>
```

3. Run `hugo server` to try it, then deploy as usual.

Using a theme? Copy the theme's `baseof.html` into your own `layouts/` folder at the same path (for Ananke: `cp themes/ananke/layouts/baseof.html layouts/`) and edit the copy, so theme updates do not overwrite it. Many themes also have a hook for this, such as `layouts/partials/extend_footer.html` in PaperMod.

## License

MIT
