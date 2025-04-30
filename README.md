# reproducer for @fastify/vite yarn install stack overflow issue

```bash
yarn
```

results in:

```
➤ YN0000: · Yarn 4.9.1
➤ YN0000: ┌ Resolution step
➤ YN0085: │ + @fastify/vite@npm:8.1.2, fastify@npm:5.3.2, vite@npm:6.3.4, @babel/helper-string-parser@npm:7.27.1, and 287 more.
➤ YN0045: │ Encountered a stack overflow when resolving peer dependencies; cf /private/var/folders/2r/fcpwtn6n6gv5ym1_p28mtqzc0000gn/T/xfs-3832c0e3/stacktrace.log
➤ YN0000: └ Completed in 3s 751ms
➤ YN0000: · Failed with errors in 3s 765ms
```

with the following stacktrace:

```
1. fastify-vite-yarn@workspace:.
2. @fastify/vite@virtual:498e3a16bbcb7f952c7b7ea65005f317a82f3aa89962cae25c3135e76ac4d3442ece6162e0b525de7cc5dee2d7314c1e83ba1c1ba7c6da5b4217e3d63c1f8d2d#npm:8.1.2
3. @fastify/react@npm:1.0.2
4. @fastify/vite@virtual:8fbef1c85e3f6768f43d511c0b0533dbb044c1746dd63cc7148ed48593e3af6fb617456d57844e7b480cc36eab896b055fec14fcafc07623c1f2a0ff25629fee#npm:8.1.2
5. @fastify/vue@npm:1.1.0
```
