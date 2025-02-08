# React Router Dom Nested Route Conflict with Wildcard Route

This repository demonstrates a common issue with React Router Dom v6 where nested routes unexpectedly fail to match when a wildcard catch-all route (`*`) is also present.

## Problem
The example includes a nested route structure. The wildcard route incorrectly intercepts requests intended for the nested routes.  This results in the wildcard component being rendered, even when a nested route should match.

## Solution
The solution involves re-ordering routes to ensure the most specific routes are checked first.  The catch-all route should always be placed last.