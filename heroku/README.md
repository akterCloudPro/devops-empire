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
This would surely crash your app. Heroku automatically sets a Port that can be accessed via `process.env.PORT`. Setting a port yourself would crash your app. Surprisingly, the command `heroku config` does not display the preset Heroku port so one might be tempted to set another port as an environment variable.
To see all the preset Heroku environment variables, use the command `heroku run printenv`

### Missing Required Environment Variable 
while setting a port would cause this error because Heroku already sets a port internally, failing to set any required environment variable (e.g your database), would prompt Heroku to greet you with this error.

### Missing Required Scripts
This error is thrown in a Node.js environment if you forget to set a `start script`. Heroku uses this script to start your app so if it is missing, it would throw an H10-App crashed error code message.
This can be solved by setting a start script in the `package.json`. e.g
![scr-01](https://user-images.githubusercontent.com/73134659/153249123-97afbb89-31d9-4f3b-aead-a8f6aeefb5f0.JPG)

### Final Thoughts
If none of the above solved your problem, you can make a last-ditch attempt by updating all your packages. If this doesn't help and you are in a `Node.js` environment, your last resort would be setting a `node version` in the engine section of your `package.json` file.
![scr-01](https://user-images.githubusercontent.com/73134659/153249427-8ee1964f-4f46-4264-8027-cd2d956af8cf.JPG)

### The Unthinkable
Lastly, if your bug defiles all solution, and by this time you are grasping at straws; I leave you in the able hands of `heroku restart`.




