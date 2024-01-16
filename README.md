# serverless-architecture-patterns-dynamoDB
If you are dealing with multiple Microservices in your product, with each service owned by a different team, how do you deploy these services is a very important question that needs to be addressed?

Each Team manages and owns end to end service deployment — API Gateway, Lambda functions and DynamoDB.

Each service gets deployed in a different AWS account (managed by the service team). It inherently increases the TPS of the overall product because API Gateway and Lambda functions concurrency limit are at the Account level. These limits are off-course soft limits and can be increased by raising a case via AWS Console, if you plan to host the services in the same AWS account

Each service can have a custom domain attached to it. Something like — catalog.example.com OR order.example.com.
