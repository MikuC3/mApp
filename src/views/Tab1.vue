<template>
  <section>
    <img :src="picture" ><br />
    <h1>ชื่อ-นามสกุล : {{ getFullName }}</h1>
    <h1>อายุ : {{ age }} ปี</h1>
    <h1>ตำแหน่งงาน : นักศึกษา</h1>
    <button @click="toggleVisible">{{ isVisible ? "ซ่อน" : "แสดง"}}รายละเอียด</button>
    <article v-show="isVisible">
      <p>ที่อยู่ : <span v-html="address"></span></p>
      <p>Social : <a :href="social" target="_blank">Facebook</a></p>
      <p v-if="hobby.length === 0">ไม่มีงานอดิเรก</p>
      <div v-else>
        <p>งานอดิเรก :</p>
        <ul>
          <li v-for="(item, index) in hobby" :key="index">{{ item }}</li>
        </ul>
      </div>
      <p>ข้อมูลพื้นฐาน :</p>
      <ul>
        <li v-for="(item, key) in general" :key="key">{{ item }}</li>
      </ul>
    </article>
  </section>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      firstName: "Worachit",
      lastName: "Toto",
      age: 20,
      address: "<i>พิษณุโลก</i>",
      picture:"https://drive.google.com/file/d/1KB-YiGQFY03rwDo_cYV1VS4i2u3ybT3A/view?usp=sharing",
      size: 150,
      social: "https://www.facebook.com/profile.php?id=100007080064703",
      hobby: [
        "เล่นเกม",
        "ดูหนัง",
        "นอน",
        
      ],
      general: { gender: "ชาย", weight: 85, height: 165, status: false },
      isVisible:false,
    };
  },
  methods: {
    toggleVisible(){
        this.isVisible = !this.isVisible
    },
    addSalary(value){
        this.salary+=value
    }
  },
  computed:{
    getFullName() {
        return `${this.firstName}  ${this.lastName}`;
    },
    getIncome(){
        return this.salary * 12;
    },
  }
};
</script>

<style></style>