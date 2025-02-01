# React Router Dom v6 Catch-all Route bug
This repository demonstrates a bug in React Router Dom v6 where a catch-all route (`/*`) incorrectly matches all routes, even those defined above it.  This leads to unexpected behavior where the catch-all route always renders, regardless of the actual URL.

The solution involves using a more precise wildcard matching strategy.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/` or `/about`.
5. Observe that the NotFound component renders in all cases, even though these routes are explicitly defined.

## Solution

The solution involves moving the catch-all route to the end of the `Routes` component. This ensures that specific routes are matched before the catch-all route is considered.