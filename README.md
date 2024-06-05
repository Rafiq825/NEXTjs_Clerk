# Next.js Clerk Integration

## Table of Contents

- [Next.js Clerk Integration](#nextjs-clerk-integration)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Features](#features)
  - [Installation](#installation)
  - [Configuration](#configuration)

## Introduction

This project is a [Next.js](https://nextjs.org/) application integrated with [Clerk](https://clerk.dev/) for user authentication and management. Clerk provides a seamless authentication experience, making it easy to add user sign-up, sign-in, and profile management to your Next.js application.

## Features

- User Authentication (Sign-up, Sign-in)
- User Profile Management
- Session Management
- Pre-built UI components
- Easy integration with Next.js


## Installation

To get started with this project, follow these steps:

1. **Clone the repository:**

    ```sh
    git clone https://github.com/Rafiq825/NEXTjs_Clerk.git
    ```

2. **Install dependencies:**

    ```sh
    npm install
    # or
    yarn install
    ```

3. **Set up Clerk:**

    Create an account on [Clerk](https://clerk.dev/) and obtain your Clerk Frontend API key.

4. **Environment Variables:**

    Create a `.env.local` file in the root of your project and add the following:

    ```env
    NEXT_PUBLIC_CLERK_FRONTEND_API=<your-clerk-frontend-api-key>
    ```

## Configuration

Configure Clerk in your Next.js application by updating the `_app.js` or `_app.tsx` file:

```jsx
// pages/_app.js
import { ClerkProvider } from '@clerk/nextjs';

function MyApp({ Component, pageProps }) {
  return (
    <ClerkProvider>
      <Component {...pageProps} />
    </ClerkProvider>
  );
}

export default MyApp;
