---
title: 'use-focus-trap'
group: 'svelteuidev-composables'
packageGroup: '@svelteuidev/composables'
slug: /composables/use-focus-trap/
description: 'Traps the focus inside the given DOM node'
import: "import { focustrap } from '@svelteuidev/composables';"
docs: 'composables/use-focus-trap.md'
source: 'svelteui-composables/src/actions/use-focus/use-focus-trap.ts'
---

<script lang='ts'>
    import { Demo, ComposableDemos } from '@svelteuidev/demos';
    import { Heading } from 'components';
</script>

<Heading />

## Usage

The `use-focus-trap` action traps the focus inside a given DOM node. The node must include at least one focusable element, and it will give priority to a node with the `autofocus` property.

```svelte
<script>
  import { focustrap } from './use-focus-trap';
</script>

<div use:focustrap>
  <h1>Title</h1>
  <input /> <!-- This will be focused -->
</div>
```

## Definition

```ts
export function focustrap(node: HTMLElement): ReturnType<Action>;
```
