#### Module 3 : Create Build Project Using `AWS Cloud Build`

https://aws.amazon.com/getting-started/hands-on/create-continuous-delivery-pipeline/module-three/

In this module, you will use `AWS CodeBuild` to build the source code previously stored in your GitHub repository. 
AWS CodeBuild is a fully managed continuous integration service that compiles source code, runs tests, and produces software packages that are ready to deploy.

![image](https://user-images.githubusercontent.com/35003840/201484700-69a65d4d-5349-49f6-a651-ae41c6142bb8.png)


- Create a build project with AWS CodeBuild
- Set up GitHub as the source provider for a build project
- Run a build on AWS CodeBuild

##### Configure AWS CodeBuild Project : 

- In a new browser tab open the AWS CodeBuild Console.
- Click the orange "Create project" button.
- In the "Project name" field type "Build-DevOpsGettingStarted."
- Select "GitHub" from the "Source provider" dropdown menu.
- Visually confirm that the "Connect using OAuth" radio button is selected.
- Click the white "Connect to GitHub" button. After clicking this button, a new browser tab will open asking you to give AWS CodeBuild access to your GitHub repo.
- Click the green "Authorize aws-codesuite" button.
- Type in your GitHub password.
- Click the orange "Confirm" button.
- Select "Repository in my GitHub account."
- Type "aws-elastic-beanstalk-express-js-sample" in the search field.
- Click on the repo you forked in Module 1. After clicking your repo, your screen should look like this:
- Visually confirm that "Managed Image" is selected.
- Select "Amazon Linux 2" from the "Operating system" dropdown menu.
- Select "Standard" from the "Runtime(s)" dropdown menu.
- Select "aws/codebuild/amazonlinux2-x86_64-standard:3.0" from the "Image" dropdown menu.
- Visually confirm that "Always use the latest image for this runtime version" is selected for "Image version."
- Visually confirm that "Linux" is selected for "Environment type."
- Visually confirm that "New service role" is selected.

##### Create A BuildSpec file for the project :

`Buildspec`: Collection of build commands and related settings, in YAML format, that CodeBuild uses to run a build.

- Select "Insert build commands." and Click on "Switch to editor."
- Replace the Buildspec in the editor with the code below:
`version: 0.2
phases:
    build:
        commands:
            - npm i --save
artifacts:
    files:
        - '**/*'
`
- Click the orange "Create build project" button. You should now see a dashboard for your project.

##### Test the CodeBuild Project :

- Click the orange "Start build" button. This will load a page to configure the build process.
- Confirm that the loaded page references the correct GitHub repo.
- Click the orange "Start build" button.
- Wait for the build to complete. As you are waiting you should see a green bar at the top of the page with the message "Build started," the progress for your build under 'Build log," and, after a couple minutes,
  a green check mark and a "Succeeded" message confirming the build worked.

