<script setup>
import { Client } from "@gradio/client";
</script>
<script>
const client = await Client.connect("KingNish/OpenGPT-4o");
console.log(client);

const result = await client.predict("/chat", { 		
  user_prompt: {"text":"Hello!","files":[]}, 		
  model_selector: "idefics2-8b-chatty", 		
  decoding_strategy: "Greedy",
  temperature: 0, 		
  max_new_tokens: 2048, 		
  repetition_penalty: 0.01, 		
  top_p: 0.01, 		
  web_search: true
});

console.log(result.data);
document.querySelector("#response").innerText = result.data;
</script>

<template>
  <header>
    
  </header>

  <main>
  </main>
</template>