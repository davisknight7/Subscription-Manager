# Development
## Tech Aspects
- Frontend: Vue 3 with TypeScript
- Backend: .NET 7.0 with C#
- Bitbucket for version control

## Vue Folder Structure
- src has the main code
- src/views contains the pages for the site, including the typescript, scss, and html in each .vue file.
- src/components ontains vue code for individual components for the pages, such as the InputGroup, AdvisorsSection, ect.
- src/assets contains images and other assets for the site.
- src/services contains the code for the api calls to the backend.
- src/types contains the typescript types.
- src/stores contains the pinia stores.
- src/validators contains the zod schema validators.
- package.json contains the dependencies for the project and scripts that can be run for the project.
## FRONTEND

### Installing Pre-requisites
- Install NodeJS (v20.9.0 recommended)
    - [Node Download](https://nodejs.org/en)

### Installing Dependencies
- Run `npm install` in the frontend directory

### Reccomended IDE Setup
#### Plugins
- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).


### Running the Frontend Locally
- Clone the code from: https://bitbucket.org/accutechcapstone/bsu.subscriptionmanager/src/master/
- master has the latest release code, dev has the latest development code. You probably will want to check out dev.
- In a terminal, navigate to the project directory. At the top level, run 'cd frontend'
- Run `npm run dev` in the frontend directory
  ![Console output](./images/console-output.png)
- Navigate to the outputted URL in your browser
- You should see the following page
  ![Site screenshot](./images/default-bulk-signup-frontend.png)

### Linting and Formatting
- Linting and Formatting is done with ESLint and Prettier using the Accutech specific configuration
- Run `npm run lint` in the frontend directory to lint the code
- Run `npm run lint:fix` in the frontend directory to fix linting errors
- Run `npm run format` in the frontend directory to format the code
- Linting guidelines can be found in the `.eslintrc` file in the frontend directory
- Formatting guidelines can be found in the `.prettierrc.json` file in the frontend directory

## BACKEND

### Installing Pre-requisites
- Install .NET 7.0
    - [Download .NET](https://dotnet.microsoft.com/en-us/download)

### Reccommended IDE Setup
- [Visual Studio Code](https://code.visualstudio.com/)
#### Plugins
- [C# Dev Kit](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csdevkit)
### Running the Backend Locally
- In a terminal, navigate to the top level of the project directory. Once there, run 'cd api'
- Run `dotnet run` in the api directory
- The output should look something like this:
  ![Console output](./images/run-backend-successfully-output.png)

- Once the backend is running, you will be able to submit a bulk signup subscription request to Maxio
- A successfull susbcription creation will look something like this in the terminal:
  ![Subscription Creation Console Output](./images/subscription-creation-output.png)
- This alert will also display on the front end:
- ![Subscription Creation Alert](./images/advisors-added-alert.png)

## Replicating via Docker
- Run `docker compose up` in the root level of the project directory
- If this is the first time running the project, it will take a while to download the images and build the containers
- If you have built the containers before and have new npm packages run `docker compose up --build` to rebuild the containers
- You should see the following output in the terminal:
  ![Docker Output](./images/docker-output.png)
- The api will be running on port `5002`
- The bulk sign up frontend will be running on port `5173`
- The subscription manager frontend will be running on port `5174`