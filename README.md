Project Description
After you hosted the website on s3 ,your CTO discovered the deploying the static website directly from s3 was not scalable. So you were asked to show the website content using cloudfront in order to fulfill this contract before routing it via the domain.
Step one

Go to Route53 and create a hosted zone

Create a record under the hosted zone
![1](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/bc22563a-c2d0-40c1-95db-c3003a1c993c)
![2](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/2899ce75-af7a-4709-a529-b96524d0a60e)
![3](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/adea615f-0110-4522-8fa4-b042a03185e9)
Step two

Go AWS certicate manager and request a certificate for the domain, make sure validation method is DNS

Waiting period for certicate to be validate is between 8-48 hours

Create Records in Route53 when done
![1](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/fb725b61-18ca-451a-bcdd-d2d332b0a07c)
![2](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/c50d5f22-99f9-4902-8479-3f1173e30b89)
![3](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/6da23353-53aa-45dd-9032-5a9fd76487d5)
![4](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/71a09bfe-539b-49a4-861b-0a3df4ff9f48)
Step Three

Now we need to go into CloudFront Console to set up cloud front and create a distribution

Make sure to choose Origin access control settings

choose viewer protocol settings (Redirect HTTP TO HTTPS)

Attach the csutom certificate we have created earlier under Custom SSl cert

also making sure origin acces contol points to he s3 bucket from the first part of the project
![1](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/cfab9809-9ac9-4ae3-b049-f7af3878c8f0)
![2](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/1c3c1f27-f856-4047-8ddf-81a9b30d59a9)
![3](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/abf6c900-deaa-4a96-9321-b043989aa8c4)
![4](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/73913d5f-3158-42fa-9e39-e50177df601b)
When we done creating and saving the Cludfront distribution

we make sur to confirm disable public access to the S3 bucket

checking our distrubution should be up and running now
![5](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/2e8e060d-1db2-4088-bf7c-6df6120e7870)
![6](https://github.com/lexbytez/-Hosting-Static-Website-Using-S3-And-Cloudfront./assets/128375535/a018cf92-db05-4f9e-b9be-0e6c9c806bab)


