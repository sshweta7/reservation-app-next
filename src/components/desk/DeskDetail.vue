<template>
<div class="row desk-detail">
  <div class="col-lg-10 bg-white" style="padding: 2%;">
    
      <div class="col-lg-12">
          <div class="col-lg-2">Book a Desk</div>
      </div>

      <div class="row date-time">
          <div class="col-lg-6">    
            <div class="form-group">
              <span>
               <span><i class="far fa-calendar-alt"></i></span>
              
                <date-picker v-model="startdate" :config="options" @dp-change="OnStartDateChange($event)"> 
                  
                </date-picker>
              </span>
              
            </div>
               
          </div>
          <div class="col-lg-6">    
                <date-picker v-model="enddate" :config="options"></date-picker>
          </div>
      </div>

      <div class="row toggle-switch">
          <div class="col-lg-6">        
              <b-input-group>
                <b-input-group-prepend is-text>
                  <b-form-checkbox switch class="mr-n2">
                    <span class="sr-only">Switch for following text input</span>
                  </b-form-checkbox>
                </b-input-group-prepend>
                
              </b-input-group>
          </div>
      </div>

      <div class="row floor-select">
        <div class="col-lg-12"><div class="col-lg-2">Select Floor</div></div>
        <b-dropdown>
          <template #button-content>
            <b-icon icon="calendar-week"></b-icon> <strong>Please choose</strong>
          </template>
          <b-dropdown-item>An item</b-dropdown-item>
          <b-dropdown-item>Another item</b-dropdown-item>
        </b-dropdown>
      </div>

      <div class="row floor-select">
        <div class="col-lg-12"><div class="col-lg-2">Select Amenities</div></div>
        <b-dropdown>
          <template #button-content>
            <b-icon icon="calendar-week"></b-icon> <strong>Please choose</strong>
          </template>
          <b-dropdown-item>An item</b-dropdown-item>
          <b-dropdown-item>Another item</b-dropdown-item>
        </b-dropdown>
      </div>


      <div class="row floor-select">
        <div class="col-lg-6">
            <div class="col-lg-12"><div class="col-lg-12">Select Seat preference</div></div>
            <b-dropdown>
              <template #button-content>
                <b-icon icon="calendar-week"></b-icon> <strong>Please choose</strong>
              </template>
              <b-dropdown-item>An item</b-dropdown-item>
              <b-dropdown-item>Another item</b-dropdown-item>
            </b-dropdown>
        </div>
        <div class="col-lg-6">
            <div class="col-lg-12"><div class="col-lg-12">Available meeting room</div></div>
            <b-dropdown>
              <template #button-content>
                <b-icon icon="calendar-week"></b-icon> <strong>Please choose</strong>
              </template>
              <b-dropdown-item>An item</b-dropdown-item>
              <b-dropdown-item>Another item</b-dropdown-item>
            </b-dropdown>
        </div>
      </div>

  </div>
 
</div>

</template>

<script>
import jQuery from 'jquery'

import datePicker from 'vue-bootstrap-datetimepicker';
import 'pc-bootstrap4-datetimepicker/build/css/bootstrap-datetimepicker.css';

export default {
  name: 'deskdetail',
  components: {
      datePicker
  },
  data () {
    return {
      startdate: new Date(),
      enddate: new Date(),
        options: {
          format: 'DD/MM/YYYY h:mm:ss',
          useCurrent: false,
        }
    } 
  },
  methods: {
    OnStartDateChange(evt) {
      console.log(evt + ":::start date");
    }
  }
}

jQuery.extend(true, jQuery.fn.datetimepicker.defaults, {
  icons: {
    time: 'fas fa-clock',
    date: 'fas fa-calendar',
    up: 'fas fa-arrow-up',
    down: 'fas fa-arrow-down',
    previous: 'fas fa-chevron-left',
    next: 'fas fa-chevron-right',
    today: 'fas fa-calendar-check',
    clear: 'fas fa-trash-alt',
    close: 'fas fa-times-circle'
  }
});
</script>

<style lang="scss">
.desk-detail {
 
  display: flex;
  justify-content: center;
  align-items: center;

  .date-time {
    padding: 10px 0 10px;
  }

  .bg-white {
     background: #fff;
  }

  .floor-select {
    padding: 10px 0 10px;
  }

}
</style>