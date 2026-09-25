# Personal website — Gaofei Shen

Static [Jekyll](https://jekyllrb.com/) site served at
<https://www.gaofeishen.com> through GitHub Pages.

## Structure

- `index.md` — Home (bio, interests)
- `publications.md` — Publications, rendered from `_data/publications.json`
- `photography.md` — Photography
- `_data/publications.json` — publication records; edit this file to update the list
- `_layouts/`, `_includes/` — shared page markup
- `assets/css/style.css` — all styling
- `CNAME` — custom domain (`www.gaofeishen.com`)

## Preview locally

With Ruby and Bundler:

```sh
bundle install
bundle exec jekyll serve
# open http://127.0.0.1:4000
```

Without Ruby, use the Jekyll container:

```sh
podman run --rm -it -p 4000:4000 \
  -v "$PWD:/srv/jekyll:Z" \
  docker.io/jekyll/jekyll:pages jekyll serve --host 0.0.0.0
```

## Notes

- The `Updated …` badge reads the Jekyll build time (`site.time`). It needs no
  manual maintenance.
- GitHub Pages runs the build on every push to the default branch.
