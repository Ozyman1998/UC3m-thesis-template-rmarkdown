# UC3m-thesis-template-rmarkdown
## A bit of history
I hate Microsoft PowerPoint and Word (especially Microsoft Word). After a few fierce discussions with a thesis collaborator due to incompatibilities between Word and LibreOffice, images movng out of place,... common ms word stuff, I decided to seek for something like Overleaf but for presentations.

Hence I decided to make my PhD defense presentation in HTML format using RStudio + Quarto + Revealjs. Every computer can open an HTML file in a browser — no matter if it's Firefox, Chrome (don't use this), or anything else. No PowerPoint license needed, no LibreOffice rendering bugs, no compatibility nightmares... Only your rstudio and a navigator. 
Obviously i found a way to make a pdf output of the presentation. I am not to idiot to aknowledge spanish university dislikes changes and strange formats. 

The result is a clean, professional presentation template with four corner logos — designed specifically for PhD defenses at UC3M but adaptable to any institution. You only have to change the png logos and any information you need. 
## What you get
- Four corner logos (one per institution/collaborator)
- Custom title slide with candidate name, director, program and date
- Clean white theme with custom fonts and colors
- Works on any computer with a browser — zero installation needed
- Fully self-contained single HTML file when rendered with `embed-resources: true`
- Compatible with wireless presentation clickers (just arrow keys)
- A few options (just click in the button-left logo)
    - ful screen
    - speaker view (wiht a time counter and a view of the following slides) - useful for rehersal
    - slide overview
    - pdf export
    - scroll view mode
## Requirements

- R (https://cran.r-project.org)
- RStudio (https://posit.co/download/rstudio-desktop)
- Quarto (https://quarto.org/docs/download)
- R packages: `install.packages("rmarkdown")`
On Linux you may also need (obviously i use linux, death to microsft)
```bash
sudo apt install libuv1-dev
```
## How to use it

1. Clone or download this repository
2. Replace the logo files in the folder with your own (PNG with transparent 
   background recommended)
3. Update the logo filenames in the `<script>` block inside `phd_defense.qmd`
4. Edit your title slide details (name, director, program, date) in the same 
   script block
5. Add your slides using `##` headings
6. Render with `Ctrl + Shift + K` in RStudio
## Logo tips

- Use PNG format with transparent background
- To remove white backgrounds from logos use ImageMagick:
```bash
convert logo.png -fuzz 10% -transparent white logo_transparent.png
```
- For EPS logos (common in universities) convert first:
```bash
inkscape logo.eps --export-type=png --export-dpi=300 -o logo.png
```
## Presenting

- Open the rendered HTML file in any browser
- Press `F11` for fullscreen
- Use arrow keys or a wireless clicker to advance slides
- Press `S` for speaker notes view
- Press `F` for Revealjs fullscreen mode

## Note on logos

This template does not include any institutional logos. Add your own and make sure you comply with your institution's logo usage policy.
