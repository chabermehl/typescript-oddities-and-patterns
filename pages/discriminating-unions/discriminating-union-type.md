```yaml
layout: center
```

<style>
  h2 {
    padding-bottom: 0.25em;
  }
</style>

## Discriminating Union Type

```ts {all|1-7|15-16|19-20|23-25}
const Shape = {
  Circle: 'Circle',
  Square: 'Square',
  Rectangle: 'Rectangle',
} as const;

type Shapes = typeof Shape[keyof typeof Shape];

type ShapeBase = {
  color: string;
}

type DrawShape = 
| {
  shape: Shape.Circle;
  radius: number;
} & ShapeBase
| {
  shape: Shape.Square;
  width: number;
} & ShapeBase
| {
  shape: Shape.Rectangle;
  width: number;
  height: number;
} & ShapeBase;
```