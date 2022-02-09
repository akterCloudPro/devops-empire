# Heroku
Heroku is a cloud platform as a service supporting several programming languages.

#### Causes of Heroku H10-App Crashed Error And How To Solve Them
*Reference article link: https://dev.to/lawrence_eagles/causes-of-heroku-h10-app-crashed-error-and-how-to-solve-them-3jnl

### Bug in Procfile
A very interesting discovery for me. A bug in your Procfile can crash your app. If your Procfile is pointing to the wrong server file. e.g If your server is in server.js and your Procfile points to app.js this would definitely crash your app and Heroku would greet you with the H10-App crashed error code message.
Secondly, a buggy Procfile can also come in the form of wrong spacing.
- Wrong: web : node index.js
- Correct web: node index.js

### Setting a PORT as a Heroku environment variable
This would surely crash your app. Heroku automatically sets a Port that can be accessed via process.env.PORT. Setting a port yourself would crash your app. Surprisingly, the command `heroku config` does not display the preset Heroku port so one might be tempted to set another port as an environment variable.
To see all the preset Heroku environment variables, use the command heroku run printenv.



