---
title: Color contrast
navigation: colors
nav: menu-criteria
---

<header>
## Color contrast
{: .article-header__title}
</header>

**Impact:** High to major

**Users mainly impacted:** Visually impaired

**RGAA criteria:** [Criterion 3.2](https://www.numerique.gouv.fr/publications/rgaa-accessibilite/methode/criteres/#crit-3-2) - [Criterion 3.3](https://www.numerique.gouv.fr/publications/rgaa-accessibilite/methode/criteres/#crit-3-3)
{: .criteria }

### Explanation

For a user who has difficulty perceiving contrasts, some writings may be impossible to read if the writing colour is not sufficiently contrasted with the background colour.

These contrasts concern:

* the text and the text present in the image;
* the interface components or graphical elements that convey information

There are values that provide sufficient minimum contrast for a large proportion of users with color perception difficulties.

To evaluate the contrasts of the elements you insert, you can use tools:

* [**Color Contrast Analyzer**](https://developer.paciellogroup.com/resources/contrastanalyser/) thanks to a pipette, you can go and pick colours from all document formats (web, office, video, etc.) for analysis;
* Lighthouse in Google **Chrome** browser allows you to quickly check your web page for text content.
* Contrast tools is available in Mozilla **Firefox** developer tools in accessibility tab.

#### Text without bold

* Less than 24px: The contrast ratio is at least 4.5:1.
* Greater than or equal to 24px: The contrast ratio is at least 3:1.

#### Text with bold

* Less than 18.5px: The contrast ratio is at least 4.5:1.
* Greater than or equal to 18.5px: The contrast ratio is at least 3:1.

#### The interface components or graphical elements that convey information

The contrast ratio is at least 3:1 of:

* The colors of an interface component in its different states and the background color.
* The different colors composing a graphic element and its background color.
* The different colors composing a graphic element.

#### Special case
* The text is part of a logo or brand name of an organization or company.
* The text or graphic element is purely decorative.
* The text or graphical element is part of an interface element on which no action is possible (e.g. a button with the disabled attribute).

#### Testing Color Contrast & Simulating Color Blindness with the Firefox Accessibility Inspector

<div class="video"><iframe title="Testing Color Contrast & Simulating Color Blindness with the Firefox Accessibility Inspector" width="560" height="315" src="https://www.youtube.com/embed/eBefjaWud-M" frameborder="0" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></div>

If you don't see these tools, go to `about:config` and search the property "gfx.webrender.all". This property must be to `true`.
