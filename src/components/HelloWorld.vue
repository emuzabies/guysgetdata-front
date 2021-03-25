<template>
<div class="guys">
  <div class="mb-2">
    <b-card border-variant="secondary" text-variant="dark" header="ต้า Database" class="text-center">
        <b-card-text>ทำได้แค่นี้หรอวะ เว็บเก็บข้อมูลมึงอ่ะ</b-card-text>
      </b-card>
  </div>
  <div class="mb-2">
      <b-card border-variant="info" text-variant="dark" header="บอม Full-stack Dev" class="text-center">
        <b-card-text>เออ อยากสวยมึงก็ทำสิ</b-card-text>
      </b-card>
  </div>
  <div class="mb-3">
      <b-card border-variant="secondary" text-variant="dark" header="ต้า Database" class="text-center ">
        <b-card-text>เหอะ ๆ ไม่อ่ะขี้เกียจ มึงทำอ่ะดีและ</b-card-text>
      </b-card>
  </div>
      <b-card bg-variant="dark" text-variant="white" title="แย่แล้ว" header-tag="header" footer-tag="footer">
      <template #header>
        <h4 class="mb-0">ต้องการความช่วยเหลือ</h4>
      </template>
      <b-card-text >พวกเราทีมพัฒนา GUYs monitoring ขี้เกียจกรอกข้อมูลลงฐานข้อมูล ขอให้เพื่อน ๆ ช่วยกันกรอกข้อมูลหน่อยครับ <br> - GUYs Devepoler Team -</b-card-text>
      <b-button to="/form" variant="primary">พร้อมแล้วลุยเลย</b-button>
      <template #footer>
        <em>*นี่ไม่ใช้โฆษณาเว็บพนันหรืออะไรแต่ต้องการข้อมูลจริง ๆ นะเอาไปโปรเจ็คง่ะ* <br>แต่ถ้าต้องการลงโฆษณาติดต่อ 094-154-1494  คุณกาย CEO</em>
      </template>
    </b-card>
    <div class="mt-3">
      <b-card border-variant="secondary" text-variant="dark" header="พื้นที่ใส่โฆษณา" class="text-center ">
        <b-card-text>ตรงที่ว่างขาว ๆ ใส่โฆษณาได้นะงับ ราคาไม่แพง ยิงhostแล้ว มาหารายได้กัน</b-card-text>
      </b-card>
  </div>
</div>
</template>

<script>
export default {
  name: 'HelloWorld'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.guys{
  text-align: center;
}

</style>
