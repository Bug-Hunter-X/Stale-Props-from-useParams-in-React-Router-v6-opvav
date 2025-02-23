# Stale useParams Data in React Router v6

This repository demonstrates a common issue in React Router v6: stale data returned by the `useParams` hook when used outside the direct children of a route component.  The problem arises when the parent component re-renders without a URL change, resulting in the `useParams` hook returning old data.

The `staleParamsBug.js` file shows the problem. The solution, provided in `staleParamsSolution.js`, addresses this by ensuring that the component using `useParams` is always a direct child of the route or by using a data fetching mechanism triggered by URL changes.