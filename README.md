# Venue Explorer - A10

## Live Demo

Deployed on Vercel: [https://swd2-hw10.vercel.app/](https://swd2-hw10.vercel.app/)

Continues A09 with NextAuth sign-in against the assignment backend.

- The Sign-In link on the left of the top menu opens the NextAuth sign-in page
  (email and password) and becomes Sign-Out after logging in.
- Sign-in posts the credentials to the backend login API and keeps the returned
  token in the session.
- `/booking` shows the signed-in user's name, email, telephone, and member since
  date, fetched from the profile API with the Bearer token.
- The home banner shows "Welcome" and the user's name at the top right.
- The A09 venue pages are retained.

## Run locally

Put the provided `.env.local` (`NEXTAUTH_URL`, `NEXTAUTH_SECRET`) in the project root.

```bash
npm ci
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) and sign in with the test account.

## Verify

```bash
npm run test -- case1.test.tsx
npm run test -- case2.test.tsx
npm run test -- case3.test.tsx
npm run lint
npm run build
npm run start
```

Test case 1 calls the real assignment API, so an internet connection is required.
