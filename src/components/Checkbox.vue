<template >
  <div class="skills-select__block">
    <div class="input" v-for="item in items" :key="item.actv">
      <input
      type="checkbox" v-model="item.check"><label>{{item.name}}</label>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    items:[
      {name: "HTML", actv: "1", check: true},
      {name: "CSS", actv: "2", check: true},
      {name: "SCSS(SASS)", actv: "3", check: true},
      {name: "БЭМ", actv: "4", check: true},
      {name: "JQuery", actv: "5"},
      {name: "Vue.js", actv: "6"},
      {name: "Nuxt.js", actv: "7"},
      {name: "Git", actv: "8", check: true},
      {name: "Адаптивная верстка", actv: "9", check: true},
      {name: "Верстка писем", actv: "10"},
      {name: "PHP", actv: "11", check: true},
      {name: "MySql", actv: "12", check: true}
    ]})
  }
</script>
