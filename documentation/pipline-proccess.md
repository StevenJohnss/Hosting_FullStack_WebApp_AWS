


* Orbs: 
```
  node: circleci/node@5.0.2
  eb: circleci/aws-elastic-beanstalk@2.0.1
  aws-cli: circleci/aws-cli@3.1.1
```

* Jobs(two main jobs) :
    * Build 
    * Deploy

* Build steps:
    1. Spin Up Environment: install node js and its packages
    2. Preparing Environment Variables:  exports all environment variables from CircleCI configuration to a .env file
    3. Checkout: go to the root directory
    4. Install api dependencies: install packages in package.json
    6. Install frontend dependencies: install packages in package.json
    7. Building frontend: execute building commands in package.json scripts 
    8. Building api: execute building commands in package.json scripts 

* Deploy steps:
    1. Spin Up Environment:install node js and its packages
    2. Preparing Environment Variables: exports all environment variables from CircleCI configuration to a .env file
    3. Checkout: go to the root directory
    4. Install aws cli: to implement aws cli commands used in deployment
    5. Setting up Elastic Beanstalk cli: to implement eb cli commands used in deployment
    6. Deploying: execute deploying commands in package.json scripts  


* Workflow: 
    1. Build job
    2. Deploy job
