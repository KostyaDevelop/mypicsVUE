<template>
  <div class="page">
    <meta name="csrf-token" content="sxRh3Iw42mpXPetex3zkJpykGvFFhvbTSZkPk3Qy">
    <div class="content">
      <div class="container">
        <Header />
        <div class="row">
           <div  class="col-lg-3 col-md-3 col-sm-3">
             <InfoAcc />
           </div>
          <div  class="col-lg-9 col-md-9 col-sm-9">
            <PhotoList />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>

import axios from 'axios'
import PhotoList from '@/components/PhotoList'
import Header from '@/components/Header'
import InfoAcc from '@/components/InfoAcc'

export default {
  name: 'StartPage',
  mounted () {
    axios
      .get('http://mypics.localhost/idd1')
      .then(response => (this.info = response))
  },
  components: {
    PhotoList,
    Header,
    InfoAcc
  }
}
</script>

<style scoped>
  .content{
    width: 100%;
    margin: 0 auto 30px;
    max-width: 935px;
  }
  /*.page{*/
  /*  background: #E9A887;*/
  /*}*/
</style>
