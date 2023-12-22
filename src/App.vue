<script>
import { ChipListComponent, ChipsDirective, ChipDirective} from '@syncfusion/ej2-vue-buttons';

export default {
  components:{
    'ejs-chiplist': ChipListComponent,
    'e-chips': ChipsDirective,
    'e-chip': ChipDirective
  },
  data(){
    return{
      chipText:null
    }
  },
  methods:{
    chipClick(e){
      if(e.event.target.classList.contains('e-chip-text')){
        this.chipText="Sent a text"
      }
    }
  }
}

</script>

<template>
  <div>
    <ejs-chiplist selection="Multiple" @click="chipClick" enableDelete="true" >
      <e-chips>
        <e-chip text="Andrew" leadingIconUrl="https://ej2.syncfusion.com/vue/demos/src/chips/images/andrew.png" ></e-chip>
        <e-chip text="Janet" leadingIconUrl="https://ej2.syncfusion.com/vue/demos/src/chips/images/janet.png" ></e-chip>
        <e-chip text="Laura" cssClass="e-outline" ></e-chip>
        <e-chip text="Margaret" avatarText="M" ></e-chip>
      </e-chips>
    </ejs-chiplist>
    <div class="text">{{chipText}}</div>
  </div>
</template>

<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-vue-buttons/styles/material.css";

.text {
  color: blue;
  font-weight: bold;
}
</style>
