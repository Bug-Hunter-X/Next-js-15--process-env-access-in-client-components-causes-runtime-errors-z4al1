# Next.js 15 Client-Side process.env Access Error

This repository demonstrates a common error encountered when using environment variables in Next.js 15 client-side components.  Accessing `process.env` directly within a client component results in a runtime error because environment variables are not available in the browser context.

**Problem:** The `about.js` file attempts to access the `process.env.MY_VARIABLE` environment variable. This works correctly on the server-side, but fails on the client-side.

**Solution:**  Environment variables should be handled via the `getStaticProps` or `getServerSideProps` functions for data fetching and passed as props to the client-side component.