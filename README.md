# vuex-console-log

```js
const store = [...document.querySelectorAll('*')]
  .find(el => el.__vue__)
  .__vue__
  .$store;

store
  .subscribe(({ type, payload }, state) => {
    console.log(
      `%c Mutation:   ${type} `,
      'background: #333; color: #bada55',
      {
        payload,
        state
      }
    );
  });

store
  .subscribeAction(({ type, payload }, state) => {
    console.log(
      `%c Action:     ${type} `,
      'background: #333; color: #54afbd',
      {
        payload,
        state
      }
    );
  });
```
