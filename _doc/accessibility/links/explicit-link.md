---
title: Explicit link
navigation: links
nav: menu-criteria
---

<header>
## Explicit link
{: .article-header__title}
</header>

**Impact:** Major

**Users mainly impacted:** Blind, severely visually impaired, visually impaired, motor impaired.

**RGAA criteria:** [Criterion 6.1 [A]](http://disic.github.io/rgaa_referentiel_en/criteria.html#crit-6-1)
{: .criteria }

### Explanation

A link allows you to navigate between the pages of a site or to link to another site. A link is defined by two important elements:

* its link text, the text visible and clickable by users;
* its context

<div class="important">
<svg role="img" aria-label="Important" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" width="40" height="36"><title>Important</title><path d="M569.517 440.013C587.975 472.007 564.806 512 527.94 512H48.054c-36.937 0-59.999-40.055-41.577-71.987L246.423 23.985c18.467-32.009 64.72-31.951 83.154 0l239.94 416.028zM288 354c-25.405 0-46 20.595-46 46s20.595 46 46 46 46-20.595 46-46-20.595-46-46-46zm-43.673-165.346l7.418 136c.347 6.364 5.609 11.346 11.982 11.346h48.546c6.373 0 11.635-4.982 11.982-11.346l7.418-136c.375-6.874-5.098-12.654-11.982-12.654h-63.383c-6.884 0-12.356 5.78-11.981 12.654z"/></svg>
For a link **to be explicit**, it is necessary that the **link text** or the ***link context*** make it possible to understand its **function and destination**.
</div>

A link must be explicit by itself (its link text alone) or through its context :

#### By itself (accessible name)

The accessible name is the text rendered by assistive technologies.

The accessible name is obtained in the following order:
* Passage of text associated by the attribute `aria-labelledby`;
* Otherwise, content of the `aria-label` attribute;
* Otherwise, link text;
* Otherwise, on link image, content of `alt`;
* Otherwise, content of the attribute `title`.

For example:
* In case of joint presence of an `aria-label` attribute and an `aria-labelledby` attribute, it is the text passage referenced by the `aria-labelledby` attribute that must be considered as the accessible name;
* If there is both an `aria-label` attribute and content in the link, it is the content of the `aria-label` attribute that must be considered as the accessible name.

#### By itself added by its context

*   The content of the sentence enclosing the link;
*   The content of the paragraph (`p` tag) containing the link;
*   The content of the list item (`li` tag), or the content of a parent list item (`li` tag) of the list item, containing the link;
*   The content of the heading (`hx` tags) that is the closest ascendant of the link;
*   The content of the table header cell(s) (`th` tags) associated with the table data cell (`td` tag) containing the link;
*   The content of the table data cell (`td` tag) containing the link;

<div class="tip">
<svg role="img" aria-label="Tip" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 352 512" width="28" height="40"><title>Tip</title><path d="M96.06 454.35c.01 6.29 1.87 12.45 5.36 17.69l17.09 25.69a31.99 31.99 0 0 0 26.64 14.28h61.71a31.99 31.99 0 0 0 26.64-14.28l17.09-25.69a31.989 31.989 0 0 0 5.36-17.69l.04-38.35H96.01l.05 38.35zM0 176c0 44.37 16.45 84.85 43.56 115.78 16.52 18.85 42.36 58.23 52.21 91.45.04.26.07.52.11.78h160.24c.04-.26.07-.51.11-.78 9.85-33.22 35.69-72.6 52.21-91.45C335.55 260.85 352 220.37 352 176 352 78.61 272.91-.3 175.45 0 73.44.31 0 82.97 0 176zm176-80c-44.11 0-80 35.89-80 80 0 8.84-7.16 16-16 16s-16-7.16-16-16c0-61.76 50.24-112 112-112 8.84 0 16 7.16 16 16s-7.16 16-16 16z"/></svg>
* If I look at the text of my links, do I understand where I'm going by clicking on them?
* Avoid generic link text such as: click here, here, read more, visit this page, download...
</div>
