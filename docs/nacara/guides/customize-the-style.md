---
title: Style your application
layout: standard
---

Nacara allows you to customize your application style to match your design.

## Main file

The main file for styling your application is `docs/style.scss` or `docs/style.sass`.

Try editing this file and see the site being updated.

## Special folder

When you website become bigger you will want to split your `style` file into smaller files.

Nacara has specials folders to deal with that:

- `docs/scss`: use this folder is you are using SCSS to write your style
- `docs/sass`: use this folder is you are using SASS to write your style

When one of the files of these folders changes, Nacara will recompile your `docs/style.scss` or `docs/style.sass`.

Let's try it out, we are going to assume you use SCSS but the process is the same when using SASS.

<ul class="textual-steps">

<li>

Add the following code to the page you created earlier `docs/tutorial/my-page`

```html
<div class="my-text">

This text should be bold and red.

</div>
```

</li>

<li>

Create a file `docs/scss/my-style.scss`

```scss
.my-text {
    color: $danger;
    font-weight: $weight-bold;
}
```

Because default layout of Nacara use Bulma, you have access to [Bulma variables](https://bulma.io/documentation/customize/variables/).

</li>

<li>

Include your file in `style.scss`

```scss
@import './scss/my-style.scss';
```

</li>

</ul>
