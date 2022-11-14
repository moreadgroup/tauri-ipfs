# Svelte-Kit + Vite

This template should help get you started developing with Tauri and Svelte-Kit in Vite.

## Recommended IDE Setup

[VS Code](https://code.visualstudio.com/) + [Svelte](https://marketplace.visualstudio.com/items?itemName=svelte.svelte-vscode) + [Tauri](https://marketplace.visualstudio.com/items?itemName=tauri-apps.tauri-vscode) + [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer).



## Errors

github/moreadgroup/tauri-ipfs via  v16.17.0 took 9s
❯ pnpm tauri dev

> tauri-ipfs@0.0.0 tauri /Users/CC/github/moreadgroup/tauri-ipfs
> tauri "dev"

     Running BeforeDevCommand (`pnpm dev`)

> tauri-ipfs@0.0.0 dev /Users/CC/github/moreadgroup/tauri-ipfs
> vite dev


  VITE v3.2.3  ready in 1290 ms

  ➜  Local:   http://localhost:1420/
  ➜  Network: use --host to expose
        Info Watching /Users/CC/github/moreadgroup/tauri-ipfs/src-tauri for changes...
   Compiling mac-notification-sys v0.5.6
   Compiling notify-rust v4.5.10
   Compiling tauri v1.2.0
   Compiling tauri-ipfs v0.0.0 (/Users/CC/github/moreadgroup/tauri-ipfs/src-tauri)
    Finished dev [unoptimized + debuginfo] target(s) in 12.93s
4:11:29 PM [vite-plugin-svelte] /Users/CC/github/moreadgroup/tauri-ipfs/src/routes/+page.svelte:22:2 Security: Anchor with "target=_blank" should have rel attribute containing the value "noreferrer"
4:11:29 PM [vite-plugin-svelte] /Users/CC/github/moreadgroup/tauri-ipfs/src/routes/+page.svelte:25:2 Security: Anchor with "target=_blank" should have rel attribute containing the value "noreferrer"
4:11:29 PM [vite-plugin-svelte] /Users/CC/github/moreadgroup/tauri-ipfs/src/routes/+page.svelte:28:2 Security: Anchor with "target=_blank" should have rel attribute containing the value "noreferrer"
✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/ipfs-core@0.17.0_undici@5.12.0/node_modules/ipfs-core/src/ipns/publisher.js:199:20:
      199 │     let seqNumber = 0n
          ╵                     ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/ipns@4.0.0_undici@5.12.0/node_modules/ipns/dist/src/selector.js:17:41:
      17 │         const aSeq = a.entry.sequence ?? 0n;
         ╵                                          ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/ipns@4.0.0_undici@5.12.0/node_modules/ipns/dist/src/selector.js:18:41:
      18 │         const bSeq = b.entry.sequence ?? 0n;
         ╵                                          ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/ipns@4.0.0_undici@5.12.0/node_modules/ipns/dist/src/utils.js:116:38:
      116 │         sequence: message.sequence ?? 0n,
          ╵                                       ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/longbits@1.1.0/node_modules/longbits/dist/src/index.js:13:69:
      13 │ ...t(this.lo >>> 0) + (BigInt(this.hi >>> 0) << 32n);
         ╵                                                 ~~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/longbits@1.1.0/node_modules/longbits/dist/src/index.js:21:49:
      21 │ ...       return -(BigInt(lo) + (BigInt(hi) << 32n));
         ╵                                                ~~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/longbits@1.1.0/node_modules/longbits/dist/src/index.js:23:65:
      23 │ ...t(this.lo >>> 0) + (BigInt(this.hi >>> 0) << 32n);
         ╵                                                 ~~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/longbits@1.1.0/node_modules/longbits/dist/src/index.js:70:22:
      70 │         if (value === 0n) {
         ╵                       ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/longbits@1.1.0/node_modules/longbits/dist/src/index.js:77:33:
      77 │         let hi = Number(value >> 32n) | 0;
         ╵                                  ~~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/longbits@1.1.0/node_modules/longbits/dist/src/index.js:78:47:
      78 │ ... let lo = Number(value - (BigInt(hi) << 32n)) | 0;
         ╵                                            ~~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/libp2p@0.40.0_undici@5.12.0/node_modules/libp2p/dist/src/metrics/stats.js:14:26:
      14 │             dataReceived: 0n,
         ╵                           ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/libp2p@0.40.0_undici@5.12.0/node_modules/libp2p/dist/src/metrics/stats.js:15:22:
      15 │             dataSent: 0n
         ╵                       ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/libp2p@0.40.0_undici@5.12.0/node_modules/libp2p/dist/src/metrics/stats.js:29:30:
      29 │             this.stats[key] = 0n;
         ╵                               ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/libp2p@0.40.0_undici@5.12.0/node_modules/libp2p/dist/src/metrics/stats.js:169:34:
      169 │             n = this.stats[key] = 0n;
          ╵                                   ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/@libp2p+peer-record@4.0.4_undici@5.12.0/node_modules/@libp2p/peer-record/dist/src/peer-record/peer-record.js:63:63:
      63 │ ... (opts.writeDefaults === true || obj.seq !== 0n) {
         ╵                                                 ~~

✘ [ERROR] Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)

    node_modules/.pnpm/@libp2p+peer-record@4.0.4_undici@5.12.0/node_modules/@libp2p/peer-record/dist/src/peer-record/peer-record.js:81:25:
      81 │                     seq: 0n,
         ╵                          ~~

4:11:35 PM [vite] error while updating dependencies:
Error: Build failed with 16 errors:
node_modules/.pnpm/@libp2p+peer-record@4.0.4_undici@5.12.0/node_modules/@libp2p/peer-record/dist/src/peer-record/peer-record.js:63:63: ERROR: Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)
node_modules/.pnpm/@libp2p+peer-record@4.0.4_undici@5.12.0/node_modules/@libp2p/peer-record/dist/src/peer-record/peer-record.js:81:25: ERROR: Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)
node_modules/.pnpm/ipfs-core@0.17.0_undici@5.12.0/node_modules/ipfs-core/src/ipns/publisher.js:199:20: ERROR: Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)
node_modules/.pnpm/ipns@4.0.0_undici@5.12.0/node_modules/ipns/dist/src/selector.js:17:41: ERROR: Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)
node_modules/.pnpm/ipns@4.0.0_undici@5.12.0/node_modules/ipns/dist/src/selector.js:18:41: ERROR: Big integer literals are not available in the configured target environment ("chrome87", "edge88", "es2020", "firefox78", "safari13" + 2 overrides)
...
    at failureErrorWithLog (/Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:1566:15)
    at /Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:1024:28
    at runOnEndCallbacks (/Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:1438:61)
    at buildResponseToResult (/Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:1022:7)
    at /Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:1134:14
    at responseCallbacks.<computed> (/Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:671:9)
    at handleIncomingPacket (/Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:726:9)
    at Socket.readFromStdout (/Users/CC/github/moreadgroup/tauri-ipfs/node_modules/.pnpm/esbuild@0.15.13/node_modules/esbuild/lib/main.js:647:7)
    at Socket.emit (node:events:513:28)
    at addChunk (node:internal/streams/readable:315:12)

