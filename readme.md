# Vite + unified + Yarn2 example

when trying to use `unified` within a `yarn2` project it does throw an error because is trying to import a node dependency that is not listed in the project:

```bash
➜ yarn dev
Pre-bundling dependencies:
  rehype-stringify
  remark-gfm
  remark-parse
  remark-rehype
  unified
  (...and 1 more)
(this will be run only when your dependencies or config have changed)
 > .yarn/cache/vfile-npm-5.2.0-316febbe4f-9a2fc257ec.zip/node_modules/vfile/lib/minurl.js:1:8: error: No matching export in "browser-external:url" for import "fileURLToPath"
    1 │ export {fileURLToPath as urlToPath} from 'url'
      ╵         ~~~~~~~~~~~~~

 > .yarn/cache/vfile-npm-5.2.0-316febbe4f-9a2fc257ec.zip/node_modules/vfile/lib/minurl.js:1:8: error: No matching export in "browser-external:url" for import "fileURLToPath"
    1 │ export {fileURLToPath as urlToPath} from 'url'
      ╵         ~~~~~~~~~~~~~

error when starting dev server:
Error: Build failed with 2 errors:
.yarn/cache/vfile-npm-5.2.0-316febbe4f-9a2fc257ec.zip/node_modules/vfile/lib/minurl.js:1:8: error: No matching export in "browser-external:url" for import "fileURLToPath"
.yarn/cache/vfile-npm-5.2.0-316febbe4f-9a2fc257ec.zip/node_modules/vfile/lib/minurl.js:1:8: error: No matching export in "browser-external:url" for import "fileURLToPath"
    at failureErrorWithLog (/Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:1493:15)
    at /Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:1151:28
    at runOnEndCallbacks (/Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:941:63)
    at buildResponseToResult (/Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:1149:7)
    at /Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:1258:14
    at /Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:629:9
    at handleIncomingPacket (/Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:726:9)
    at Socket.readFromStdout (/Users/horacio/workspace/playground/unified-demo-vite/.yarn/unplugged/esbuild-npm-0.13.13-3fef6f7bc5/node_modules/esbuild/lib/main.js:596:7)
    at Socket.emit (node:events:394:28)
    at addChunk (node:internal/streams/readable:312:12)
Command failed: /Users/horacio/.yvm/versions/v1.22.15/bin/yarn.js dev
```
