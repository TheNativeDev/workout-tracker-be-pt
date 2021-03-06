[![Maintainability](https://api.codeclimate.com/v1/badges/7081253f23a08f107ff0/maintainability)](https://codeclimate.com/github/Lambda-School-Labs/workout-tracker-be-pt7/maintainability)

[![Test Coverage](https://api.codeclimate.com/v1/badges/7081253f23a08f107ff0/test_coverage)](https://codeclimate.com/github/Lambda-School-Labs/workout-tracker-be-pt7/test_coverage)

# API Documentation

#### Backend delpoyed at [Heroku](https://dashboard.heroku.com/apps/frozen-hamlet-18508/deploy/github) <br>

## Getting started

To get the server running locally:

- Clone this repo
- **npm install** to install all required dependencies
- **npm server** to start the local server
- **npm test** to start server using testing environment

### Knex, Express.js, Node.js

- Knex: A query builder for PostgreSQL, because it is designed to be flexible, portable, and fun to use
- Express.js: Released as free and open-source software under the MIT License. It is designed for building web applications and APIs. It has been called the de facto standard server framework for Node.js
- Node.js: An open-source, cross-platform, JavaScript runtime environment that executes JavaScript code outside of a browser.

## Endpoints

#### User Routes

| Method | Endpoint                | Access Control      | Description                                        |
| ------ | ----------------------- | ------------------- | -------------------------------------------------- |
| GET    | `users/org`             | all users           | Returns info for all users.                        |
| GET    | `/login`                | users               | Logs that user in.                                 |
| GET    | `/users/:userId`        | users               | Returns info for a single user.                    |
| POST   | `/users/register`       | none                | Creates a new user.                                |
| PUT    | `/users/:userId`        | users               | Updates the current user.                          |
| DELETE | `/users/:userId`        | users               | Deletes the current user.                          |

# Data Model

#### USERS

---

```
{
  username: req.body.username,
  email: req.body.email,
  password: hash,
  goal: req.body.goal,
  goal_startdate: req.body.goal_startdate,
  goal_enddate : req.body.goal_enddate
}
```

## Actions

`getUsers()` -> Returns all users.

`getUserById(userId)` -> Returns a single user by user ID.

`returning(['id', 'email', 'username'])` --> Creates a new user and returns that user.

`findBy(req.params.id, updatedUser)` -> Updates a single user by ID.

`deleteUser(userId)` -> Deletes everything dependent on the user.

## Environment Variables

In order for the app to function correctly, the user must set up their own environment variables.

create a .env file that includes the following:
    
    *  DEV_DB_USER
    *  DEV_DB_PASSWORD
    *  DEV_DB_HOST
    *  DEV_DB_DATABASE
    *  DEV_DB_ENV='development'
    *  DEV_DATABASE_URL
    *  DATABASE_URL
    
## Contributing

When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change.

Please note we have a [code of conduct](./code_of_conduct.md). Please follow it in all your interactions with the project.

### Issue/Bug Request

 **If you are having an issue with the existing project code, please submit a bug report under the following guidelines:**
 - Check first to see if your issue has already been reported.
 - Check to see if the issue has recently been fixed by attempting to reproduce the issue using the latest master branch in the repository.
 - Create a live example of the problem.
 - Submit a detailed bug report including your environment & browser, steps to reproduce the issue, actual and expected outcomes,  where you believe the issue is originating from, and any potential solutions you have considered.

### Feature Requests

We would love to hear from you about new features which would improve this app and further the aims of our project. Please provide as much detail and information as possible to show us why you think your new feature should be implemented.

### Pull Requests

If you have developed a patch, bug fix, or new feature that would improve this app, please submit a pull request. It is best to communicate your ideas with the developers first before investing a great deal of time into a pull request to ensure that it will mesh smoothly with the project.

Remember that this project is licensed under the MIT license, and by submitting a pull request, you agree that your work will be, too.

#### Pull Request Guidelines

- Ensure any install or build dependencies are removed before the end of the layer when doing a build.
- Update the README.md with details of changes to the interface, including new plist variables, exposed ports, useful file locations and container parameters.
- Ensure that your code conforms to our existing code conventions and test coverage.
- Include the relevant issue number, if applicable.
- You may merge the Pull Request in once you have the sign-off of two other developers, or if you do not have permission to do that, you may request the second reviewer to merge it for you.

### Attribution

These contribution guidelines have been adapted from [this good-Contributing.md-template](https://gist.github.com/PurpleBooth/b24679402957c63ec426).

## Documentation

- See [Web Frontend Documentation](https://github.com/Lambda-School-Labs/workout-tracker-fe-pt7) for details on the fronend of our project.
- See [iOS App Documentation](https://github.com/Lambda-School-Labs/workout-tracker-ios-pt7) for details on the iOS portion of our project.
- See [UX Documentation](https://www.figma.com/file/kEKgIN0bWriJGpIZ9hmGI2/Workout-Tracker%2C-Mahiya-%26-Adeolu?node-id=313%3A6) for details on the UX design of our project.
