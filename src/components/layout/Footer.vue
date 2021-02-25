<template>
  <div class="row custom-footer">
    <div class="col-lg-10">
      <div class="row">
        <div class="col-lg-12">
          <div class="row">
            <div class="col-lg-2">       
            </div>
            <div class="col-lg-8">
              <h2>{{ text }}</h2>
            </div>
            <div class="col-lg-2">              
            </div>
          </div>
        </div>  
      </div>
    </div>
    
     
  </div>
</template>

<script>
export default {
  name: 'customfooter',
  data () {
    return {
      text: 'Confirm Booking'
    }
  }
}
</script>

<style lang="scss">
.custom-footer {
  height: 5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
}
</style>