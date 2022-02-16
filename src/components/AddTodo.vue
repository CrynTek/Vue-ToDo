<template>

  <div class="container">
    <v-container>
      <h1>การบ้าน/งานที่ได้รับมอบหมาย</h1>
      <v-select v-model="select" :items="items" label="--วิชา--" solo></v-select>
      <v-text-field v-model="name" label="รายละเอียด" outlined></v-text-field>
      <center>
      <v-btn color="success" class="mr-4" @click="validate()">เพิ่ม</v-btn>
      </center>
    </v-container>
  </div>
</template>


<script>
export default {
  subject: "",
  work: "",
  data() {
    return {
      select:"",
      name:"",
      items: ["  คพ232 สถาปัตยกรรมคอมพิวเตอร์", "  คพ252 คณิตศาสตร์สำหรับวิทยาการคอมพิวเตอร์", "  คพ313 การพัฒนาโปรแกรมประยุกต์บนเว็บ", "  คพ343 การวิเคราะห์และออกแบบเชิงวัตถุ","  ศท013 สุขภาพเพื่อการดำรงชีวิต","  อื่นๆ"],
      selectedItem: 1,
      additems: [ ],
    };
  },
  props: ["XM"],
  methods: {
    validate() {
      this.$emit("Input", this.select, this.name);
       (this.select = " "), (this.name = " ");
    },
  },
};
</script>

<style>
</style>
