# Full Stack JS Project - DevJobs - 02 - Express Router + EJS Views

## Context
You are going to build a full stack web application with node.js + React. In order to become familiar with how a node project works, you will be responsible for configuring the  initial major components of the project.  

- express server
- **application routes [this assignment]**
- **views [this assignment]**
- api layer
  - data access
  - data models (ORM)
  - RESTful routes


## The Assignment
For this assignment, we will focus on creating the **express router** and the **express views**.

### Part A -- Router
Configure the express router to serve the following routes:

```
/                  : home.html
/about             : about.html
/api/jobs          : json - jobsData
/api/companies     : json - companies

* No Match *       : 404.html
```

**Requirements:**

- you must create a `routers/` directory in `src/`

- you must create 2 router files in the `routers/` directory:
  - `pageRouter.js`
  - `apiRouter.js`

- you must initialize the `express.Router()` in the 2 router files, export the routers in `module.exports`
  - for `pageRouter.js`
    - `/` route should send the `home.html`
    - `/about` route should send the `about.js`
  - for `apiRouter.js`
    - `/api/jobs` route should send _`jobsData`_
    - `/api/companies` route should send _`companiesData`_ (see below)

- the routes must be imported in `server.js` and passed correctly to `app.use(....)`

- you must use `express.static`  to serve static `.css` and `.js` files.

  ```js
  app.use(express.static(__dirname + '/public'));
  ```


## Setup Instructions

In Terminal:

```sh
# (1) navigate to your project--devjobs directory
cd ~/Documents/muktek/assignments/project--devjobs

# (2) Commit your changes from the previous demo
git commit -m 'committing work form 01'

# (3) You will work on the part-02-router branch for this feature
git checkout -b part-02-router

# (4) Download the public files and unzip them into `public/`
curl ...
unzip publicfiles.zip -d ./public/

# (5) Remove the zip files
rm *.zip



```

## Extra

#### `_jobsData_`
```js
[
  {
    title: 'SQL Server Administrator - Postgres',
    description: 'Bring to the table win-win survival strategies to ensure proactive domination. User generated content in real-time will have multiple touchpoints for offshoring.',
    location: 'Guadalajara',
    salary: 27000,
    fullTime: true,
    companyId: 1
  },
  {
    title: 'UX Engineer',
    description: 'Override the digital divide with additional clickthroughs from DevOps. Leverage agile frameworks to provide a robust synopsis for high level overviews.',
    location: 'Monterrey',
    salary: 35000,
    fullTime: true,
    companyId: 1
  },
  {
    title: 'API Architect',
    description: 'Collaboratively administrate turnkey channels whereas virtual e-tailers. Objectively seize scalable metrics whereas proactive e-services.',
    location: 'Ciudad de Mexio',
    salary: 39000,
    fullTime: true,
    companyId: 2
  },
  {
    title: 'Mid-Level Front End Engineer',
    description: 'Interactively coordinate proactive e-commerce via process-centric "outside the box" thinking. Completely pursue scalable customer service through sustainable potentialities.',
    location: 'Ciudad de Mexico',
    salary: 21000,
    fullTime: false,
    companyId: 2
  }
]
```

#### _`companiesData`_
```js
[
  {
    name: 'Company ABC',
    description: 'Energistically network alternative technology deploying impactful partnerships.',
    imageLink: 'http://www.tinygraphs.com/labs/isogrids/hexa16/nsuaio',
    location: 'Guadalajara'
  },
  {
    name: 'Lossless Enterprises',
    description: 'Quickly strategizing team driven "outside the box" thinking.',
    location: 'Ciudad de Mexico',
    imageLink: 'http://www.tinygraphs.com/labs/isogrids/hexa16/8282',
  }
]
```
