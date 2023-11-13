## Deployment
## Server
- This web app runs on a a Vite server.
- The URL is provided for this when running the front end, after npm installing.
  ![Console output](./images/console-output.png)
## Where to put files/folders
- When you clone the repository (from: https://bitbucket.org/accutechcapstone/bsu.subscriptionmanager/src/master/) all files should be in place. Just clone to wherever you want to.
## How to start stop the system
- Currently the system can only be run locally. Navigate into the frontend directory of the project. Run 'npm run dev'
- The backend is run similarily. Navigate to the api directory of the project. Run 'dotnet run'
- Navigate to the link outputted by the frontend, and when both the frontend and backend are running, form submissions are allowed and will create subscriptions in Maxio.
## Troubleshooting
- The best way to troubleshoot would be utilizing the consoles
- Use the stack trace to find the source of issues, if it is code related
- This would usually be the reason for errors currently, as we are only running locally.
## Where to find errors
- Errors can be thrown in a couple of places in this system.
- Errors for the front end and our bulk signup endpoint are liekly to be logged in the developer console, in the browser (i.e. DevTools in Chrome).
- Errors are also logged from Maxio's api response in the terminal where .Net was run, displaying if something went wrong on subscription creation.
## Vulnerable pieces
- Currently the most vulnerable piece of the system is our api endpoint and call to Maxio.
- Our data object in the backend that takes form info is setup pretty specfically right now, so if changes were made to what is passed in, lots would break.
- We do not currently have any validation on the backend to ensure the information passed to Maxio is exactly how Maxio wants it, so this could potentially cause issues.
- Our front end has lots of validation, so there is not much that could cause the system to fail currently.
