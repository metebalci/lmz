# pages/

This is LMZ's project page, published by GitHub Pages. Its files are written
by hand, with no build step, no generator and no script. (`site/`, in this
repository, is something else: the site files a Lisp Machine loads.)

- `index.html` is the page. It is brief on purpose, and will grow.
- `style.css` is the stylesheet, in the look of ozd's page
  (<https://ozd.metebalci.com/>): ink and paper with one spot color, and no
  dark mode.
- `mascot.svg` is LMZ's mascot, drawn by hand for this page: a small robot
  with a screen for a face, parentheses for ears and a lambda for an antenna,
  in a pink T-shirt with a Z. A paper halo under its linework lets it stand
  on a dark background too. `favicon.svg` is its shirt, cropped to the Z.
- `fonts/` holds the three families, served from here rather than from
  Google. `fonts/README.md` says where they came from and under what license.

`.github/workflows/pages.yml` publishes this directory on every push to
`main` that touches it, and can be run by hand. It needs a one-time setting:
the repository's Pages source must be GitHub Actions (Settings, Pages, Build
and deployment, Source). The page is then served at the repository's
`github.io` address. A custom domain can be added later, with a `CNAME` file
here and the same domain in the Pages settings; none is chosen yet.

To look at the page before pushing, open `index.html` in a browser, or serve
the directory:

    python3 -m http.server -d pages 8000

The fonts hold only printable ASCII and a few punctuation marks (see
`fonts/README.md`). A character outside that set is drawn in a fallback face,
so write `&rsquo;`, `&mdash;`, `&middot;` and `&copy;`, and nothing beyond them.
