# [ONDATA](https://dev4223.github.io/ondata/)

Based on [Jekyll](https://jekyllrb.com/) and [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/)
[![GitHub release](https://img.shields.io/gem/v/minimal-mistakes-jekyll.svg)](https://github.com/mmistakes/minimal-mistakes/releases) [![GitHub license](https://img.shields.io/badge/license-MIT-lightgrey.svg)](https://raw.githubusercontent.com/mmistakes/minimal-mistakes/master/LICENSE.txt)

Minimal Mistakes is a flexible two-column Jekyll theme. See what's new in the [CHANGELOG](https://github.com/mmistakes/minimal-mistakes/blob/master/CHANGELOG.md).

:sparkles: Minimal Mistakes is now available as a [Ruby gem](https://rubygems.org/gems/minimal-mistakes-jekyll). Consult the [Quick-Start Guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) and [this blog post](https://mmistakes.github.io/minimal-mistakes/jekyll/gemified-theme-beta/) to learn how to upgrade.

[![Minimal Mistakes live preview][2]][1]

[1]: https://mmistakes.github.io/minimal-mistakes/
[2]: screenshot.png (live preview)

![layout examples](screenshot-layouts.png)

## Notable Features

- "Gemified" for easier install/upgrading
- Compatible with Jekyll 3.5 and GitHub Pages
- Support for Jekyll's built-in Sass/SCSS preprocessor
- Several responsive layout options (single, archive index, splash, and paginated home page)
- SEO optimized with support for [Twitter Cards](https://dev.twitter.com/cards/overview) and [Open Graph](http://ogp.me/) data
- Optional [header images](https://mmistakes.github.io/minimal-mistakes/docs/layouts/#headers), [custom sidebars](https://mmistakes.github.io/minimal-mistakes/docs/layouts/#sidebars), [table of contents](https://mmistakes.github.io/minimal-mistakes/docs/helpers/#table-of-contents), [galleries](https://mmistakes.github.io/minimal-mistakes/docs/helpers/#gallery), related posts, [breadcrumb links](https://mmistakes.github.io/minimal-mistakes/docs/configuration/#breadcrumb-navigation-beta), [navigation lists](https://mmistakes.github.io/minimal-mistakes/docs/helpers/#navigation-list), and more.
- Commenting support (powered by [Disqus](https://disqus.com/), [Facebook](https://developers.facebook.com/docs/plugins/comments), Google+, [Discourse](https://www.discourse.org/), static-based via [Staticman](https://staticman.net/), and custom).
- [Google Analytics](https://www.google.com/analytics/) support.
- UI localized text in English (default), Brazilian Portuguese, Chinese, French, German, Italian, Korean, Nepali (Nepalese), Russian, Spanish, and Turkish

## Demo Pages

| Name                                        | Description                                           |
| ------------------------------------------- | ----------------------------------------------------- |
| [Post with Header Image][header-image-post] | A post with a large header image. |
| [HTML Tags and Formatting Post][html-tags-post] | A variety of common markup showing how the theme styles them. |
| [Syntax Highlighting Post][syntax-post] | Post displaying highlighted code. |
| [Post with a Gallery][gallery-post] | A post showing several images wrapped in `<figure>` elements. |
| [Sample Collection Page][sample-collection] | Single page from a collection. |
| [Categories Archive][categories-archive] | Posts grouped by category. |
| [Tags Archive][tags-archive] | Posts grouped by tag. |

Additional sample posts are available under [posts archive][year-archive] on the demo site. Source files for these (and the entire demo site) can be found in [`/docs`](docs).

[header-image-post]: https://mmistakes.github.io/minimal-mistakes/layout-header-image-text-readability/
[gallery-post]: https://mmistakes.github.io/minimal-mistakes/post%20formats/post-gallery/
[html-tags-post]: https://mmistakes.github.io/minimal-mistakes/markup/markup-html-tags-and-formatting/
[syntax-post]: https://mmistakes.github.io/minimal-mistakes/markup-syntax-highlighting/
[sample-collection]: https://mmistakes.github.io/minimal-mistakes/recipes/chocolate-chip-cookies/
[categories-archive]: https://mmistakes.github.io/minimal-mistakes/categories/
[tags-archive]: https://mmistakes.github.io/minimal-mistakes/tags/
[year-archive]: https://mmistakes.github.io/minimal-mistakes/year-archive/

## Usage

For detailed instructions on how to configure, customize, add content, and more read the [theme's documentation](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/).

**Note:** Gem version of the theme requires Jekyll v3.3+ and is not currently supported on [GitHub Pages](https://pages.github.com/). You can still use the theme with GitHub Pages, you'll just need to install using the old "[repo fork method](https://mmistakes.github.io/minimal-mistakes/docs/installation/)".

## Quick Start

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "minimal-mistakes-jekyll"
```

Add this line to your Jekyll site's `_config.yml` file:

```yaml
theme: minimal-mistakes-jekyll
```

Then run Bundler to install the theme gem and dependencies:

```bash
bundle install
```

To update the theme run `bundle update`.

---

## Credits

### Creator Minimal Mistakes Theme

**Michael Rose**

- <https://mademistakes.com>
- <https://twitter.com/mmistakes>
- <https://github.com/mmistakes>

### Other:

- [Jekyll](http://jekyllrb.com/)
- [jQuery](http://jquery.com/)
- [Susy](http://susy.oddbird.net/)
- [Breakpoint](http://breakpoint-sass.com/)
- [Magnific Popup](http://dimsemenov.com/plugins/magnific-popup/)
- [FitVids.JS](http://fitvidsjs.com/)
- Greedy Navigation - [lukejacksonn](http://codepen.io/lukejacksonn/pen/PwmwWV)
- [jQuery Smooth Scroll](https://github.com/kswedberg/jquery-smooth-scroll)
