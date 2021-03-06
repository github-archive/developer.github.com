---
title: Miscellaneous
---

# Miscellaneous

This is a miscellaneous set of APIs which provide access to top level {{ site.data.variables.product.product_name }} resources and info.

## [Emojis][]

The [Emojis API][Emojis] lets you list all the emojis available to use on
{{ site.data.variables.product.product_name }}.

## [Gitignore][]

The [Gitignore API][Gitignore] gives you access to the available gitignore
templates.

## [Markdown][]

The [Markdown API][Markdown] lets you render Markdown documents.

## [Meta][]

{% if page.version == 'dotcom' %}

The [Meta API][Meta] provides information about GitHub.com (the service).

{% else %}

The [Meta API][Meta] provides information about your
organization's [GitHub Enterprise](https://enterprise.github.com/) installation.

{% endif %}

{% if page.version == 'dotcom' %}

## [Rate Limit][]

The [Rate Limit API][Rate Limit] lets you check your current rate limit
status at any time.

{% endif %}

## [Licenses][]

The [Licenses API][Licenses] returns information about open source licenses or under what license, if any a given project is distributed.

[Emojis]: /v3/emojis
[Gitignore]: /v3/gitignore
[Markdown]: /v3/markdown
[Meta]: /v3/meta
[Rate Limit]: /v3/rate_limit
[Licenses]: /v3/licenses
