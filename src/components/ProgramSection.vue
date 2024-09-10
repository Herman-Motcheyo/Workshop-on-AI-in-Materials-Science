<template>

  <section>
    <hr style="height:30px">
    <h2>{{ day }}</h2>
    <div class="program">
     
      <table id="PUTSPEAKERNAMEHERE" v-for="item in program" :key="item.time" >
        <tr>
          <td class="date" rowspan="3">
            {{ item.time }}
          </td>
          <td class="title">
            {{ item.title }}
          </td>
        </tr>
        <tr>
          <td class="speaker">
            {{ item.speaker == null ? '' : `${item.speaker} - (${item.affiliation})` }}
          </td>
        </tr>

      </table>
    </div>
   
  </section>
</template>


<script setup>
import { defineProps } from 'vue';
const props = defineProps(
  {
    program: {
      type: Array,
      required: true,
      default: () => []
    },
    day:{
      type:String,
      required: true
    }
  }
)
console.log(props);

</script>

<style scoped>
.program {
  padding: 20px;
  background-color: #e9ecef;
}

.program ul {
  list-style-type: none;
}
</style>