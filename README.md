# Steps

1. yarn
2. yarn dev
3. Check browser console:

```
[Vue warn]: Hydration node mismatch:
- Client vnode: div
- Server rendered DOM: <componenta>​</componenta>​
  at <ComponentA>
  at <Home onVnodeUnmounted=fn<onVnodeUnmounted> ref=Ref< undefined > >
  at <RouterView>
  at <App>
```

Also check terminal output:

```
[Vue warn]: resolveComponent can only be used in render() or setup().
```

4. Remove `<my-x />` from template OR replace it with `<div />`. Notice no hydration error.

# Point of interest

`/src/pages/Home.vue`. The rest of the files don't matter.
