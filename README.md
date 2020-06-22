[![Netlify Status](https://api.netlify.com/api/v1/badges/169b6b58-dbd7-4f25-a4fc-5906221132c8/deploy-status)](https://app.netlify.com/sites/planetscale/deploys) [![StackShare](http://img.shields.io/badge/tech-stack-0690fa.svg?style=flat)](https://stackshare.io/planetscale/docs-planetscale-com)

# Codebase for docs.planetscale.com

## Internals

- GatsbyJS
- Hosted and deployed via Netlify

## How to setup local development (on MacOS)

- Install homebrew (https://brew.sh/)
- Install yarn (MacOS: `brew install yarn`)
- Install netlify CLI (MacOS: `yarn global add netlify-cli`)
- Login to netlify via `netlify login`
- Git clone this repository (`git clone git@github.com:planetscale/website.git`)
- Switch to the repository's folder
- Link your repository to the planetscale.com project on netlify via `netlify link`
- `yarn install` to install all dependencies
- `netlify dev` to start a local server
- Open `http://localhost:8888` to access the local server instance

## How to add a new document

- All pages in the documentation are markdown files with a frontmatter block on the top. The frontmatter block defines the title of the page.
- When creating a new page, also create a corresponding entry in `meta.yml` file to define the category and position of the file in the table of contants. The title defined in the frontmatter is also used here to provide the text for the link in the table of contents.

Note: Although it is preferable to have a single title used across the table of contents and the document, there will be times when a longer title needs to be truncated to provide a succinct link text for the navigation list. You can use the smaller title in the frontmatter to enable this behavior.

Note: If you are adding a new document to any of the external repositories, you'd have to edit the `meta.yml` file in this repository as well.

## Notes

- The main website hosted on webflow embeds the greenhouse job board which uses a custom stylesheet. A copy of it is available in this repository at src/styles/greenhouse.css
- Favicons are generated via https://favicon.io/favicon-converter/
