# README

This README would normally document whatever steps are necessary to get the
application up and running.

* Switching to rails 6.1.4.4

$ rvm gemset create rails6
$ rvm gemset use rails6
$ gem install rails -v 6.1.4.4
$ rails -v
=> Rails 6.1.4.4

* Database creation
$ rails new hello-world -d postgresql -T
$ cd hello_world
$ rails db:create
$ rails s
Go to browser, type localhost:3000, should see the rails global community image

* React components
$ bundle add react-rails
$ rails webpacker:install:react
$ rails generate react:install
$ rails generate react:component App
Go to text editor, follow path to see App.js file, app/javascript/components/App.js

* Add html tags to App.js
`import React, { Component } from 'react'

class App extends Component {
  render() {
    return(
      <>
        <h1>Hello World!</h1>
      <>
    )
  }
}

export default App`

* Add a remote repository for github
Select your repositories
Click New
Create a name and do not select any options. You will be manually creating a main branch
Click Create
copy/paste one line from the `…or create a new repository on the command line` that looks like the following code
$ git remote add origin https://github.com/SunkissedQueen/hello_there.git

* Create a main branch for github remote repository
$ git checkout -b main
$ git add .
$ git commit -m "initial commit"
$ git push origin main
Go to browser and should see main branch name appear at the bottom left corner of text editor
In the github webpage, click the repository name. Page should refresh with initial commit and folders currently on app. The message should appear on everything that changed with that commit.

* Delete a branch after merging (Do not delete main branch)
$ git checkout main
$ git pull origin main
$ git branch -d <branch name>

* Pair programming
$ git status
Ensure you want to save changes. Ensure on proper directory $ pwd
$ git add . 
Saves all changes. If not $ git add <copy/paste file name>
Following steps performed by current driver
$ git commit -m "brief descriptive message of changes"
$ git push origin <branch name>
Following steps performed by new driver
$ git clone <copy/paste repository link>
$ git fetch origin <branch name>
$ git checkout <branch name>
$ git pull origin <branch name>
$ <text editor>

* Sole programming
$ git status
Ensure you want to save changes. Ensure on proper directory $ pwd
$ git add . 
Saves all changes. If not $ git add <copy/paste file name>
Following steps performed by current driver
$ git commit -m "brief descriptive message of changes"
$ git push origin <branch name>
Copy/paste github link
Open pull request/merge branch/delete branch on gitHub
follow steps to delete branch in terminal
Follow steps to create a new branch

* Create a new branch before performing changes to main
$ git checkout main
$ git pull origin main
$ git checkout -b rails-controller

* Rails Controller (to connect to React component), View (asssociated with that route), and Route for landing page (App.js)
$ rails g controller Home
Add a file in app/views/home called `index.html.erb`
Add the following code to this file so component can be rendered in browser `<%= react_component 'App' %>`
Inform rails app to serve React App.js to be the landing page go to `config/routes.rb`. Add the following code `root 'home#index'`. This route can be seen on by running in the terminal $ rails routes --expanded
Stop the server and start it again to see changes on browser
Ctrl + C in the terminal
Refresh browser. Should see "Hello World"



* Troubleshooting Tips
Stop the server and start it again.
Did all the setup commands run properly? The commands can be rerun if something isn't working.
Seeing a blank page? Look for errors in the terminal or inspect your page.
Errors? Always look at the first error in the list.
