<template>
  <div class="home">
    <h1>Home</h1>
    <h1>Refs</h1>
    <p>My name is {{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">Click me</button>
    <h2>Reactivee</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
    <button @click="updateNinjaTwo">Click me</button>
    <br />
    <br />
    <button @click="test">Test</button>
    <hr />
    <h2>Computed</h2>

    <input type="text" v-model="search" />
    <p>search term - {{ search }}</p>
    <div v-for="name in matchingNames" :key="name">
      <p>{{ name }}</p>
    </div>

    <button @click="handleClick">Stop watching</button>
  </div>
</template>

<script>
import { ref, reactive, computed, watch, watchEffect } from "vue";

export default {
  name: "Home",
  setup() {
    // Setup allways runs first
    // Reactive don't work on primitive type
    const ninjaOne = ref({ name: "mario", age: 30 });
    const ninjaTwo = reactive({ name: "luigi", age: 35 });

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40;
    };

    const updateNinjaTwo = () => {
      ninjaTwo.age = 45;
    };

    // Computed properties
    const search = ref("");
    const names = ref([
      "mario",
      "yoshi",
      "luigi",
      "toad",
      "bowser",
      "koopa",
      "peach",
    ]);

    const stopWatch = watch(search, () => {
      console.log("watch function ran");
    });

    // Allways runs initially
    const stopEffect = watchEffect(() => {
      console.log("watchEffect function ran", search.value);
    });

    const matchingNames = computed(() => {
      return names.value.filter((name) => name.includes(search.value));
    });

    const handleClick = () => {
      stopWatch();
      stopEffect();
    };

    return {
      ninjaOne,
      updateNinjaOne,
      ninjaTwo,
      updateNinjaTwo,
      names,
      search,
      matchingNames,
      handleClick,
    };
  },
  data() {
    return {
      // Reactive values
    };
  },
  methods: {
    test() {
      // console.log(this.age);
      this.ninjaTwo.age = 9;
      this.ninjaOne.age = 9;
      // console.log(this.age);
    },
  },
};
</script>
