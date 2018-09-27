<template>
    <div>
        <button   @click="onClick" >Push</button>
    </div>
</template>

<script>
import { EventBus } from '../event-bus.js';

console.log(EventBus)

export default {
    name:"ContControl",
    methods:{
        onClick(){
            // this.$emit('testEvent', 'test event message')
            EventBus.$emit('testEvent', 'test event message');
        }
    },
    computed:{
        // inputListeners : function(){
        //     var vm = this
        //     return Object.assign({},
        //         // We add all the listeners from the parent
        //         this.$listeners,
        //         // Then we can add custom listeners or override the
        //         // behavior of some listeners.
        //         {
        //         // This ensures that the component works with v-model
        //         input: function (event) {
        //             vm.$emit('input', event.target.value)
        //         }
        //         }
        //     )
        // }
    },
    mounted(){
        console.log(this.$bus)
        // this.$bus.$on('testEvent', function(evt){
        //     console.log(evt)
        // })
    }
}
</script>

