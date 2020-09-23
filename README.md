# Assignment — D3 basic charts

This repository is your starting point for the assignment and includes the instructions below.

Link to your GitHub pages website: `[insert your hyperlink here]`

# Aim of the assignment

D3 is a valuable JavaScript library you can use to create custom data visualizations or to bind elements of the DOM to data in general. This assignment will help you learn the basics of D3 by creating two custom charts: a bar chart and a line chart.

# Instructions
Please look through **all** the materials below so you understand the setup instructions; how to run, organize, and submit your code; and our requirements for the visualization.

## Setup

**Under no circumstances should you be editing files via the GitHub user interface.** Do all your edits locally after cloning the repository. Commit major versions to your git repository.

1. In `README.md` (this file), modify the  `[insert your hyperlink here]` code to point to your GitHub pages URL. Ensure it is a clickable hyperlink. (Detailed instructions for GitHub pages [here](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Using_Github_pages).)
Commit your changes to your local repo and push to the remote GitHub repo.

2. In `index.html` update the GitHub repo URL with the URL of your repository. It is in the span with `id='forkongithub'`.

5. Ensure your code passes the [W3 validator](https://validator.w3.org/).

1. Clone this repository to your local machine. E.g., in your terminal / command prompt `CD` to where you want this the folder for this activity to be. Then run `git clone <YOUR_REPO_URL>`

1. `CD` or open a terminal / command prompt window into the cloned folder.

1. Start a simple python webserver. E.g., one of these commands:
    * `python -m http.server 8000`
    * `python3 -m http.server 8000`
    * `py -m http.server 8000`

    If you are using Python 2 you will need to use `python -m SimpleHTTPServer 8000` instead, but please switch to Python 3 as [Python 2 has been sunset as of 2020-01-01](https://www.python.org/doc/sunset-python-2/).

1. Wait for the output: `Serving HTTP on 0.0.0.0 port 8000 (http://0.0.0.0:8000/)`

1. Now open your web browser (Firefox or Chrome) and navigate to the URL: http://localhost:8000


## Organization

Here is an overview of the files and folders we provide for you in your repo.

### Root Files
* `README.md` is this explanatory file for the repo.

* `index.html` contains the main website content.

* `style.css` contains the CSS.

* `LICENCE` is your source code license.

### Folders
Each folder has an explanatory `README.md` file.

* `data` will hold the data file for the visualization.

* `favicons` contains the favicons for the web page. You shouldn't change anything here.

* `.github` contains [GitHub Actions](https://github.com/features/actions) ([docs](https://docs.github.com/en/actions)) which will automatically validate your HTML, CSS, and hyperlinks when you push. **Do not edit files here** except to create new `.yml` files for any additional actions you choose to add (you are not required to make any).

* `js` will contain all JavaScript files you write. E.g.,

  * `main.js` is the js code that you will have to fill in.

* `lib` will contain any JavaScript library you use. It currently includes D3. To ensure long-term survivability, **use the included D3 here rather than linking to [d3js.org](https://d3js.org) or some other CDN.** Likewise, put your other libraries here rather than loading them from elsewhere.

## Visualization and web page requirements

You must implement, commit, and push the web page following these requirements:

**Type**: ​One of the two visualizations you create has to be a bar chart, and the other has to be a line chart.

**Data**: ​In this assignment we give you the chance to find and select your own data. It can be related to your research, a subject of interest, a hobby, etc. **Please submit a copy of the raw data in your repository in the `data` folder.**

**Color**: ​Both plots must include color as a channel to encode some data.

**Interaction**: ​The expectation is that these plots are static except for the following requirement: at minimum one of your two plots should have a "details on demand" interaction, i.e., mouseover or click on bar/line to retrieve and display value.

**Overall excellence**: Make sure your plots follow the design guidelines and rules of thumb discussed in the reading as well as lecture. 

**Code comments**: Please make sure to add copious comments to your code to demonstrate your understanding of how your code works. Points will be deducted for little or no comments. 

**Descriptive prose**: Please include on your web page answers to the following questions for ​each visualization (a few sentences for each is sufficient):

1. Explain the dataset you choose to use and why you chose it.
*Make sure to include a clickable hyperlink to the original data source and include a copy of the data with your submission.*
2. Justify your encoding (i.e., bar, line) type for the data you visualize and why it is appropriate.
3. State for each visualization what colormap you used (categorical, diverging, sequential) and why. The colormaps used should make sense and follow the guidelines discussed in the reading as well as lecture.
4. Discuss the perceptual principles at play in your visualizations (e.g., pop-out effects, color theory, etc.) and how they positively support or enhance your plot.

**Academic integrity**:
You are welcome to use D3 tutorials or resources as a starting point for your code. However you must cite and reference the resources or sample code you use, ***including anything from [bl.ocks.org](bl.ocks.org/) or [stackoverflow](https://stackoverflow.com/)**.* Failure to properly cite and attribute code is a breach of academic honesty.  Also, per our syllabus, homework is an individual assessment and should be completed alone. You are welcome to ask fellow classmates and students for help and discuss the assignment, but the submission should be your own work. ***See [the syllabus](https://northeastern.instructure.com/courses/18721) for much more detail on our academic integrity policy and expectations.***

# Submission Instructions

1. Make sure your data is included in the repository on GitHub.

1. Ensure all visualization and prose required above is present in your GitHub page.

1. Submit the URL of  **your GitHub Classroom-generated repository** (same as the link you edited at the top) to [the associated assignment on Canvas](https://northeastern.instructure.com/courses/18721/assignments/573829). **Do not submit a link to a personal repository. It must be within our class GitHub organization.** 

# Tips and Tricks

## Resources

**There are different versions of D3**,  so make sure that the tutorials that you are using are up to date for either version 5 or version 6.*   

* [D3 Homepage](https://d3js.org)
* [D3 API Documentation](https://github.com/d3/d3/blob/master/API.md)
* [D3 Wiki Gallery](https://github.com/d3/d3/wiki/Gallery)
* [D3 Wiki Tutorials](https://github.com/d3/d3/wiki/Tutorials)
* [Tons of examples on bl.ocks.org](https://bl.ocks.org/)
* [D3 Tips and Tricks **v3.x (Warning: old version of D3)**](https://leanpub.com/D3-Tips-and-Tricks/read)

## Function/method chaining

D3, and this assignment, use [function chaining](https://en.wikipedia.org/wiki/Method_chaining) to apply several changes to the same visualization.

You don't have to use chaining.
E.g., instead of this:
```js
d3.select('body')
  .append('p')
    .text('Hello, world!');
```
you can write:
```js
var body = d3.select('body');
var p = body.append('p');
p.text('Hello, world!');
```

## JS statements: `let` vs. `var` vs. `const`

To make our code more modular, reusable, and error-free we should limit variable scope to the relevant parts of the code.
In part, we do this by using [`let` statements](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) instead of [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var) by default so as to not set global variables.
We can also use [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) to create read-only references.

## ES6 Arrow functions `=>`

Note that we can use [ES6 Arrow functions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions).
E.g., instead of writing `function(d){ return d.name; }` we write `d => d.name` or `d => { return d.name; }`. We would use the latter version with surrounding `{...}` when we need multiple lines of code vs. just a simple expression.

# Assignment Setup (For Instructors Only):

## Create Repo

1. Go to this year's staff GitHub organization.

1. Create the new repository using a meaningful name, consistent with the other assignments for this class and with Canvas.

1. Clone the repository locally.

1. Copy in the files from last year and make any necessary updates, *including assignment links to Canvas.*

1. Commit and push changes.

## GitHub Pages

It is necessary if using GitHub Classroom to set up GitHub pages for the students, as they do not have admin permissions on their repository. To do this, we need to create and move everything to the `gh-pages` branch and delete the `master` branch.

1. Commit the files to the `master` branch on GitHub.

1. `git branch gh-pages`

1. `git checkout gh-pages`

1. `git branch -D master`

1. `git push origin gh-pages`

1. On GitHub, go to `Settings`->`Branches` and set the default branch to `gh-pages`.

1. `git push origin :master`

## Template Repository

1. On GitHub, go to `Settings` and check the box for `Template repository` at the top. This makes GitHub Classroom copies much faster.

## GitHub Classroom

1. Create the assignment on GitHub Classroom.

1. Set the assignment title to be the same as on Canvas and consistent with the other assignments for this class.

1. Change the pre-set repository prefix so that it includes two dashes (--) between the type of assignment and the name of it. E.g., `in-class-programming--javascript` and `assignment--altair-and-jupyterlab-setup`.

1. Set the deadline (23:59 of the due day), make sure it matches the assignment on Canvas, and make sure it is Eastern time.

1. Make the repository Public.

1. Set the template repository (where this file is) as the starter code.

1. Enable feedback pull requests.

1. Update assignment.

1. Enable the assignment invitation URL.

1. In the Canvas assignment, replace the old assignment invitation URL and template repo link URLs with the new ones.