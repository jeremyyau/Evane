<script setup>
  import { Client } from "@gradio/client";
</script>
<script> 
  async function runGradioClient() {
    const client = await Client.connect("KingNish/OpenGPT-4o");

    console.log(client);
    const result = await client.predict("/chat", {
      user_prompt: { "text": "sample text", "files": [] },
      web_search: true,
      image3: null,
    });
    console.log(result.data);
    document.getElementById("result").innerText = result.data;
  }

  runGradioClient().catch(error => console.error(error));
</script>

<template>
  <header>
    
  </header>

  <main>
  </main>
</template>