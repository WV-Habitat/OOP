# Quarto presentation template

[![Deploy](https://github.com/habitat-nature/presentation_template/actions/workflows/build.yml/badge.svg)](https://github.com/habitat-nature/presentation_template/actions/workflows/build.yml)  [![html](https://img.shields.io/badge/read-html-blue)](https://habitat-nature.github.io/presentation_template/)

Build and deploy interactive slides with a single click.


## Getting Started

1. First click on the [Use this template](https://github.com/habitat-nature/presentation_template/generate) button to fork this repository, and check the option `Include all branches`.

2. Once the fork is completed, git clone the repo to your local machine

3. Install the R dependencies with the help of `renv` R package:

```r
# install.packages('renv')

# check with repo dependencies
renv::restore()
```

4. Edit your slides with Markdown flavor, with R, Python, and Julia integration. If you add new R packages in the slides, don't forget to run `renv::snapshot()` to update the dependencies list.

5. Add, commit, and push your changes to the remote GitHub repo and let the GitHub Actions render and deploy the presentation for you

6. Your presentation will be available on the `https://habitat-nature.github.io/<repo_name>/` URL when the Action is completed.

7. Enjoy 😎


### Render the presentation locally

To avoid pushing and waiting for the GitHub Action to render and deploy your presentation, it is recommended to keep rendering frequently as you edit your slides. This will avoid surprises (🐛) in the compilation process. To render the presentation locally, you need the [Quarto](https://quarto.org/docs/get-started/) client installed.

Render the HTML presentation by running the following code on Terminal:

```bash
quarto render index.qmd
```

Open the output `index.html` file.


## Getting involved

The layout of the presentation and color theme are still open for improvement. I tried my best to use some Habitat color palettes, but they are not easy to compose with. Any suggestion as an [issue](https://github.com/habitat-nature/presentation_template/issues) is welcome!

GitHub Actions uses Quarto to render the HTML output and send it to the `gh-pages` branch. We use [GitHub Pages](https://pages.github.com/) to host the files available on the `gh-pages` branch to the web. Because of our GitHub plan, we cannot host private websites for free, meaning that the presentation will be available to anyone with the URL link. An alternative is to use [Azure Static WebApp](https://azure.microsoft.com/en-us/products/app-service/static).

