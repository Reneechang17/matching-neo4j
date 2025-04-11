# Tinder-Like App Using Neo4j Graph Database

## Overview
- This is a Tinder-like application featuring user authentication and a user-friendly interface. The app uses Neo4j as the database to store and manage user relationships (Likes/Dislikes).

### Get Started
- Run the application locally using:  `npm run dev`
- The application will be available at `http://localhost:3000`.

## Why Neo4j
- Its graph structure is ideal for modeling and querying relationships between users.
- It efficiently handles complex relationship queries (like finding mutual likes).
- It scales well for social network-type applications where **relationships** are the primary focus.

## Features and Functionality

### User Authentication with Kinde
- The application uses Kinde for user authentication:
- New users can create an account or returning users can log in using email.
![Signin/Login](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Signin%20or%20Login.jpg)

- Both signup and login require an authentication code sent directly to the user's email.
![Auth code](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Signin%3A%20Login-Auth.jpg)

### New User Onboarding
- When a new user signs up, they can view all existing users as swipeable cards.
- Implemented by `react-tinder-card`.
![New User](https://github.com/Reneechang17/matching-neo4j/blob/main/static/New%20user%20can%20see%20all%20existing%20users.jpg)

- And automatically creates a new user node in the Neo4j database.
![New User-DB](https://github.com/Reneechang17/matching-neo4j/blob/main/static/New%20user%20add%20in-db.jpg)

### User Interactions
- Users have two primary actions available:
- 1. Left Swipe (Dislike): Indicates the user is not interested.
- => A --Dislike--> B
![LeftSwipe](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Can%20choose-dislike.jpg)

- 2. Right Swipe (Like): Indicates interest in matching with another user
- => A --Like--> B
![RightSwipe](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Can%20choose-like.jpg)

- All user interactions are recorded as relationships in the Neo4j database.
![Operation res- db](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Prev%20relationship-before%20add%20new%20user.jpg)

### Match Functionality
- When two users mutually like each other (User A likes User B **AND** User B likes User A):
- A match notification appears as an alert:
![Got matched](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Congrats%20on%20matched~.jpg)

- Users can view their matches at the `/match` endpoint
- Example: MinHsin and Hannah liked each other and created a match
![See matched1](https://github.com/Reneechang17/matching-neo4j/blob/main/static/When%20two%20matched-1.jpg)
![See matched2](https://github.com/Reneechang17/matching-neo4j/blob/main/static/When%20two%20matched-2.jpg)

### Database Architecture
- Neo4j Database will keep record the new users and new relationships...
- This graph structure makes it easy to query for matches and potential recommendations features.
![Result Page-db](https://github.com/Reneechang17/matching-neo4j/blob/main/static/final%20relationship-tinder.jpg)

----------

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
