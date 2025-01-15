# React Router Catch-All Route Issue

This repository demonstrates an uncommon issue with React Router's catch-all route (`*`).  Even when a more specific route *should* match, the catch-all route takes precedence. This can prevent proper handling of 404 errors or other specific route-based logic.

## Problem

The provided `App.js` demonstrates the issue.  No matter what path is entered in the URL, the `NotFound` component always renders.  This occurs because the catch-all route always matches, regardless of whether a more specific route might also apply.

## Solution

The solution addresses this by ensuring that the catch-all route (`*`) is placed correctly, specifically at the very end of the route definitions within the `<Routes>` component.  This ensures other routes have a chance to match before the catch-all takes effect.  See `AppSolution.js` for the corrected implementation.