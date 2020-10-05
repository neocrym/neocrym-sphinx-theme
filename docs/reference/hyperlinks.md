# Hyperlinks

Hyperlinks are useful!

```{furo-demo}
Hyperlinks can take various forms, so here's a list of them:

- standalone hyperlink: <https://python.org/>
- hyperlink using references: [link][markdown-external-hyperlink]
- hyperlink with inline URL: [link](https://python.org/)
- hyperlink to a different page: [link](../quickstart)
- hyperlink to a specific API element: {class}`pathlib.Path`

[markdown-external-hyperlink]: https://python.org/

+++

Hyperlinks can take various forms, so here's a list of them:

- standalone hyperlink: https://python.org/
- hyperlink using references: link_ (this is borked due to a MyST bug)
- hyperlink with inline URL: `link <https://python.org/>`_
- hyperlink to a different page: :any:`link <../quickstart>`
- hyperlink to a specific API element: :class:`pathlib.Path`

.. _link: https://python.org/
```