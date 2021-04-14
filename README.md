# don8

_don8_ is a multi platform mobile app designed to connect charities with people who can help them. Post adverts with what your charity needs, and volunteers can see what you need, and where!   
We created _don8_ for our final project on the [Makers Academy](https://makers.tech/) course. In creating the app, we used the mobile MERN stack (MongoDB, Express, React Native & Node.js), which was entirely new to all of us. We had two weeks to complete the project, with a feature freeze on the second Wednesday, from which point we did not add any new functionality.

---

## Index

- [Demo](#demo)
- [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
- [Running the Program](#running-the-program)
- [Development Process](#development-process)
  * [Modelling](#modelling)
    + [User Stories](#user-stories)
      - [:white_check_mark: User Story 01](#white_check_mark-user-story-01)
      - [:white_check_mark: User Story 02](#white_check_mark-user-story-02)
      - [:white_check_mark: User Story 03](#white_check_mark-user-story-03)
      - [:white_check_mark: User Story 04](#white_check_mark-user-story-04)
      - [:heavy_exclamation_mark: User Story 05](#heavy_exclamation_mark-user-story-05)
      - [:heavy_exclamation_mark: User Story 06](#heavy_exclamation_mark-user-story-06)
    + [Diagramming](#diagramming)
  * [Test-Driven Design](#test-driven-design)
- [Minimum Viable Product](#minimum-viable-product)
  * [Wireframes](#wireframes)
- [Project Conclusions](#project-conclusions)
  * [Unfinished Features](#unfinished-features)
  * [Further Features](#further-features)
- [Built With](#built-with)
- [Authors](#authors)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Demo

<div align="center"><img src="https://github.com/JoshSinyor/don8/blob/main/docs/don8-demo.gif" width=300/><br>
<a href=https://www.youtube.com/watch?v=epjusmKqPDY>Full demo available here</a></div>


---


## Getting Started
This app is not currently hosted online, and can only be run locally. The instructions for how to do that on a Mac are given below, but please note that you will need some API keys in order for the app to function properly.

### Prerequisites

This project uses npm to manage packages, which is installed with Node.js. If you have Node.js installed, you should have npm installed. You can check if you have Node.js and npm installed by running `node -v` and `npm -v` in the command line respectively. If you don't have either installed, you can follow [these instructions](https://www.npmjs.com/get-npm).  

In order to run the app on your mobile phone, you will need to download the Expo Go app from the [Play Store](https://play.google.com/store/apps/details?id=host.exp.exponent&hl=en_GB&gl=US) or [App Store](https://apps.apple.com/gb/app/expo-go/id982107779).


### Installation

1. Download this repo to your local computer.
2. `cd` into the repo and run command `npm install` in the command line to install necessary packages.
3. Call `cd backend` and then another `npm install` in the command line to install necessary packages for the backend.
4. Create a `.env` file in the `backend` folder. This file should have three lines, `API_URL = /api/v1`, a `DATABASE_CONNECTION` line with our DB connection string, and a `secret` line, which you can set yourself.
5. Back in the root folder, create an `app.config.js` file with an [API key for google maps](https://developers.google.com/maps/documentation/javascript/get-api-key) which looks like:
```js
export default ({ config }) => {
  config['extra'] = {
    googleApi: 'your1api2for3google4maps5xyz'
  }
  return {
    ...config,
  };
};
```

---

## Running the Program

1. First start the backend. `cd backend` and then run `npm start`. This will allow API calls to the database to work.
2. In a separate terminal window, run `npm start` from the root folder. This will open an Expo window in your browser.
3. Scan the QR Code in the Expo web page from the Expo Go app (on Android) or the camera (on iOS).
4. Alternatively, if you have [Android Studio](https://developer.android.com/studio) or [XCode](https://developer.apple.com/xcode/) installed, you can run the app in an emulated phone by clicking the option from the Expo web page.

---

## Development Process

### Modelling

In order to aid us in our process, we did some modelling to guide us. This included some diagramming and user stories.

#### User Stories

We thought about the most important elements of how we wanted our app to work, and wrote these out as User Stories, as shown below. We used these to guide our development.

Actions are *italic*. Nouns are **bold**. Attributes of nouns are **_bold italics_**.

User stories marked :white_check_mark: are complete and those with :heavy_exclamation_mark: are incomplete

##### :white_check_mark: User Story 01

&nbsp;&nbsp;&nbsp;As a charity,<br>
&nbsp;&nbsp;&nbsp;So that I can advertise for donations of time or goods,<br>
&nbsp;&nbsp;&nbsp;I'd like to be able to post adverts.

##### :white_check_mark: User Story 02

&nbsp;&nbsp;&nbsp;As a donor,<br>
&nbsp;&nbsp;&nbsp;So that I can donate,<br>
&nbsp;&nbsp;&nbsp;I'd like to be able to see charities' adverts.

##### :white_check_mark: User Story 03

&nbsp;&nbsp;&nbsp;As a charity,<br>
&nbsp;&nbsp;&nbsp;So that I can manage my adverts,<br>
&nbsp;&nbsp;&nbsp;I'd like to be able to sign up as a charity.

##### :white_check_mark: User Story 04

&nbsp;&nbsp;&nbsp;As a charity,<br>
&nbsp;&nbsp;&nbsp;So that I can manage my adverts,<br>
&nbsp;&nbsp;&nbsp;I'd like to be able to log in and out.


##### :heavy_exclamation_mark: User Story 05

&nbsp;&nbsp;&nbsp;As a charity,<br>
&nbsp;&nbsp;&nbsp;So that I can manage my adverts,<br>
&nbsp;&nbsp;&nbsp;I'd like to be able to edit adverts.

##### :heavy_exclamation_mark: User Story 06

&nbsp;&nbsp;&nbsp;As a charity,<br>
&nbsp;&nbsp;&nbsp;So that I can manage my adverts,<br>
&nbsp;&nbsp;&nbsp;I'd like to be able to delete adverts.

#### Diagramming

The following diagram shows the flow of information as we first envisioned it for the Minimum Viable Product

![request_return_diagram](/docs/request_return_diagram.svg)

### Test-Driven Design

We intended to use TDD to drive our development process. However, having decided to use React Native, it proved difficult for us to run end-to-end testing, and we decided to focus more on picking up the syntax and skills needed for the new framework.
We tested our API routes and data models on the backend using Jest.

---

## Minimum Viable Product
* Charity can post what they need - either time or objects
* Volunteers can see what charities need

### Wireframes

The appearance of an MVP version of our program was projected to look something like as follows:

![wireframe_homepage](/docs/wireframe_homepage.svg) ![wireframe_new_request_page](/docs/wireframe_new_request_page.svg)


---

## Project Conclusions


### Unfinished Features

With more time, we would have liked to complete other features:

1. We ran out of time on the second Wednesday to complete a couple of features on the form for creating new adverts, which we wanted to include:
  - Picture upload - we have implemented the backend code but not the frontend yet
  - Auto-filling the location & contact details for the adverts from the logged-in charity details
2. Similarly, we have the backend routes to delete and edit adverts, but didn't consider it a priority to implement the frontend for these

### Further Features

As well as these unfinished features, there were other features we thought could be useful:
1. Contact charities directly through the app
2. Calendar showing when volunteers are needed
  * We debated this early on, but decided adding locations was more useful (and interesting for us to code!)
  * Would be able to search adverts by date
  * Volunteers would also be able to see a personalised calendar for adverts they had responded to
  * Similarly, charities would have public calendar of all volunteering opportunities available with them
3. Sign up as a volunteer
  * This would enable some of the other features - such as contacting charities

---

## Built With

This program's dependencies are:

- [Expo](https://docs.expo.io/)
- [React Native](https://reactnative.dev/)
- [MongoBD](https://www.mongodb.com/)

This program's development and test frameworks depend upon:

- [ESLint](https://eslint.org/)
- [Jest](https://jestjs.io/)
- [Cypress](https://www.cypress.io/)

---

## Authors

Proudly authored by [Oscar Bertrand](https://github.com/OscarB89), [Hugh Cavanagh](https://github.com/hacaravan), [Sean Edwards](https://github.com/bear99a9), [Joshua Sinyor](https://gist.github.com/JoshSinyor) and [Louis Wickremeratne](https://github.com/louiswicks).

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgements

- Table of contents generated with [markdown-toc](http://ecotrust-canada.github.io/markdown-toc/).
- Wireframes generated with [Figma](https://www.figma.com/).
- Diagrams generated with [Diagram.codes](https://www.diagram.codes/).
- API testing conducted with [Postman](https://www.postman.com/).
