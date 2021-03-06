---
title: Content visible and understandable without CSS
navigation: presentation-of-information
nav: menu-criteria
---

<header>
## Content visible and understandable without CSS
{: .article-header__title}
</header>

**Impact:** Strong to major

**Users mainly impacted:** Blind and severely visually impaired.

**RGAA criteria:** [Criterion 10.2 [A]](http://disic.github.io/rgaa_referentiel_en/criteria.html#crit-10-2) - [Criterion 10.3 [A]](http://disic.github.io/rgaa_referentiel_en/criteria.html#crit-10-3)
{: .criteria }

### Explanation

#### Content visible without CSS

Information content inserted via CSS may not be retrieved by screen readers or voice magnifying systems.

##### Background images

Background images inserted in CSS (`background` or `background-image`) must never be informative.

*It is possible to transmit the information conveyed by the image via hidden text, however this technique is not recommended. This technique does not allow some devices to read content such as some high contrast modes.*

##### Content generated by CSS

The CSS property `content` allow us to display content.
However, even if this content is visible with CSS enabled, it is no longer visible when CSS is disabled. So, you should never use `content` to insert text content.

Content and the pseudo-selectors `::after` and `::before` are very often used for the insertion of icons using icon fonts. If the icons are purely decorative, then there is no accessibility problem. However, if they are icons that carry information, then you must ensure that an alternative means of retrieving this information is available.

A common mistake is to create a link with an icon generated by CSS. In this case the link is empty.

###### Poor practice

In this example the information is only visual. Users using voice synthesis will not have the information.

```html
<a href="#"><span class="fa fa-home"></span></a>
```

```css
.fa-home::before {
    content: "\f015";
}
```

<div class="tip">
<svg role="img" aria-label="Tip" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 352 512" width="28" height="40"><title>Tip</title><path d="M96.06 454.35c.01 6.29 1.87 12.45 5.36 17.69l17.09 25.69a31.99 31.99 0 0 0 26.64 14.28h61.71a31.99 31.99 0 0 0 26.64-14.28l17.09-25.69a31.989 31.989 0 0 0 5.36-17.69l.04-38.35H96.01l.05 38.35zM0 176c0 44.37 16.45 84.85 43.56 115.78 16.52 18.85 42.36 58.23 52.21 91.45.04.26.07.52.11.78h160.24c.04-.26.07-.51.11-.78 9.85-33.22 35.69-72.6 52.21-91.45C335.55 260.85 352 220.37 352 176 352 78.61 272.91-.3 175.45 0 73.44.31 0 82.97 0 176zm176-80c-44.11 0-80 35.89-80 80 0 8.84-7.16 16-16 16s-16-7.16-16-16c0-61.76 50.24-112 112-112 8.84 0 16 7.16 16 16s-7.16 16-16 16z"/></svg>
Consult the page on good techniques for [integrating icons in an accessible way](../../techniques/accessible-icons.html).
</div>

#### Content understandable without CSS

In CSS, it is possible to change the order in which the elements are displayed. Inconsistencies in the order in which the content appears in the code can lead to misunderstandings for blind and partially sighted people who access the content through a screen reader.

For example a feature to share an article that is before the article title. In this case it is difficult to know what you are sharing. In this case it is necessary to position in the source code the feature after the title or to make the feature understandable out of context.
