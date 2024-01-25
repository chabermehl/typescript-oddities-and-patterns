```yaml
layout: center
```

<style>
  h2 {
    padding-bottom: 0.25em;
  }
</style>

## With Some Additional Help From TypeScript

```ts twoslash
const Shape = {
  Circle: 'Circle',
  Square: 'Square',
  Rectangle: 'Rectangle',
} as const;

type Shapes = typeof Shape[keyof typeof Shape];
//    ^?
```