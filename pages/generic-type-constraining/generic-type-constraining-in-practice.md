```yaml
layout: center
```

<style>
  h2 {
    padding-bottom: 0.25em;
  }
</style>

## Generic Type Constraining In Practice

```ts {8-9|11|1-5|14-15|all}
interface IMultiListField<TValue, TComponents> {
  /** `react-select` component overrides */
  components?: TComponents;
  // ... other props omitted for brevity
}

const MultiListField = <
  TValue extends {value: string; label: string},
  TComponents extends SelectComponentsConfig<TValue, true, GroupBase<TValue>>
>(
  props: IMultiListField<TValue, TComponents>
): JSX.Element => {
  return (
    <Select<TValue, true, GroupBase<TValue>>
      components={components}
      // ... other props omitted for brevity
    />
  );
}
```