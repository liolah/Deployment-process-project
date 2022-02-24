## Infrastructure description and pipeline process

### Infrastructure description

- To deploy the app you have to provide these resources in order. Later deployment steps require endpoints that will be acquired after the provision of previous services.

The resources required by the app:

1. AWS RDS hosting postgres database:
   i. Size: db.t3.micro
   ii. publicly accessible.
   iii. Edit the VPC security group rules to make it accessible. Modify the default inbound rule by changing the source address to 0.0.0.0/0 in order to allow access from any source.(It didn't work for me without this step)  
   <br>
2. AWS EB hosting the udagram-api:
   i. Deploy the udagram-api on a new environment hosting nodejs.
   ii. Configure the environment variables using the database credentials obtained after the provision of the database.
   <br>
3. AWS S3 bucket to host the frontend:
   i. Replace the url to the API endpoint in the frontend environment configuration files with the endpoint obtained after the deployment of the udagram-api on EB.
   ii. Create a new bucket and upload the contents of the build folder. Make sure to enable public access and ACLs.
   iii. Enable static web hosting.
   iv. Modify the bucket policy to enable public read.

### pipeline process

- The steps in the pipeline:
  1. Install node, AWS CLI, and EB CLI orbs.
  2. Install node
  3. Setup AWS CLI and EB CLI with the IAM credentials provided in the environment variables.
  4. Install the frontend dependencies.
  5. Install the backend dependencies.
  6. Build the frontend application.
  7. Build the backend application.
  8. Deploy the frontend application.
  9. Deploy the backend application.
