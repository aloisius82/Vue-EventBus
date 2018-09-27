<template>
    <div>
        <h2>Test</h2>
        <span v-on:testEvent="onTestEvent"  ></span>
    </div>
</template>

<script>

import { EventBus } from '../event-bus.js';

export default {
  name: 'ContMessage',
  props: {
    
  },
  methods:{
      onTestEvent(evt){
          console.log('onTestEvent', evt)
      }
  },
    mounted(){
        EventBus.$on('testEvent', evt => {
            console.log(`event bus :`, evt )
        });
    }
}
</script>
