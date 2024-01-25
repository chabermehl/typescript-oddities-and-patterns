```yaml
layout: center
```

<style>
  h2 {
    padding-bottom: 0.25em;
  }
</style>

## Generic Type Constraining Basics

```ts {1-3|5|6}
const logString = <TString extends string>(toLog: TString) => {
    console.log(toLog);
}

logString("this is my string to log");
logString(1045);
```
