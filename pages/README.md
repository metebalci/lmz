# pages/

This is LMZ's project page, published by GitHub Pages. Its files are written
by hand, with no build step, no generator and no script. (`site/`, in this
repository, is something else: the site files a Lisp Machine loads.)

- `index.html` is the page. It is brief on purpose, and will grow.
- `style.css` is the stylesheet, in the look of ozd's page
  (<https://ozd.metebalci.com/>): ink and paper with one spot color, and no
  dark mode.
- `mascot.svg` is LMZ's mascot: a 3.5-inch diskette with a label reading
  LMZ, wearing Cold Boot's face and waving arm, as ozd's page draws CADR, OZ
  and muir-fpga's board. LMZ is the software, so it is the diskette.
  `favicon.svg` is the diskette without its face.
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
