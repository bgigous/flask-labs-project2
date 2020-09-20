# Blueprints And Application Factory

Samir is realizing that it's not so easy to scale his app up, as he must add view function after view function to the same file. He'd rather update particular components of his app, like post-management, within individual modules that hook together to form the whole app. Hmm, what could he use...

You see, Samir has big dreams for this app. He eventually wants to see it used by CEOs of the world's top companies and wants to go around the world giving talks about how making Byte Blogger changed his life. Even though you think it's more likely to be struck by lightning and *simultaneously* bitten by a shark while at a tiki bar, you decide to help once again.

It turns out you want to practice more with building **blueprints and application factories** in Flask anyway, and you think this is a great opportunity.

___

## Instructions

In this lab, you will create a few blueprints and register them within an application factory.

### Getting Started

To get started with this lab:

- Mac or Linux
  ```bash
  python3 -m venv env
  . env/bin/activate
  pip install -r requirements
  # run the app
  python app.py
  ```

- Windows
  ```powershell
  python3 -m venv env
  env\Scripts\activate.bat
  pip install -r requirements
  # run the app
  python app.py
  ```

### 1. Create The Blueprints

You will separate out the project into three blueprints:

- `blog`: This blueprint will manage posts, which means the functionality that adds, deletes, shows, or modifies a post.
- `auth`: This blueprint will handle anything that logs a user in or out, or registers their account. Note: You don't have to know what the user authentication does in order to complete this lab.
- `main`: All other functionality will go in this blueprint.

### 2. Create The Application Factory

To make the best use of those blueprints, you'll want to register them within an application factory. Create this application factory and initialize your app within it. For this lab, you can pass no arguments to the app factory, and put any configuration within the app factory.
