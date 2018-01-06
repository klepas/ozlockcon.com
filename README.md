OzSecCon Jekyll website
=============

[![Build Status](https://semaphoreci.com/api/v1/barnie995/ozlockcon-com-3/branches/master/badge.svg)](https://semaphoreci.com/barnie995/ozlockcon-com-3)
> Code that builds a static copy of the OzSecCon website.


## Content

* [Configuration](#configuration)
* [Editing content](#editing-content)
* [Dependencies](#dependencies)
* [Building](#building)
* [License](#license)


----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Configuration

Most of the con’s details are tracked in the config file (`_config.yml`), for example:

```yaml
title: OzSecCon
con_year: 2017
con_date: June 3–4th
con_location: Melbourne
email: admin@OzSecCon.com
```

Check out what’s there before you hardcode stuff. (:

These are called in the [templates](https://jekyllrb.com/docs/templates/) like so

```liquid
<a href="mailto:{{ site.email }}">{{ site.email }}</a>
```


**[↑ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Editing content

Easiest way is to edit the Markdown files right here on GitHub, via the web interface.

The site is configured to use the [kramdown Markdown parser](https://kramdown.gettalong.org/syntax.html), which has some pretty nice syntax features.

If you add a new page you will have to manually add it to the navigation include (`_includes/navigation.html`).


**[↑ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Dependencies

To build the site locally you will need:

- Ruby `2.3.1` (haven’t tested with later versions; should work fine)
- [Jekyll](https://jekyllrb.com/) `3.3.0` (Ruby-based static site generator)
- [jekyll-assets](https://github.com/jekyll/jekyll-assets) (an asset pipeline)
- [Bourbon](http://bourbon.io/) and [Neat](http://neat.bourbon.io/)

We sorta have automated [CI setup through semaphoreci.com](https://semaphoreci.com/klepas/ozlockcon-com) for the `develop` branch. This currently points to an Amazon S3 bucket... but our web server is elsewhere so poke @klepas or @barnie995 to do a build if you can’t and/or can’t cp files to the box.


**[↑ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## Building

If you need to build the site manually (eg for a manual deploy, or for development):

1. clone the repo
2. set up ruby
3. install dependencies (pulled from the `Gemfile`)
4. run/build

(I’m skipping the setup of Ruby here — have fun with that. FWIW, klepas uses [rbenv](https://github.com/rbenv/rbenv), and he hears that [rvm](https://rvm.io/) is similarly OK.)

```shell
git clone git@github.com:klepas/ozlockcon.com.git
cd ozlockcon.com
bundle install
```

And then either to serve or just build respectively:

```shell
bundle exec jekyll serve
```

```shell
bundle exec jekyll build
```

The generated output files (html/css/…) will reside in the `_site/` folder.


**[↑ back to top](#content)**

----------------------------------------------------------------------------------------------------------------------------------------------------------------

## License

Code is licensed under [MIT](https://raw.githubusercontent.com/klepas/ozlockcon.com/master/LICENSE).

[Code of Conduct](https://raw.githubusercontent.com/klepas/ozlockcon.com/master/conduct.md) is licensed under the [Creative Commons Attribution-ShareAlike license](http://creativecommons.org/licenses/by-sa/3.0/).

Content is © 2016– OzSecCon Consmiths.


**[↑ back to top](#content)**

# `%}`
