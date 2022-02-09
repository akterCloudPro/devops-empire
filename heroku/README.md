# Heroku
Heroku is a cloud platform as a service supporting several programming languages.

#### Causes of Heroku H10-App Crashed Error And How To Solve Them
*Reference article link: https://dev.to/lawrence_eagles/causes-of-heroku-h10-app-crashed-error-and-how-to-solve-them-3jnl

### Bug in Procfile
A very interesting discovery for me. A bug in your Procfile can crash your app. If your Procfile is pointing to the wrong server file. e.g If your server is in server.js and your Procfile points to app.js this would definitely crash your app and Heroku would greet you with the H10-App crashed error code message.
Secondly, a buggy Procfile can also come in the form of wrong spacing.
- Wrong: web : node index.js
- Correct web: node index.js



