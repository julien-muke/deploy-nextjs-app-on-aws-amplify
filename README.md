# ![aws](https://github.com/julien-muke/Search-Engine-Website-using-AWS/assets/110755734/01cd6124-8014-4baa-a5fe-bd227844d263)     Deploy Nextjs App to AWS with Amplify Hosting.


## <a name="introduction">🤖 Introduction</a>

In this demo, i'm going to show you how i deployed my portfolio website to AWS with Amplify and set up a custom domain in AWS Route 53.

## <a name="design">📐 Project Architecture</a>

![Nextjs-5](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/5d3b4cac-4e68-4f42-a2c3-919f4cfb9988)

**Prerequisites**

Before you begin this tutorial, complete the following prerequisites.

**Sign up for an AWS account:**

If you are not already an AWS customer, you need to ![create an AWS account](https://portal.aws.amazon.com/billing/signup#/start/email) by following the online instructions. Signing up enables you to access Amplify and other AWS services that you can use with your application.

**Create an application:**

Create a basic Next.js application to use for this tutorial, using the ![create-next-app](https://nextjs.org/docs/app/api-reference/create-next-app) instructions in the Next.js documentation.

**Create a Git repository:**

Amplify supports GitHub, Bitbucket, GitLab, and AWS CodeCommit. Push your `create-next-app` application to your Git repository.


## <a name="steps">☑️ Steps</a>

The procedure for deploying this architecture on AWS consists of the following steps:

Step 1. Launch the instance scheduler stack

Step 2. Configure periods and schedules

Step 3. Creating an EC2 instance and Tag your instances

Step 4. Test Instance Scheduler


## ➡️ Step 1 - Create CloudFormation