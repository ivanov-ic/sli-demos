# Solids, Liquids and Interfaces — interactive demos

Eight interactive demos for Lectures 5 to 8 of the second-year module *Solids, Liquids and
Interfaces*, Department of Chemistry, Imperial College London.

Each demo is a single HTML file with no dependencies at all: no scripts, stylesheets, images
or fonts are fetched from anywhere. Open one from a web address, from a USB stick, or from a
folder on a lecture-theatre machine and it behaves the same.

| | Demo | Lecture |
|---|---|---|
| 5.1 | [Ionic atmosphere and the Debye length](l5-1-ionic-atmosphere.html) | Ions in solution |
| 5.2 | [Coulomb against thermal energy](l5-2-coulomb-thermal.html) | Ions in solution |
| 6.1 | [Three models against the measurements](l6-1-activity-models.html) | Non-ideality |
| 6.2 | [Counting the free water](l6-2-free-water.html) | Non-ideality |
| 7.1 | [The ion race](l7-1-ion-race.html) | Migration and conductivity |
| 7.2 | [Extrapolating to the limiting value](l7-2-extrapolation.html) | Migration and conductivity |
| 8.1 | [The diffusion clock](l8-1-diffusion-clock.html) | Diffusion and thermal gradients |
| 8.2 | [Thermophoresis and an MST titration](l8-2-thermophoresis-mst.html) | Diffusion and thermal gradients |

`javascript-test.html` is a two-kilobyte page that reports whether scripts are allowed to run
wherever it is opened. Use it to check a virtual learning environment before blaming a demo.

## Embedding in Canvas

Canvas blocks JavaScript inside files uploaded to its own Files area, so the demos have to be
served from here and pulled in with an iframe. On a Canvas page, switch to HTML view and paste:

```html
<iframe src="https://USERNAME.github.io/sli-demos/l5-1-ionic-atmosphere.html"
        width="100%" height="1550" style="border:1px solid #ddd;border-radius:6px"
        title="Ionic atmosphere explorer" allowfullscreen></iframe>
```

Save from HTML view. Switching back to the rich editor first strips the iframe attributes.
Each page detects that it is inside a frame and trims its layout to suit; 1550 px is enough
at the widths a Canvas content column normally gets.

## Crawlers and machine reading

`robots.txt` asks ordinary search engines to index these pages and asks the crawlers
that gather text for training generative models to leave them alone. Every page also
carries `<meta name="robots" content="index, follow, noai, noimageai">` in its head.

Two things to know. Both are requests rather than controls: a crawler that ignores
them is not prevented from reading anything. And robots.txt is only ever read from the
root of a host, so on a project page at `USERNAME.github.io/sli-demos/` the file in
this repository is never fetched. To make it bite, copy it into a repository named
`USERNAME.github.io`, which serves the root of that host, or use a custom domain. The
`meta` tag in each page works either way, which is why it is there as well.

To keep the demos out of search results entirely, change `index, follow` to
`noindex, nofollow` in the head of each page.

## Licence

Copyright © 2026 Aleksandar P. Ivanov, Department of Chemistry, Imperial College London.

These demos are licensed under
[Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International](https://creativecommons.org/licenses/by-nc-nd/4.0/)
(`CC-BY-NC-ND-4.0`). You may copy and redistribute them in any medium or format, for
non-commercial purposes, with appropriate credit. You may not distribute modified versions.
The full legal code is in [LICENSE](LICENSE).

Teaching use at another institution is non-commercial and so is permitted, with credit. If you
want to adapt a demo rather than use it as it stands, or use one commercially, please ask.

The typefaces embedded in each HTML file are licensed separately under the SIL Open Font
License 1.1 and are not covered by the licence above. See [OFL.txt](OFL.txt). IBM Plex Sans
and IBM Plex Mono, Copyright IBM Corp. Source Serif 4, from the Adobe Source Serif project.

### Why one licence covers the code too

Each demo is a single self-contained page: the physics, the prose, the layout and the
script that draws it are one artefact, and there is no sensible line between the worked
example and the code that evaluates it. Splitting the repository into a content licence
and a software licence would create a boundary that neither of them could describe.

Creative Commons advises against CC licences for software, on the grounds that they carry
no patent grant and say nothing about source against binary form. Neither point bites
here: nothing is compiled, nothing is linked against, and no patent is in play. What would
bite is the reverse choice, because no open-source licence can express these terms at all.
Non-commercial use and no-derivatives both fail the Open Source Definition by design, so
every licence approved by the Open Source Initiative is more permissive than intended.
