# pipeline process

- The steps in the pipeline:
  1. Install node, AWS CLI, and EB CLI orbs.
  2. Install node
  3. Setup AWS CLI and EB CLI with the IAM credentials provided in the environment variables.
  4. Install the frontend dependencies.
  5. Install the backend dependencies.
  6. Build the frontend application.
  7. Build the backend application.
  8. Deploy the frontend application to the designated S3 bucket.
  9. Deploy the backend application to EB and set the environment variables using the ones provided in CircleCI.
