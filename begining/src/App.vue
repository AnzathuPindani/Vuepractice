<script setup>
import {ref} from 'vue';
const name = ref('Rachel');
const href=ref('https://www.scrimba.com');
const disabled = ref(true);
const attributes={
  id:'big_emoji',
  class:'waving',
}
const coding_years=ref(0);
const getFormattedDate=(date)=>{
  const options={year:'numeric',month:'long',day:'numeric'};
  return date.toLocaleDateString('en-UK',options);
}
const username=ref('rachelktjohnson');
const event=ref('dblclick');
const blockLeave=()=>{
alert("You can't Leave");
};

</script>

<template>
  <div>
    <h1>Hi, my name is {{ name }}</h1>
    <a :href="href" target="_blank">
      <button :disabled="disabled">Click to visit my favourite website</button>
    </a>

    <h2 v-on:[event]="coding_years++">{{ coding_years }}</h2>
  </div>

</template>

