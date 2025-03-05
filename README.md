# turbo-caret-bug

1. `yarn install`
2. `turbo c#build:app:recursive --force`

Output:

```
c:build:app: cache bypass, force executing c6789a69995e9773
b:build:app: cache bypass, force executing 998750810f885b11
c:build:app:
b:build:app:
b:build:app: b#build:app
c:build:app: c#build:app

 Tasks:    2 successful, 2 total
Cached:    0 cached, 2 total
  Time:    317ms
```

Expected: a#build:app should run first, since b depends on a.
