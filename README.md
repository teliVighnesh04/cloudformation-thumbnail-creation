
# Thumbnail-Creation-Template

An AWS CloudFormation template for seamless thumbnail generation: This template deploys two S3 buckets - *eg., 'master' and 'resized-master.*' When users upload images to the 'master' bucket, an automatic Lambda function is triggered through S3 event notifications. This function generates thumbnails of the images and stores them in the 'resized-master' bucket. To enhance cleanup, a custom Lambda function is implemented. When attempting to delete the CloudFormation stack, it triggers another Lambda function that empties both buckets, ensuring the successful deletion of the stack and associated resources.


## Prerequisites
Create an S3 bucket and upload **'lambda_function.zip'** to it. 
```
This zip file contains the code and dependencies required for the thumbnail creation Lambda function.
```
