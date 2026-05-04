# quarto_apathesis

Quarto custom thesis format extension based on [**apaquarto** (by W. Joel Schneider)](https://github.com/wjschne/apaquarto).

Updated based on the thesis formatting guidelines of Faculty of Arts (Department of Psychology) of Charles University for use with [**Quarto Book**](https://quarto.org/docs/books/) format.

Warning: This was mostly vibecoded so there may be bugs.

## Installation

To automatically add extension to your thesis folder, run in terminal:

```
quarto add simon-jukl/quarto_apathesis
```

which downloads the extension from GitHub.

For more information, see Quarto documentation for [Managing Extensions](https://quarto.org/docs/extensions/managing.html).

## Configuration

Documentation is work in progress.

This extension is made to run "as is" as much as possible but there are many configuration options.

When you create a Quarto Book project (in Positron, RStudio etc.) and add the extension (see Installation above), set the custom format by editing your `_quarto.yml` file:

```
format:
  apathesis-html: default
  apathesis-pdf: default
```

The extension needs additional information in `_quarto.yml` to format the title page correctly:

```
thesis:
  university: "Název Univerzity"
  faculty: "Název Fakulty"
  department: "Název Katedry"
  type: "Seminární práce"      # "Bakalářská práce", "Diplomová práce" etc.
  # logo: "logo.pdf"
  # logo-width: "5cm"
  advisor: "Jméno Vedoucího"
  program: "Název Studijního Programu"
```

You can uncomment (i.e. remove `"#"`) the `logo:` line add faculty/university logo (if you have one in the thesis directory) and adjust its width.

You can also add `lang: cs` (for Czech) on a new line below.

Then you render by running

```
quarto render
```

in terminal.

### Change languages

Every built-in name or title should be changable.

(See `apalanguage.lua` file for changable titles and names.)

## Insides

This section is *work in progress*.

Here are going to be details on how the extension works under the hood.

For now, see `_extension.yml` file for more information.
