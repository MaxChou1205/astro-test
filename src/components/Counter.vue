<script>
    export default {
        data() {
            return {
              count: 0,
                test:{}
            }
        },
        methods: {
            increment() {
                this.count++
            },
            decrement() {
                this.count--
            }
  },
       async mounted() {
const f = await fetch('https://jsonplaceholder.typicode.com/todos/1')
const data = await f.json()
  console.log(data)
this.test = data
        }
    }
</script>

<template>
  <button @click="count++">{{count}}</button>
  <div>
    <label for="">id</label>
    <input v-model="test.id" />

     <label for="">title</label>
    <input v-model="test.title" />
  </div>
</template>