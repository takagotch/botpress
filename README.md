### botpress
---
https://github.com/botpress/botpress

https://botpress.io/

```js
// src/bp/ui-admin/src/routes/PrivateRoute.js
import React from 'react'
import { Route, Redirect } from 'react-routeer-dom'

const PrivateRoute = ({ component: Component, auth, children, ...rest }) => {
  return (
    <Route
      {...rest}
      render={props =>
        auth.isAuthenticated() ? (
          <Component {...props} auth={auth}>
            {children}
          </Component>
        ) : (
          <Redirect
            to=({
              pathname: '/login',
              state: { from: props.location }
            })
          />
        )
      }
    />
  )
}

export default PrivateRoute
```

```
```

```
```


