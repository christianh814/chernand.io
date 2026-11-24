# Website Powered by HUGO

This is the code for my personal website.

# Building

To build and publish. 

```shell
hugo -t sada
```

Then run

```shell
git add .
git commit -sam "some msg"
git push
```


# Content Page

The page at [/content](https://chernand.io/content/) is driven entirely by `[params.content]` in `config.toml`
(template: `layouts/_default/content-tabs.html`). Each `[[params.content.tabs]]` becomes a tab, and each
`[[params.content.tabs.items]]` under it becomes a bullet:

```toml
[[params.content.tabs]]
name = "Demos"

    [[params.content.tabs.items]]
    title = "My Demo"
    url = "https://example.com"
    description = "Optional, markdown supported"
```

Tabs can be linked directly with a hash, e.g. `https://chernand.io/content/#blogs`.
