<template>
  <div class="row custom-header">
    <div class="col-lg-10">
      <div class="row">
        <div class="col-lg-12">
          <div class="row">
            <div class="col-lg-2">
                <b-icon icon="bar-chart-steps"></b-icon>
            </div>
            <div class="col-lg-8">
              <h2>{{ location }}</h2>
            </div>
            <div class="col-lg-2">
              <b-icon icon="pencil"></b-icon>
            </div>
          </div>
        </div>  
      </div>
    </div>      
  </div>
</template>

<script>
export default {
  name: 'customheader',
  data () {
    return {
      location: 'Selected location'
    }
  }
}
</script>

<style lang="scss">
.custom-header {
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