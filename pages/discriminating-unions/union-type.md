```yaml
layout: center
```

<style>
  h2 {
    padding-bottom: 0.25em;
  }
</style>

## Union Type

```ts {1|4|5-9}
type Shapes = 'Circle' | 'Square' | 'Rectangle';

type DrawShape = {
  shape: Shapes;
  radius?: number;
  width?: number;
  height?: number;
  sides?: number;
  color?: string;
}
```