<template>
  <div>
  Time now:
  <br/>
  <span>{{ time }}</span>
  </div>
</template>
<script>
import moment from 'moment';

const timeVue = {
  data() {
    return {    
      time: ''
    };
  },
  mounted: function(){
      const  self = this;
      setInterval(() => {
          const dateNow = new Date(Date.now());
          self.time = moment(dateNow).format('MMMM Do YYYY, h:mm:ss a');
      }, 1000);
  }
};

export default timeVue;
</script>
