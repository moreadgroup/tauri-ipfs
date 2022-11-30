<script lang="ts">
  import { onMount, afterUpdate } from "svelte";

  import * as IPFS from "ipfs-core";

  import type { CID } from "multiformats";
  import { webSockets } from "@libp2p/websockets";
  import { all } from "@libp2p/websockets/filters";

  afterUpdate(async () => {
    const ws = webSockets({
      filter: all,
    });
    const node = await IPFS.create({
      config: {
        Bootstrap: [],
      },
      libp2p: {
        transports: [ws],
        connectionManager: {
          autoDial: false,
        },
      },
    });

    const version = await node.version();

    console.log("Version:", version.version);

    const file = await node.add({
      path: "hello.txt",
      content: new TextEncoder().encode("Hello World 101"),
    });

    console.log(
      "Added file, file.path=",
      file.path,
      " file.cid=",
      file.cid.toString()
    );
    try {
      // @ts-expect-error CID has no toUpperCase method
      file.cid.toUpperCase();
    } catch (error) {}

    const content = await readFile(node, file.cid);

    console.log("Added file contents:", content);
  });
  const readFile = async (ipfs: IPFS.IPFS, cid: CID): Promise<string> => {
    const decoder = new TextDecoder();
    let content = "";

    for await (const chunk of ipfs.cat(cid)) {
      content += decoder.decode(chunk, {
        stream: true,
      });
    }

    return content;
  };
</script>

<h1 class="text-3xl font-medium bg-red-400 p-5 mt-10">Tauri ipfs</h1>
<div>test tauri ipfs integration</div>

<ul class="grid grid-flow-row  gap-4 ">
  <div class="grid grid-flow-row grid-cols-2">
    <h1 class="bg-blue-400 text-3xl font-medium px-2 m-2">IPFS Node</h1>
    <input
      class="m-2"
      type="text"
      value="/Users/CC/github/ipfs/sample/hello.txt"
      disabled
    />
  </div>

  <div class="grid grid-flow-row grid-cols-2">
    <h1 class="bg-blue-400 text-3xl font-medium px-2 m-2">Cid</h1>
    <input
      class="m-2"
      type="text"
      value="QmTiy2nSQ1wbftsxpubSx11EgcwPVrMQKVjKaKuN9tfqdS"
      disabled
    />
  </div>

  <div class="grid grid-flow-row grid-cols-2">
    <h1 class="bg-blue-400 text-3xl font-medium px-2 m-2">Title</h1>
    <input class="m-2" type="text" value="title" />
  </div>

  <div class="grid grid-flow-row grid-cols-2">
    <h1 class="bg-blue-400 text-3xl font-medium px-2 m-2">Body</h1>
    <textarea class="m-2" type="textarea" value="body" cols="30" rows="6" />
  </div>

  <div class="grid grid-flow-row grid-cols-2">
    <h1 class="bg-blue-400 text-3xl font-medium px-2 m-2">Tags</h1>
    <textarea class="m-2" type="textarea" value="tags" cols="30" rows="6" />
  </div>

  <button class="bg-blue-500 border border-solid border-black m-2 ">
    <h1 class="bg-blue-400 text-3xl font-medium ">
      Publish to IPFS Carefully!
    </h1>
  </button>
</ul>

<h1 class="text-3xl font-medium bg-red-400 p-5 mt-10">
  Warnings: Your File Will be public accessible if you publish it to IPFS
  network. The accessiblity can not be revoked!
</h1>
