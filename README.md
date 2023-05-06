
### Running the project

1. Clone the repository to your local machine. 

<br>




1. Open a terminal and run the following commands to start the server
    - `cd server`
    - `npm install`
    - `npm run dev`

2. Open a terminal and run the following commands to start the client
    - `cd react-client`
    - `npm install` 
    - `npm start`

3. Register for an account! 
- You can create your own account
- Alternatively you can use login credentials in the next step 

1. Login 
- Login with the credentials you used in the previous step or use:

Note 
    - `npm install` installs the node modules and only needs to be ran once in each folder
    - `CTRL+C` can be pressed at anytime to close the server, client or tests.  

<br><br >

### Architecture Overview

#### server
- **config**: Contains configuration files for the application, including settings for the server, database. Also contains some validation of fields.
- **controllers**: Includes functions that handle HTTP requests from the client and send responses back. These functions may also interact with the model module to retrieve or manipulate data. Handles login, registration and database queries.
- **data**: A json copy of the recipes. Used initially to create the database.
- **logs**: Contains log files for the application, which can be used for debugging or monitoring purposes.
- **middleware**: Includes functions that can be used to modify incoming HTTP requests or outgoing responses. Includes authentication and logging functionality.
- **model**: Includes functions that interact with the data module to retrieve or manipulate data. Used by the controller module. It includes a User and Recipe model. 
- **node_modules**: Contains third-party dependencies that the application uses.
- **public**: Contains static files that the application serves to client only contain a single css file.
- **routes**: Contains files that define the routes for the application. Each route maps an HTTP request method and URL path to a controller function.
- **test**: Mocha test for the 6 server-side features.
- **views**: Contains files that define the templates for rendering HTML pages to clients. We have a custom 404 page here.
- **.env**: A file containing environment variables that are used by the application.
- **package-lock.json**: A file used by NPM to ensure that the application's dependencies are installed consistently across different machines.
- **package.json**: Contains metadata about the application, including its name, version, and dependencies.
- **gitignore**: A file specifying files or directories that should not be tracked by version control. 

#### react-client
- **node_modules**: Contains third-party dependencies that the application uses.
- **public**: Contains static files that the application serves to client, contains index.html and a logo
- **src**
    - **api**: Use to create axios instances. 
    - **components**: Contains reusable components used by the application. Such as headers, footers, the homepage layout etc.
    - **context**: This provider component makes the auth state and setAuth function available to its children via the AuthContext.
    - **features**: Contains all the react client-side features implemented for part 3. 
    - **hooks**: Contains custom React hooks used by the application.
    - **App.mjs**:The main React component that renders the application.
    - **index.css**: CSS styling for the application.
    - **index.mjs**: The entry point for the application, which renders the App component.
<br><br>
- **gitignore**: A file specifying files or directories that should not be tracked by version control.
- **package-lock.json**: A file used by NPM to ensure that the application's dependencies are installed consistently across different machines.
- **package.json**: Contains metadata about the application, including its name, version, and dependencies.
- **README**: Common commands to use with the application.
