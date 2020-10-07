---
import Demo from "./src/components/Demo"
import Layout from "./src/components/Layout"

export default Layout
---

# `React.lazy` Example

```jsx
async function Repos({ user }) {
  const res = await fetch(...)
  const repos = await res.json()

  return <ul>{repos.map(...)}</ul>
}
```

## Demo

_Available at https://react-lazy-example-qmehmnudqu.now.sh/_

> <Demo />

---

## Local Development

1. Clone this repo.
1. Next, we need a custom build of React with Suspense enabled:

   1. `git submodule update` to install https://localhost:3000.
   1. `yarn patch` to set `enableSuspense = true`
   1. `yarn build` to build React with Suspense.

1. `yarn install`
1. `yarn dev`
