---
title: removeObjectElement
tags: object,intermediate
---

Remove element from object without mutating original.

- Use destructuring on assigning variable
- Pick up the field that you don't want and the rest elements (`...rest`) would be the result

```js
const noFirstName = (value) => {
  /* Remove `firstName` from user by destructuring */
  const { firstName, ...result } = user

  /* The `result` would have no `firstName` */
  return { ...result }
}

const user = {
  firstName: 'John',
  lastName: 'Doe',
  age: 24
}

noFirstName(user)
```