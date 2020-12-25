[![Stories in Ready](https://badge.waffle.io/citizenlabsgr/openbudgetgr.svg?label=ready&title=Ready)](http://waffle.io/citizenlabsgr/openbudgetgr)
[![Build Status](https://travis-ci.org/citizenlabsgr/openbudgetgr.svg?branch=master)](https://travis-ci.org/citizenlabsgr/openbudgetgr)

# Open Budget Grand Rapids

Open Budget Grand Rapids intends to promote a deeper understanding of the City of Grand Rapids Budget. We believe that this project will allow citizens, officials, and other stakeholders to engage in more informed dialogue about how the City of Grand Rapids currently works and how it should in the future.

## Getting Started

Use the following documentation to help you get started developing with this project.

### Prerequisites

These next items listed are necessary to develop this project on your local machine.

#### Yarn

This project uses Yarn package manager to install dependencies.

You can install Yarn on mac using the command below or by going to the [Yarn website](https://yarnpkg.com/).

```
brew install yarn
```

#### Harp

This site is built with the [Harp static site generator](http://harpjs.com/).

To install Harp globally, make sure you have `yarn` package manager installed, and then use the following commands

```sh
yarn global add harp
```

Harp was partially created to be a development tool for static sites, and includes minimal setup to start developing on the site locally

### Development

The [`/src`](./_src) directory is the working folder of this project, and contains all necessary code that is compiled in the static site.

To start developing, make sure you have all [prerequisites](#prerequisites) installed, and run the the following commands

```sh
# Go to the '_src' folder of the OpenBudget GR project
cd [repo-location]/_src

# Install required project dependencies
yarn install

# Run harp development server
harp server
```

The Harp server should tell you where to point your browser. Once you do that you should see the Open Budget Grand Rapids project that you can activey develop on.

## Documentation

Do not be afraid of updating the documentation if there is anyting that should be changed. Also please add to this documentation when a new feature is implemented.

### Creating & Editing Pages

- Page content is inserted into the `layout.jade` file (which includes basic header and footer snippets)
- Create your `.jade` file
- Add a link to the main nav in the appropriate place
- Add relevant metadata in `_data.json` (page title, page slug (url), ...)
- If your page uses custom page-specific css, add it to a new `.scss` partial and import it into the main stylesheet. (Make sure to namespace it the same way the others are.)

### Instructions for "Flow" Diagram Pages

* Flow pages are built off a template; copy one of the `*-budget-flow.jade` pages and update the content blocks as necessary.
* Data files must be placed in the `data/flow` directory. Follow the naming convention seen there or your files won't load properly. **Note: Two underscores required in data file name, ex: FY17__final.csv.** You also will need to point your page at the appropriate files as seen in the `get_datafiles` content block.
* The following columns are required in your datafile and their names should be normalized as seen here. Other columns should be removed to minimize the data download.
    - budget_year
    - department
    - fund_code
    - account_type (this should be the Expense/Revenue column, if there are duplicate names)
    - account_category
    - amount

### Instructions for "Treemap" Diagram Pages

* Treemap pages are built off a template; copy one of the `*-budget-tree.jade` pages and update the content blocks as necessary.
* Instructions for generating the necessary data files can be found [here](_treemap/README.md). Add them to the `data/tree/` directory following the naming convention seen in the existing files.
* Json files should follow this naming convention, Status (Final, Preliminary, Proposed, etc).Acount Type (Revenue or Expense).Budget Year.json. Examples: `Final.Expense.FY19.json` and `Final.Revenue.FY19.json`
* Update the `datafiles` content block with the appropriate metadata and file path for the data files you generated.

### Instructions for "Compare" page

* The Compare page is mainly powered by a React application. The source files are in `_src/js/compare/` and are are bundled with [Webpack](https://webpack.js.org/).
* When developing on the Compare page, run `yarn` to install all the necessary node dependencies and `yarn run watch` to watch the source files for changes and rebuild the asset bundles accordingly.
* The Compare page communicates with a separately maintained API to fetch its data. Documentation for that API can be found [in our wiki](https://github.com/openoakland/openbudgetoakland/wiki/API-Documentation).

### Creating/Updating Budget Timeline

The timeline is made using [TimelineJS](http://timeline.knightlab.com), an open-source tool that enables anyone to build visually rich, interactive timelines. Beginners can create a timeline using nothing more than a Google spreadsheet, like the one we used for the Timeline above. Experts can use their JSON skills to create custom installations, while keeping TimelineJS's core functionality.

The Google spreadsheet for the current [Budget Timeline used for Grand Rapids](https://grbudget.citizenlabs.org/budget-process.html) is a Citizen Labs' shared Google Sheet, can be [viewed here.](https://docs.google.com/spreadsheets/d/1jL2_7lJSgbLchJfAGWrST16ZxKe5Z-vbOfrAu14QyG8/edit?usp=sharing)

### Publishing Changes

Make changes on your personal fork or branch. If you have repo access, and your changes are ready for review, you can merge them into the development branch and publish to the staging site for review. You can also publish changes to your own server and merge to development afterwards.

## Contributing

Before making your first contribution to this project, please read the [Contribution Guide](./CONTRIBUTING.md)


## Data Sources

City of Grand Rapids, [MI Data Portal](https://www.grandrapidsmi.gov/GRData)

- [FY2017 Data](https://data.world/citizenlabs/city-of-grand-rapids-fy-2017-budget)
- [FY2018 Data](https://data.world/citizenlabs/city-of-grand-rapids-fy-2018-budget)

## Built With

- [Node](https://nodejs.org/en/)
- [Harp](http://harpjs.com/)
- [Jade](https://jade-lang.com/)
- [Sass](https://sass-lang.com/)
- [Bootstrap](https://getbootstrap.com/)
- [React](https://reactjs.org/)
- [Yarn](https://yarnpkg.com/en/)
- [Chartjs](https://www.chartjs.org/)
- [TimelineJS](http://timeline.knightlab.com)

## Skills
- Documentation
- Data collection
- Data visualization
- Civic Engagement
- Design
- Javascript
