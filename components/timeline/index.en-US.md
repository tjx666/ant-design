---
category: Components
group: Data Display
title: Timeline
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*FkTySqNt3sYAAAAAAAAAAAAADrJ8AQ/original
demo:
  cols: 2
---

Vertical display timeline.

## When To Use

- When a series of information needs to be ordered by time (ascending or descending).
- When you need a timeline to make a visual connection.

<Alert message="After version 5.2.0, we provide a simpler usage &lt;Timeline items={[...]} /&gt; with better performance and potential of writing simpler code style in your applications. Meanwhile, we deprecated the old usage in browser console, we will remove it in antd 6.0."></Alert>

```jsx
// works when >=5.2.0, recommended ✅
const items = [{ children: 'sample', label: 'sample' }];
return <Timeline items={items} />;

// works when <5.2.0, deprecated when >=5.2.0 🙅🏻‍♀️
return (
  <Timeline onChange={onChange}>
    <Timeline.Item>Sample</Timeline.Item>
  </Timeline>
);
```

## Examples

<!-- prettier-ignore -->
<code src="./demo/basic.tsx">Basic</code>
<code src="./demo/color.tsx">Color</code>
<code src="./demo/pending.tsx">Last node and Reversing</code>
<code src="./demo/alternate.tsx">Alternate</code>
<code src="./demo/custom.tsx">Custom</code>
<code src="./demo/right.tsx">Right alternate</code>
<code src="./demo/label.tsx">Label</code>
<code src="./demo/wireframe.tsx" debug>Wireframe</code>

## API

### Timeline

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| mode | By sending `alternate` the timeline will distribute the nodes to the left and right | `left` \| `alternate` \| `right` | - |
| pending | Set the last ghost node's existence or its content | boolean \| ReactNode | false |
| pendingDot | Set the dot of the last ghost node when pending is true | ReactNode | &lt;LoadingOutlined /&gt; |
| reverse | Whether reverse nodes or not | boolean | false |
| items | Each node of timeline | [Items](#Items)[] | 5.2.0 |

### Items

Node of timeline.

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| color | Set the circle's color to `blue`, `red`, `green`, `gray` or other custom colors | string | `blue` |
| dot | Customize timeline dot | ReactNode | - |
| label | Set the label | ReactNode | - |
| children | Set the content | ReactNode | - |
| position | Customize node position | `left` \| `right` | - |
