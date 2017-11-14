# Full Stack JS Project
**`fullstack-js-03-views-and-static-files`**


## Context
You are going to build a full stack web application with node.js + React. In order to become familiar with how a node project works, you will be responsible for configuring the  initial major components of the project.  

- express server
- application routes
- **views [this assignment]**
- api layer
  - data access
  - data models (ORM)
  - RESTful routes


## The Assignment
For this assignment, we will focus on creating the **views** and serving static files

#### Requirements

- You will need to install EJS

- You will need to register the EJS view engine with express

- You will need to use `res.render()` to render the appropriate `.ejs` view inside the router

- You will need to serve static files (CSS files, JS files, and images) from the `/public` directory

- You will need to correctly write the `<link>` to the styles file (located at `public/css/style.css`) in the `home.ejs`, `about.ejs`, and `404.ejs` files.

## Setup Instructions

In Terminal:

```sh
# (1) navigate to your project--devjobs directory
cd ~/Documents/muktek/assignments/project--devjobs

# (2) Commit your changes from the previous demo
git commit -m 'committing work from part-02'

# (3) You will work on the part-03-views branch for this feature
git checkout -b part-03-views

# (4) Download + unzip files into public/
curl https://raw.githubusercontent.com/muktek/assignment--fullstack-js-03-views-and-static-files/master/publicfiles.zip

unzip publicfiles.zip -d ./public/


# (5) Download + unzip files into src/views
curl https://raw.githubusercontent.com/muktek/assignment--fullstack-js-03-views-and-static-files/master/viewfiles.zip  > viewfiles.zip

unzip viewfiles.zip -d ./src/views/

# (6) Delete the zip files
rm *.zip


```
