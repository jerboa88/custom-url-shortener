<!-- Project Header -->
<div align="center">
	<img class="projectLogo" src="images/icon.svg" alt="Project logo" title="Project logo" width="256">
	<br/>
	<h1 class="projectName">
		<a href="https://l.johng.io">Short End - URL Shortener</a>
	</h1>
	<p class="projectBadges">
		<a href="https://unmaintained.tech/">
			<img src="https://unmaintained.tech/badge.svg" alt="No Maintenance Intended" title="No Maintenance Intended"/>
		</a>
		<img src="https://img.shields.io/badge/Experimental-%E2%9A%A0%EF%B8%8E-ca8a04.svg" alt="Experimental" title="Experimental"/>
		<img src="https://johng.io/badges/category/App.svg" alt="Project category" title="Project category">
		<img src="https://img.shields.io/github/languages/top/jerboa88/Short-End.svg" alt="Language" title="Language">
		<img src="https://img.shields.io/github/repo-size/jerboa88/Short-End.svg" alt="Repository size" title="Repository size">
		<a href="LICENSE">
			<img src="https://img.shields.io/github/license/jerboa88/Short-End.svg" alt="Project license" title="Project license"/>
		</a>
			<a href="https://l.johng.io" title="Short End - URL Shortener">
			<img src="https://img.shields.io/website?url=https%3A%2F%2Fl.johng.io&up_message=l.johng.io%20%E2%86%97" alt="Project URL" title="Project URL">
		</a>
	</p>
	<p class="projectDesc">
		An experimental client-side URL shortener
	</p>
	<br/>
</div>


> [!IMPORTANT]
> I've marked this project as [UNMAINTAINED](https://unmaintained.tech/) because it hasn't seen an update in a while. You can still fork/download/use this project at your own risk, but I won't be able to provide support or updates.

> [!WARNING]
> This is an experimental or POC project. It may contain bugs or incomplete features, and is not intended for production use. Breaking changes may be made at any time. Consider more stable alternatives for critical applications.

## About
This is an experimental URL shortener using client-side redirects. If you want a simple link shortener for personal use but don't have your own server for setting up HTTP redirects, you may find this interesting.

Obviously, it's not a good idea to use this for anything important. Client-side redirects are slower and less reliable than HTTP redirects because they require the page to load before redirecting. They can negatively impact SEO, as search engines may not follow them consistently, and may cause accessibility issues or a poor user experience—especially if users briefly see the original page.


## Installation
This project is built with [Jekyll] and hosted on [GitHub Pages].

If you don't already have Ruby installed, refer to the [Ruby documentation] for installation instructions. You can then install Jekyll and Bundler with `gem install bundler jekyll`.


## Usage
ID to target URL mappings are defined using Markdown files in the `_links` directory. Each file represents a single link, where the filename is the ID of the link, and the target URL is defined using the `to` key in the YAML front matter.

In the following example, the link `/github` will redirect to `https://github.com/jerboa88`:

```yml
# _links/github.md
---
to: https://github.com/jerboa88
---
```

You can build the site using `bundle exec jekyll build` and serve it locally using `bundle exec jekyll serve`. When the site is built, [Jekyll] generates a page for each mapping, which redirects to the target URL using meta refresh redirects.

Refer to the [GitHub Pages with Jekyll] documentation for more information about hosting Jekyll sites on GitHub Pages.


## License
This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

The project logo is based on the `ruler-solid.svg` by [FontAwesome] and is licensed under [CC BY-SA 4.0].

[FontAwesome]: https://fontawesome.com/
[CC BY-SA 4.0]: https://creativecommons.org/licenses/by-sa/4.0/
[Jekyll]: https://jekyllrb.com/
[GitHub Pages]: https://pages.github.com/
[Ruby documentation]: https://www.ruby-lang.org/en/documentation/installation/
[GitHub Pages with Jekyll]: https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll
