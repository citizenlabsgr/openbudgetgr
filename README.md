[![Stories in Ready](https://badge.waffle.io/citizenlabsgr/openbudgetgr.svg?label=ready&title=Ready)](http://waffle.io/citizenlabsgr/openbudgetgr)
[![Build Status](https://travis-ci.org/citizenlabsgr/openbudgetgr.svg?branch=master)](https://travis-ci.org/citizenlabsgr/openbudgetgr)

# Open Budget Grand Rapids

Open Budget Grand Rapids intends to promote a deeper understanding of the City of Grand Rapids Budget. We believe that this project will allow citizens, officials, and other stakeholders to engage in more informed dialogue about how the City of Grand Rapids currently works and how it should in the future.

## Getting Started

Use the following documentation to help you get started developing with this project.

### Prerequisites

These next items listed are necessary to develop this project on your local machine.

#### Yarn

This project uses Yarn package manager to install dependencies. Go to the [Yarn website](https://yarnpkg.com/) in order to learn how to install it.

#### Harp

This site is built with the [Harp static site generator](http://harpjs.com/). Harp can be used to develop on the site locally with minimal setup.

To install Harp globally, make sure you have `yarn` package manager installed, and then use the following commands

```sh
yarn global add harp
```

### Development

The [`/src`](./_src) directory is the working folder of this project, and contains all necessary code that is compiled in the static site.

To start development of this project, make sure that you have all of the [prerequisites](#prerequisites), and run the the following commands

```sh
# Go to the '_src' folder of the OpenBudget GR project
cd [repo-location]/_src

# Install required project dependencies
yarn install

# Run harp development server
harp server
```

## Contributing

Before making any changes please consider reading the [Contribution Guide](./CONTRIBUTING.md). This document sets a guideline for how to best contribute to parts of the OpenBudget GR project.

The easiest way you can make a pull request is by making changes to the documentation or README files. Otherwise you should check out the [issues](https://github.com/citizenlabsgr/openbudgetgr/issues) and see if there are any that you can work on.

### Maintainers

Project maintainers have write access to this project are responsible for reviewing and merging all pull requests.

The current maintainers of this project are:
* [@allen](https://citizenlabs.slack.com/messages/@allen/)
* Jace B

It is recommended to reach out to them if you need any help getting started with this project. They can be found on the [CitizenLabs Slack](#slack)

Updates to documentation or the [README](/README.md) make for a great first pull request.

### Slack

You can talk with Citizen Labs and the maintainers of this project through [Slack](https://join.slack.com/t/citizenlabs/shared_invite/enQtNTQ0Mjk1NjQ3NjcxLTI0YTRhOWYzZGY4MTBjMWU0NzU0MGY1OTU3Y2YwYTkxZGI2ZTVhMjQwYWEwMWI4NGUwYjI3OTE3Y2NlNTdhNzU). The specific channel name for this project is `#project-openbudgetgr`

## Data

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

## Skills
- Documentation
- Data collection
- Data visualization
- Civic Engagement
- Design
- Javascript
