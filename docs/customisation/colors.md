# Changing colors

neocrym-sphinx-theme allows customising colors to fit your brand's identity, by using CSS variables. These can be declared directly in [`html_theme_options`][sphinx-html_theme_options], in your `conf.py`.

## How light and dark mode work

neocrym-sphinx-theme is in light mode by default, switching to the dark mode when requested by the user's browser (through `prefers-color-scheme: dark`).

As a consequence of this design, the dark mode inherits the variable definitions from the light mode, only overriding specific values to adapt the theme. While the mechanism for switching between light/dark mode is not configurable, the exact CSS variable definitions used in this process can be configured.

## Defining overrides for defaults

neocrym-sphinx-theme allows defining [CSS variables that overrides its default values](css-variables). The exact variable names to use can be found in neocrym-sphinx-theme's source code, where the [variable declarations](https://github.com/neocrym/neocrym-sphinx-theme/tree/main/src/neocrym_sphinx_theme/assets/styles/variables) are made.

This mechanism allows configuring nearly every facet of neocrym-sphinx-theme's design, including spacing between various items and the colors of nearly every component.

````{admonition} Example
Changing neocrym-sphinx-theme's blue accent (used for stylising links, sidebar's content etc) to a purple one:

```py
html_theme_options = {
    "light_css_variables": {
        "color-brand-primary": "#7C4DFF",
        "color-brand-content": "#7C4DFF",
    },
    "dark_css_variables": {
        "color-brand-primary": "#7C4DFF",
        "color-brand-content": "#7C4DFF",
    },
}
```
````

## Code block styling

neocrym-sphinx-theme does not directly handle highlighting of the code blocks. This is done by Sphinx, and is configurable using [`pygments_style`][sphinx-pygments_style] and `pygments_dark_style` in `conf.py`.

```py
pygments_style = "sphinx"
pygments_dark_style = "monokai"
```

```{note}
`pygments_dark_style` is neocrym-sphinx-theme-specific at this time.
```

[sphinx-html_theme_options]: https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-html_theme_options
[sphinx-pygments_style]: https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-pygments_style
