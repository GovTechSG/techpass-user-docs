# TechPass User Doc Repository
This is a documentation repository for TechPass, written for Documentation portal, using [docsify](https://docsify.js.org/#/). You can find out what docsify or markdown extensions are supported [here](https://stg.docs.developer.gov.sg/docs/public/238425294/doc-portal-publisher-guide/#/).

> The repository is currently in active development and contents will change rapidly.

## File Structure
All markdown files should live within the **/docs** folder. Each main section should be a separate markdown file by itself. If you have added a new main section, you should also update [_sidebar.md](docs/_sidebar.md) so that it will show up when the webpage is rendered.

All non-markdown files (i.e. images and sample code files) should live within the assets subfolder.

## Running Locally
### Setting Up
- Install docsify cli `npm --location=global install docsify-cli`
- Download this repository via `git clone`
- Run `docsify serve .`

#### Setting Up on zsh terminal
if you get `zsh:1: command not found: docsify` after npm install:
make sure you add `export PATH="$HOME/.npm-packages/bin:$PATH"` to the 1st line in your ~/.zshrc.
Then `source ~/.zshrc` to reload. Finally, test with `docsify --version`. You should see the following:
> docsify-cli version:
x.x.x


### Syntax Highlighting
The repository has been pre-configured to pull in the default Developer portal's styling for Documentations. (See [index.html](./index.html))

## Web Hosting
By default, once you commit and push any changes into github, the contents will be updated automatically.

## Contributing
Please fork the repository, make your changes and submit a Pull Request.
