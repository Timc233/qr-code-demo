<script setup>
import {ref} from "vue"
const userInputHistory = ref(["input a", "input b", "input c"])



</script>

<template>
<div flex h-max>
    <div class="w-1/2"
        bg-yellow>
        <div w-100 h-100
            bg-green-400
            mx-10
            my-5
            rounded-3xl
            >
            <h1 text-center
                py-35>Display Part</h1>
        </div>
        <div ml-5>
            <button v-for="i in 5"
                w-20 h-20
                m-2
                rounded-3xl
                b-0
                cursor-pointer
                bg-red-400
                hover-bg-red-500
                ease-in-out
                ></button>
        </div>
    </div>
    <div class="w-1/2"
    bg-blue
    >
       <form >
           <input placeholder="User input"
                h-10 class="w-3/4"
                mt-30 mb-10 mx-20
                rounded
                b-0
                p-3>
       </form>
       <div flex="~ wrap"
            mx-15>
           <button v-for="item in userInputHistory"
                h-8 w-120
                m-5
                b-0 rounded
                cursor-pointer
                bg-white
                hover-bg-slate-100
                >{{item}}</button>
       </div>
       
        
    </div>
</div>
</template>