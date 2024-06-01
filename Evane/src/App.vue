<script setup>
import { Client } from "@gradio/client";
</script>
<script>
const client = await Client.connect("KingNish/OpenGPT-4o");
console.log(client);

const result = await client.predict("/chat", { 		
  message: {"text":"sample text","files":[]},
  request: "idefics2-8b-chatty",
  param_3: "Greedy",
  param_4: 0,
  param_5: 2048,
  param_6: 0.01,
  param_7: 0.01,
  audio: null,
  image3: null,
});

console.log(result.data);
</script>

<template>
  <header>
    
  </header>

  <main>
  </main>
</template>