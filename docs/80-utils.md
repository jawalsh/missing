---
title: Utilities
url: ./utils/
---

# Utilities

For the minor alterations to the default look that make all the difference,
missing.css has a collection of classes and custom elements.

[[toc]]

## Visually hidden content

<dfn>`.vh`</dfn>, <dfn>`<v-h>`</dfn>
:   Visually hide a content without hiding it from assistive software.

## Container

`<div class="container">`

The <dfn>`.container`</dfn> class imposes a maximum width on an element and 
centers it. The `<main>` element does the same, but carries semantic baggage
that might not be appropriate for all contexts.


## Density {#density}

The density utilities set the <dfn>`--density`</dfn> [CSS variable][], which
controls the amount of spacing between elements. The default value of
`--density` is `1`, which means the spacing between paragraphs is
equal to the height of 1 line.

We provide three utility classes that set `--density`:

| Class                     | Density                                    |
|---------------------------|--------------------------------------------|
| <dfn>`.packed`</dfn>      | `--density` = 0                            |
| <dfn>`.crowded`</dfn>     | `--density` = 0.5                          |
| <dfn>`.dense`</dfn>       | `--density` = 1 (same as default)          |
| <dfn>`.spacious`</dfn>    | `--density` = 2                            |
| <dfn>`.airy`</dfn>        | `--density` = 3                            |
| <dfn>`.autodensity`</dfn> | sets density based on viewport width       |

You can set `--density` yourself in inline styles or your own CSS:

<figure>
<figcaption>Setting <code>--density</code> with inline styles</figcaption>

  ~~~ html
  <section id="tagline" style="--density: 2">
    <h1>So easy, even a programmer can do it.</h1>
    <p>
        missing.css makes it easy to ship beautiful applications without
        locking yourself into classless libraries.
    </p>
  </section>
  ~~~
</figure>

<figure>
<figcaption>Setting <code>--density</code> in a stylesheet</figcaption>

  ~~~ css
  .link-embed {
      --density: .5; /* Embeds shouldn't take up too much space */
  }
  ~~~

</figure>


## Typography

<dfn>`.bold`</dfn>
:   Sets text in boldface.

<dfn>`.italic`</dfn>
:   Sets text in italics. Nested italic elements
    (`em`, `cite`, `dfn`, `var`, `i`, `address`) will be set in roman instead.

<dfn>`.allcaps`</dfn>
:   Sets text in all caps and adds appropriate letter spacing.

<dfn>`.monospace`</dfn>
:   Renders the text in the monospace font (`--font-mono`).


## Masquerades

The following classes can be used to make one element look like another:

- <dfn>`.<h1>`</dfn>
- <dfn>`.<h2>`</dfn>
- <dfn>`.<h3>`</dfn>
- <dfn>`.<h4>`</dfn>
- <dfn>`.<h5>`</dfn>
- <dfn>`.<h6>`</dfn>
- <dfn>`.<button>`</dfn>
- <dfn>`.<a>`</dfn>
- <dfn>`.<small>`</dfn>
{role="list" .tool-bar}

<figure>

  ~~~ html
  <a class="<button>" href="/cta">Call to action</a>
  ~~~

  <p><a class="<button>" href="#">Call to action</a>


</figure>


## Reset

Use the <dfn>`.all:initial`</dfn> class to reset all CSS properties on an
element and return it to its browser-default styles.


[CSS variable]: /docs/variables
