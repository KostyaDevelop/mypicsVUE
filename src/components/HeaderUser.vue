<template>
  <div class="add-photo">
    <div class="add-photo-icon">
      <img src="../assets/img/addPhoto.svg">
    </div>
  </div>
</template>

<script>
export default {
  name: 'AddPhoto'
}
</script>

<style scoped>
  .add-photo-icon{
    display: flex;
    justify-content: flex-end;
  }
  .add-photo-icon img{
    width: 25px;
    height: 25px;
    cursor: pointer;
  }
</style>
