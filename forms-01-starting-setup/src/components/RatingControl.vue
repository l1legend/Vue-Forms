<template>
  <ul>
    <li :class="{active: activateOption === 'poor'}"><button type="button" @click="activate('poor')">Poor</button></li>
    <li :class="{active: activateOption === 'average'}"><button type="button" @click="activate('average')">Average</button></li>
    <li :class="{active: activateOption === 'great'}"><button type="button" @click="activate('great')">Great</button></li>
  </ul>
</template>

<script>
export default {
    data() {
        return {
            activeOption: null
        };
    },
    methods: {
        activate(option) {
            this.activeOption = option;
        }
    }
}
</script>

<style scoped>
.active {
    border-color: #a00078;
}

.active button {
    color: #a00078;
}

ul {
    list-style: none;
    margin: 0.5rem 0;
    padding: 0;
    display: flex;
}

li {
    margin: 0 1 rem;
    border: 1px solid #ccc;
    padding: 1 rem;
    display: flex;
    justify-content: center;
    align-items: center;
}

button {
    font: inherit;
    border: none;
    background-color: transparent;
    cursor: pointer;
}
</style>