# ![aws](https://github.com/julien-muke/Search-Engine-Website-using-AWS/assets/110755734/01cd6124-8014-4baa-a5fe-bd227844d263)     Deploy Nextjs App to AWS with Amplify Hosting.


## <a name="introduction">🤖 Introduction</a>

In this demo, i'm going to show you how i deployed my portfolio website to AWS with Amplify and set up a custom domain in AWS Route 53.

## <a name="design">📐 Project Architecture</a>

![Nextjs-9](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/ff268da1-4ef4-40b8-9bec-cee842426f82)


## 📝 Prerequisites

Before you begin this tutorial, complete the following prerequisites.

* **Sign up for an AWS account:**

You need to ![create an AWS account](https://portal.aws.amazon.com/billing/signup#/start/email) by following the online instructions. Signing up enables you to access Amplify and other AWS services that you can use with your application.

* **Create an application:**

Create a basic Next.js application to use for this tutorial, using the ![create-next-app](https://nextjs.org/docs/app/api-reference/create-next-app) instructions in the Next.js documentation.

* **Create a Git repository:**

Amplify supports ![GitHub](https://github.com/signup), Bitbucket, GitLab, and AWS CodeCommit. Push your `create-next-app` application to your Git repository.


## <a name="steps">☑️ Steps</a>

The procedure for deploying this architecture on AWS consists of the following steps:

Step 1. Create and configure a Next.js 14 app

Step 2. Push your Next.js 14 app to GitHub

Step 3. Set up AWS Amplify

Step 4. Deploy the Next.js 14 app

Step 5. Set up a custom domain in AWS Route 53

Step 6. Configure the custom domain in AWS Amplify


## ➡️ Step 1 - Create and configure a Next.js 14 app

To create a new Next.js application, Run this command:

```bash
npx create-next-app@latest YOUR-PROJECT-NAME
```

Once you created the application, navigate to the project directory and open your project with a code editor (VS code). You can create more files within your application.

For me, i've built my portfolio website with Next.js for handling the user interface, Three.js for rendering 3D elements, Framer motion for beautiful animations, and styled with TailwindCSS.

![3D Screen Mockup 03_EDIT_01-JM-min](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/06009c5c-6ea5-4afb-a199-764df861d4fd)

Note: If you want a website example, i have a few React.js apps in my ![GitHub repo](https://github.com/julien-muke) that you can clone into your local machine and use for this AWS demo. Feel free to follow and give it a star ⭐


## ➡️ Step 2 - Push your Next.js 14 app to GitHub

When you're done building your Next.js application, You have to push your code to GitHub.

Create a GitHub repository and push your Next.js app's code to this repository by using the following command:

```bash
git init
git add .
git commit -m "Your commit message"
git branch -M master
git remote add origin <your_repository_url>
git push -u -f origin master
```

## ➡️ Step 3 - Set up AWS Amplify

In this step, you connect your Next.js application in a Git repository to Amplify Hosting.

To connect an app in a Git repository:

1. Open the Amplify console
2. Choose Create new app at the top of the page.
3. On the Start building with Amplify page, choose your Git repository provider, then choose Next.
4. On the Add repository branch page do the following:
* Select the name of the repository to connect.
* Select the name of the repository branch to connect.
* Choose Next.





