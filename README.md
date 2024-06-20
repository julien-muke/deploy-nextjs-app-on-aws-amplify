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

Step 3. Set up AWS Amplify & Deploy the Next.js 14 app

Step 4. Set up a custom domain in AWS Route 53

Step 5. Configure the custom domain in AWS Amplify


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

## ➡️ Step 3 - Set up AWS Amplify & Deploy the Next.js 14 app

In this step, you connect your Next.js application in a Git repository to Amplify Hosting.

To connect an app in a Git repository:

1. Open the ![Amplify console](https://console.aws.amazon.com/amplify/)
2. Choose Create new app at the top of the page.

![Screenshot 2024-06-19 at 12 34 32](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/30ed747b-5fdb-4622-b5e1-10212bbadbb2)


3. On the Start building with Amplify page, choose your Git repository provider, then choose Next

![Screenshot 2024-06-19 at 12 35 48](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/6995955e-4c5e-4f05-8248-739f5aafea30)

4. If this is the first time connecting a GitHub repository, A new page opens in your browser on GitHub.com, requesting permission to authorize AWS Amplify in your GitHub account. 

5. Next, you must install the Amplify GitHub App in your GitHub account. A page opens on Github.com requesting permission to install and authorize AWS Amplify in your GitHub account.

6. Select the GitHub account where you want to install the Amplify GitHub App.

7. To limit the installation to the specific repositories that you select, choose Only select repositories. Make sure to include the repo for the app that you are migrating in the repos that you select.

8. Choose Install & Authorize.

9. You are redirected to the Add repository branch page for your app in the Amplify console.

10. In the Recently updated repositories list, select the name of the repository to connect, in my case `julien-muke/julienmuke.cloud`.

11. In the Branch list, select the name of the repository branch to connect `main`

12. Choose Next.

![Screenshot 2024-06-19 at 12 54 48](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/76ab9821-3cd5-4044-bdd6-dd2b21f3d954)

13. On the Review page, choose Save and deploy.

As you can see below our Nextjs App has been deployed successfully to AWS Amplify.

14. Choose Visit deployed URL

![Screenshot 2024-06-19 at 13 00 55](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/93bbf786-cf86-4b88-ad1f-9b62c020fd00)


## ➡️ Step 4 - Set up a custom domain in AWS Route 53

To add a custom domain managed by Route 53:

1. In your Amplify Console, choose your app that you want to connect to a custom domain in my case `julienmuke.cloud`
2. In the navigation pane, under Overview > Hosting > Custom domains

![Screenshot 2024-06-19 at 13 10 19](https://github.com/julien-muke/deploy-nextjs-app-on-aws-amplify/assets/110755734/33416e0a-2fc6-459f-a77f-50a251da16ae)


3. Use your own custom domain with free HTTPS to provide a secure, friendly URL for your app. Register your domain on ![Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/domain-register.html) for a one-click setup, or connect any domain registered on a 3rd party provider.

NOTE: As a 3rd party provider, i have purchased my domain on ![Hostinger](https://www.hostinger.com/) named `julienmuke.cloud` 


4. Amplify can create a hosted zone in Amazon Route 53 for you. This will ensure better integration with the Amplify Console. It will also confirm your ownership of this domain and allow faster deployment.

For that, i'm going to choose `Create hosted zone on Route 53`

5. Choose Configure domain.

