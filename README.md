### sweetalert
---
https://github.com/t4t5/sweetalert

```
npm install --save sweetalert
```

```js
import swal from 'sweetalert';
swal("Hello");

swal("Opps!", "Something went wrong!", "error");

swal({
  title: "Are you sure?",
  text: "Are you sure that you to leave this page?",
  icon: "warning",
  dangerMode: true,
})
.then(willDelete => {
  if(willDelete) {
    swal("Deleted!", "Your imaginary file has been deleted!", "success");
  }
});

const willDelete = await swal({
  title: "Are you sure?",
  text: "Are you sure that you want to delete this file?",
  icon: "warning",
  dangerMode: true,
});

if(willDelete) {
  swal("Deleted!", "Your imaginary file has been deleted!", "success");
}

swal("Type something:", {
  content: "input",
})
.then((value) => {
  swal(`You typed: ${value}`);
});

const value = await swal("Type something:", {
  content: "input",
});
swal(`You typed: ${value}`);

swal({
  text: "Wanna log some information about Bulbasur?",
  button: {
    text: "Search!",
    closeModal: false,
  }
})
.then(willSearch => {
  if (willSearch){
    return fetch("http://pokeapi.co/api/v2/pokemon/1");
  }
})
.then(result => rsult.json())
.then(json => console.log(json))
.catch(err => {
  swal("Opps!", "Seems like we couldn't fetch the info", "error");
});

const willSearch = await swal({
  text: "Wanna log some information about Bulbasaur?",
  button: {
    text: "Search!",
    closeModal: false,
  },
});
if(willSearch) {
  try {
    const result = await fetch("http://pokeapi.co/api/v2/pokemon/1");
    const json = await result.json();
    console.log(json);
  } catch(err){
    swal("Opps!", "Seems like we couldn't fetch the info", "error");
  }
}

import React from 'react'
import swal from '@sweetalert/with-react'
swal(
  <div>
    <h1>Hello</h1>
    <p>
      This is now rendered with JSX!
    </p>
  </div>
)
```

```
```

