# next-transpile-modules-issue-36
Reproduction of https://github.com/martpie/next-transpile-modules/issues/36

## Usage

```
npm install --global pnpm@3.4.1
pnpm install
pnpm run dev
```

Observe this output:

```
Starting the development server ...

  > Waiting on http://localhost:3000
> Using "webpackDevMiddleware" config function defined in next.config.js.
[ ModuleNotFoundError: Module not found: Error: Can't resolve 'object-assign' in '/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/react-dom/cjs'
    at factory.create (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/webpack/4.29.0_webpack@4.29.0/node_modules/webpack/lib/Compilation.js:823:10)
    at factory (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/webpack/4.29.0_webpack@4.29.0/node_modules/webpack/lib/NormalModuleFactory.js:397:22)
    at resolver (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/webpack/4.29.0_webpack@4.29.0/node_modules/webpack/lib/NormalModuleFactory.js:130:21)
    at asyncLib.parallel (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/webpack/4.29.0_webpack@4.29.0/node_modules/webpack/lib/NormalModuleFactory.js:224:22)
    at /Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/neo-async/2.6.1/node_modules/neo-async/async.js:2830:7
    at /Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/neo-async/2.6.1/node_modules/neo-async/async.js:6877:13
    at normalResolver.resolve (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/webpack/4.29.0_webpack@4.29.0/node_modules/webpack/lib/NormalModuleFactory.js:214:25)
    at doResolve (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/enhanced-resolve/4.1.0/node_modules/enhanced-resolve/lib/Resolver.js:184:12)
    at hook.callAsync (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/enhanced-resolve/4.1.0/node_modules/enhanced-resolve/lib/Resolver.js:238:5)
    at _fn0 (eval at create (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/tapable/1.1.3/node_modules/tapable/lib/HookCodeFactory.js:33:10), <anonymous>:15:1)
    at resolver.doResolve (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/enhanced-resolve/4.1.0/node_modules/enhanced-resolve/lib/UnsafeCachePlugin.js:37:5)
    at hook.callAsync (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/enhanced-resolve/4.1.0/node_modules/enhanced-resolve/lib/Resolver.js:238:5)
    at _fn0 (eval at create (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/tapable/1.1.3/node_modules/tapable/lib/HookCodeFactory.js:33:10), <anonymous>:15:1)
    at hook.callAsync (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/enhanced-resolve/4.1.0/node_modules/enhanced-resolve/lib/Resolver.js:238:5)
    at _fn0 (eval at create (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/tapable/1.1.3/node_modules/tapable/lib/HookCodeFactory.js:33:10), <anonymous>:27:1)
    at resolver.doResolve (/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/.registry.npmjs.org/enhanced-resolve/4.1.0/node_modules/enhanced-resolve/lib/DescriptionFilePlugin.js:42:38)
resolve 'object-assign' in '/Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/react-dom/cjs'
  Parsed request is a module
  using description file: /Users/spencerelliott/Dev/elliottsj/next-transpile-modules-issue-36/node_modules/react-dom/package.json (relative path: ./cjs)
    resolve as module

...continued
```
