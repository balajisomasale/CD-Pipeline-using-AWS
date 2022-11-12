### Create Delivery Pipeline

https://aws.amazon.com/getting-started/hands-on/create-continuous-delivery-pipeline/module-four/

In this module, you will use AWS CodePipeline to set up a continuous delivery pipeline with source, build, and deploy stages.
The pipeline will detect changes in the code stored in your GitHub repository, 
build the source code using AWS CodeBuild, and then deploy your application to AWS Elastic Beanstalk.

- Set up a continuous delivery pipeline on AWS CodePipeline
- Configure a source stage using your GitHub repo
- Configure a build stage using `AWS CodeBuild`
- Configure a deploy stage using your `AWS ElasticBeanstalk application`
- Deploy the application hosted on GitHub to ElasticBeanstalk through a pipeline

#### Create New Pipeline : 

- In a browser window, open the AWS CodePipeline Console.
- Click the orange "Create pipeline" button. A new screen will open up so you can set up the pipeline.
- In the "Pipeline name" field type "Pipeline-DevOpsGettingStarted."
- Visually confirm that "New service role" is selected.
- Click the orange "Next" button.

Just follow the link to check all the steps for Create > Configure > Build > Deploy 

![image](https://user-images.githubusercontent.com/35003840/201485320-033f0b23-edaa-4ca0-ab5d-a1ab9abdf33e.png)

![image](https://user-images.githubusercontent.com/35003840/201485396-2214f918-7260-497d-8a6c-e1345622cfe8.png)

Website can be accessed from AWS Elastic Bean stalk 

We have created a continuous delivery pipeline on AWS CodePipeline with three stages: source, build, and deploy.
The source code from the GitHub repo created in Module 1 is part of the source stage. 
That source code is then built by AWS CodeBuild in the build stage.
Finally, the built code is deployed to the AWS Elastic Beanstalk environment created in Module 3.

completed building CD Pipeline using AWS modules 



