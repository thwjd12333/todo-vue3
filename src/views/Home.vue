<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
    <div>{{ test }}</div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue"
import HelloWorld from "@/components/HelloWorld.vue" // @ is an alias to /src

export default defineComponent({
  name: "Home",
  components: {
    HelloWorld,
  },
  setup() {
    class Person {
      public age: number
      private geder: string
      constructor(gender: string, age: number) {
        this.geder = gender
        this.age = age
      }
    }
    const p = new Person("W", 23)
    let test: number = 0
    if (p.age) {
      test = p.age
    }

    class Enemy extends Person {
      location: string

      constructor(geder: string, age: number, location: string) {
        super(geder, age)
        this.location = location
      }
    }

    // interface IPerson {
    //   name: string
    //   age: number
    //   ssn?: string
    // }
    // class Person {
    //   constructor(public config: IPerson) {}
    // }
    // let ePerson: IPerson = {
    //   name: "Kang",
    //   age: 23,
    // }

    // let p = new Person(ePerson)

    // let test: string = "test입니다."

    //test = p.geder
    return {
      // test,
    }
  },
})
</script>
