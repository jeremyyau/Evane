<script setup>
import { Client } from "@gradio/client";
</script>
<script>
// const client = await Client.connect("KingNish/OpenGPT-4o");
// console.log(client);

// const result = await client.predict("/chat", { 		
//   message: {"text":"sample text","files":[]},
//   request: "idefics2-8b-chatty",
//   param_3: "Greedy",
//   param_4: 0,
//   param_5: 2048,
//   param_6: 0.01,
//   param_7: 0.01,
//   audio: null,
//   image3: null,
// });

// console.log(result);
const app = await Client.connect("KingNish/JARVIS");
const result = await app.predict("/predict_1", [		
				"用繁體中文回答我，你是建基於甚麼model？", // string  in 'User' Textbox component		
				"Mixtral 8x7B", // string  in 'Model' Dropdown component		
				0, // number (numeric value between 0 and 999999) in 'Seed' Slider component
]);

console.log(result.data);
document.querySelector("#response").innerText = result.data;
</script>

<template>
  <header>
    
  </header>

  <main>
  </main>
</template>