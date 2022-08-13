<template>
<div class="puzzleBox">
<div class="puzzle">
    <draggable
      v-model="list1"
      group="zboom"
      class="draggable"
      @start="drag = true"
      @end="drag = false"
    >
      <template #item="{ element }">
        <div class="letter">
          {{ element.name }}
        </div>
      </template>
    </draggable>
  </div>
  <div class="puzzle">
    <draggable
      v-model="list2"
      group="zboom"
      class="draggable"
      @start="drag = true"
      @end="drag = false"
    >
      <template #item="{ element }">
        <div class="letter">
          {{ element.name }}
        </div>
      </template>
    </draggable>
  </div>
  <div class="puzzle">
    <draggable
      v-model="list3"
      group="zboom"
      class="draggable"
      @start="drag = true"
      @end="drag = false"
    >
      <template #item="{ element }">
        <div class="letter">
          {{ element.name }}
        </div>
      </template>
    </draggable>
  </div>
  <div class="puzzle">
    <draggable
      v-model="list4"
      group="zboom"
      class="draggable"
      @start="drag = true"
      @end="drag = false"
    >
      <template #item="{ element }">
        <div class="letter">
          {{ element.name }}
        </div>
      </template>
    </draggable>
  </div>
  <div class="puzzle">
    <draggable
      v-model="list5"
      group="zboom"
      class="draggable"
      @start="drag = true"
      @end="drag = false"
    >
      <template #item="{ element }">
        <div class="letter">
          {{ element.name }}
        </div>
      </template>
    </draggable>
  </div>
</div>
<div>
  <div class="puzzle">
    <draggable
      v-model="list6"
      group="zboom"
      class="draggable"
      @start="drag = true"
      @end="drag = false"
    >
      <template #item="{ element }">
        <div class="letter">
          {{ element.name }}
        </div>
      </template>
    </draggable>
  </div>
</div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import draggable from "vuedraggable";

const drag = ref(false);

let list1 = ref([{ id: "001", name: "B" }]);
let list2 = ref([{ id: "002", name: "M" }]);
let list3 = ref([{ id: "003", name: "O" }]);
let list4 = ref([{ id: "004", name: "O" }]);
let list5 = ref([{ id: "005", name: "Z" }]);
let list6 = ref([]);
let draggableProps = {
  animation: 300,
};
</script>

<style scoped lang="scss">
.letter {
  font-size: 8rem;
  color:#888;
}
.puzzle{
  width: 10rem;
  height: 10rem;
  background-color: #282828;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 2rem;
  box-shadow: inset 0 2px 2px #111;
}
.puzzleBox{
  display: flex;
}

.draggable{
  width: 100%;
  height: 100%;
}
</style>
