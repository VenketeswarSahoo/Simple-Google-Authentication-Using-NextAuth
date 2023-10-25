# Simple nextauth authentication through Google

## Overview

This repository contains a simple example project that demonstrates how to set up authentication in a Next.js application using [NextAuth.js](https://next-auth.js.org/) and Google OAuth. The instructions below provide step-by-step guidance on how to set up this project.

## Prerequisites

Before you begin, make sure you have the following prerequisites in place:

1. Node.js and npm installed on your system. If not, you can download and install them from [Node.js](https://nodejs.org/).

## Getting Started

Follow the steps below to set up the project:

1. Install NextAuth.js by running the following command:

   ```shell
   npm install next-auth
   ```

2. Create a folder named `auth` inside the `/pages/api` directory. Inside this folder, create a `[...nextauth].js` file. You can refer to the NextAuth documentation for code examples and configuration details.

3. Inside your `/pages/_app.js` file, add code as per the NextAuth documentation to configure authentication in your Next.js app.

4. In your `/pages/index.js` file, add code as per the NextAuth documentation to enable authentication and protect routes as needed.

5. Next, go to the [Google Cloud Console](https://console.cloud.google.com/apis/credentials).

6. Click on "OAuth consent screen" on the left navigation menu, and create a project name. Make sure to add your email address as one of the authorized users.

7. After configuring the consent screen, navigate to the "Credentials" section.

8. Under "OAuth 2.0 Client IDs," click on "Create Credentials" and select "OAuth client ID." Add your project name, set the JavaScript origin path (e.g., `http://localhost:3000`), and add authorized redirect URIs (e.g., `http://localhost:3000/api/auth/callback/google`).

9. Once you've completed the setup and added the necessary credentials, your Google OAuth integration is complete.

## Usage

To run the project locally, use the following commands:

```shell
npm install
npm run dev
```

Your Next.js application with NextAuth.js and Google OAuth should now be accessible at `http://localhost:3000`.
