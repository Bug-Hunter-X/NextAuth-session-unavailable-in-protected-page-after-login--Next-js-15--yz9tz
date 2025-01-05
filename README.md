# NextAuth Session Issue in Next.js 15

This repository demonstrates a problem with NextAuth session access in a protected page within a Next.js 15 application.  After successfully logging in, the protected About page fails to retrieve the session, resulting in an access denied message.

## Problem Description

The `AboutPage` component utilizes `unstable_getServerSession` to verify user authentication.  Despite successful login, the session object remains null, leading to the access denial.

## Steps to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Navigate to the `/about` page.
5. Observe the access denied message despite being logged in.

## Solution

The solution involves ensuring proper configuration of NextAuth and correct usage of `unstable_getServerSession`. See the solution in the `aboutSolution.js` file.