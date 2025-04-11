# Tinder Like App -- Using GraphDB: neo4j

## Wrap up what I did
- This is a Tinder Like App with user authentication and friendly frontend, and used Neo4J as database to store and manage the user relationships(Like/Dislike).

- Used `npm run dev` to start the server and it run on local port 3000.

### Auth -- Kinde
- I used Kinde to hanlde user authentication, you can choose create one account if you haven't use it before, or just login using email.
![Signin/Login](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Signin%20or%20Login.jpg)

- Both signin and login required authentication code.(Directly send to your signin/login email)
![Auth code](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Signin%3A%20Login-Auth.jpg)

### New user add in
- If new user signin, new user can see all existing users as 'card'.
![New User](https://github.com/Reneechang17/matching-neo4j/blob/main/static/New%20user%20can%20see%20all%20existing%20users.jpg)

- And database will create a new user as well.
![New User-DB](https://github.com/Reneechang17/matching-neo4j/blob/main/static/New%20user%20add%20in-db.jpg)

### Operations and results
- User can choose two operations: 
- 1. left swipe: that means user dislike other user.
![LeftSwipe](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Can%20choose-dislike.jpg)

- 2. right swipe: that means user like other user, and that result 'matched'.
![RightSwipe](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Can%20choose-like.jpg)

- And we can see the relationship update in database.
![Operation res- db](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Prev%20relationship-before%20add%20new%20user.jpg)

### If Matched! (That means A 'LIKE' B && B 'LIKE' A)
- You can see an alert with matched notification!
![Got matched](https://github.com/Reneechang17/matching-neo4j/blob/main/static/Congrats%20on%20matched~.jpg)

- And see your matched card with `/match`.
- For example, MinHsin and Hannah like each other, they got matched.
![See matched1](https://github.com/Reneechang17/matching-neo4j/blob/main/static/When%20two%20matched-1.jpg)
![See matched2](https://github.com/Reneechang17/matching-neo4j/blob/main/static/When%20two%20matched-2.jpg)


- Database will keep record the new users and new relationships...
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
