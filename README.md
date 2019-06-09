# Incremental Game with Backend

In this game, a player performs a simple action by clicking the "slaps" button, which in turn rewards the player with a unit of currency. The player may spend their currency to purchase generators that allow the player to earn currency faster or automatically, without needing to perform the initial action. Also, a player can save his/her progress by logging into the app.

## Runtime dependencies

You will need Java, Node.js, Gradle to run this project (or simply Docker).

## Development

In brief, there are two side of story in this project: **front end development**
and **back end development**.

### File Structure

```
client/                         -> Front end resources
	src/                        -> Source codes
		app.js                  -> JavaScript entry/main file
	test/                       -> Test folder
	.babelrc                    -> JavaScript transpiling configuration (through BabelJS)
	package.json                -> Front end dependencies in npm packages (if any)
	webpack.config              -> Bundler configuration
src/main/
	/java/                  -> Your java classes
		edu/csula/web/HelloServlet.java -> HelloServlet for example
	/webapp/                -> Your front end resources
		js/                 -> JavaScript assets
			app.bundle.js   -> Bundled JavaScript code from `client/src`
build.gradle                    -> necessary gradle definition
build/                          -> built files
	classes                     -> compiled java classes
```

### Running the application

```
gradle appRun
```

And on the front end side of things, you can run the following command under `client` folder after running `npm install`:

```
npm run build
```

> Upon running the `npm run build` command, it will build the bundled JavaScript
> file to `/src/main/webapp`. This means that you don't need to manually copy
> and paste the file to webapp anymore. They are in the right location.

### Tests

To run tests on Java side on root directory of the project:

```
gradle test
```

To run tests on JavaScript side, run the following command in `client` folder:

```
npm test
```

### Demo

https://adityanemade.github.io/Incremental-Game/
