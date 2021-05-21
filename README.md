# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

Steps :

1 - rails new app-name --skip-webpack-install --skip-javascript
2 - mkdir -p app/assets/javascripts
3 - Create app/assets/javascripts/application.js with the following contents (taken from a Rails 5 app) :
//= require rails-ujs
//= require turbolinks
//= require_tree .
4 - open app/assets/config/manifest.js add the following line :
...
//= link_directory ../javascripts .js
5 - open app/views/layouts/application.html.erb and add the following line :
<%= javascript_include_tag 'application', 'data-turbolinks-track': 'reload' %>
6 - remove lines with javascript_pack_tag

Add Frontend Part (Create-react-app) :

1 - npx create-react-app frontend
2 - echo 'PORT=3001' > frontend/.env
3 - cd frontend
4 - npm start