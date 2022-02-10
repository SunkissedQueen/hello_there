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
$ git checkout -b main
$ git add .
$ git commit -m "initial commit"
$ git push origin <branch name>

* Rails Controller and View

* Deployment instructions

* Troubleshooting Tips
Stop the server and start it again.
Did all the setup commands run properly? The commands can be rerun if something isn't working.
Seeing a blank page? Look for errors in the terminal or inspect your page.
Errors? Always look at the first error in the list.
