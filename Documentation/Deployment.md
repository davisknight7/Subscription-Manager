## Deployment
## Server
- This web app runs on a a Vite server
- An AWS server is probably the best option for deploying this project to an actual server
## Where to put files/folders
- The BitBucket repository (https://bitbucket.org/accutechcapstone/bsu.subscriptionmanager/src/master/) can be connected to AWS in order to deploy the source code onto the server. Once the repo is connected, choose a branch to build and deploy
- You will need to confirm frontend and backend settings, add environment variables, and finally save and deploy
## How to start stop the system
- This can be done manually or automatically
- Sign into the AWS console and open EC2 console
- Choose instances in the navigation pane, and select your isntance
- To start, just choose the instance and choose instance state, start instance
- To stop an isntance, choose instance, stop instance. You will need to confirm the stop, which could take a few minutes
## Troubleshooting
- The best way to troubleshoot would be utilizing AWS docs on troubleshooting instances:
  https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-troubleshoot.html
- Console could also be used
## Where to find errors
- Errors can be thrown in a couple of places in this system
- Errors for the system could be found in the pipeline
- Errors could also be found in logs, here is how to view them:
  https://docs.aws.amazon.com/systems-manager/latest/userguide/fleet-logs.html
## Vulnerable pieces
- AWS servers face vulnerabilities around identity and access management, data encryption, liability, etc. More here:
  https://www.getastra.com/blog/security-audit/aws-cloud-security/
- Currently the most vulnerable piece of the system is our api endpoint and call to Maxio
- Our data object in the backend that takes form info is setup pretty specfically right now, so if changes were made to what is passed in, lots would break
- We do not currently have any validation on the backend to ensure the information passed to Maxio is exactly how Maxio wants it, so this could potentially cause issues
