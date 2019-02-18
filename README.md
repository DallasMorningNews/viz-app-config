# DMN Vizier app config

This repo contains the `.vizppconfig` file for publishing graphics to interactives.dallasnews.com using the [ai2html](http://ai2html.org/) and the [Vizier app](https://github.com/voxmedia/viz-app).

### Installation

1. Install Vizier (see https://github.com/voxmedia/viz-app#how-to-use-it)
2. In Vizier, go to "Preferences" > "Import preferences" and import [`tdmn.vizappconfig`](tdmn.vizappconfig)
3. If prompted, reinstall the ai2html script

### Updating this config

The available options for the config are well documented in https://github.com/voxmedia/viz-app/blob/master/example.vizappconfig.

Most of our configuration focuses on mapping "Illustrator" font names to CSS. For example, telling ai2html to render _PT Serif Italic_ as PT Serif with `font-weight: 400` and `font-style: italic`:

```json
{
  "aifont": "PTSerif-Italic",
  "family": "'PT Serif', Georgia, Times, serif",
  "weight": "400",
  "style": "italic"
}
```

To update the font mappings you'll need to first install the [aifontname.js script](https://github.com/newsdev/ai2html/tree/master/utilities) from the `ai2html` project. The script will give you the values for the `aifont` property in the config file. See http://ai2html.org/#using-fonts-other-than-arial-and-georgia for more information about how ai2html handles custom fonts.
