# webpack dependency demo using npm@3

Dependency tree:

```
    A <- entry
   / \
  B   C
     /
    B
```

- `npm install -g npm@3`
- `cd A`
- `npm install`
- `npm run build`

The dependencies between A, B, and C are specified using local paths.

Look at `A/dist/out.js` — it will contain 1 version of `B`.

Change some code in B or C, run `npm install`, and the local installations in A
should be updated when using npm@3 (but not when using npm@2).
