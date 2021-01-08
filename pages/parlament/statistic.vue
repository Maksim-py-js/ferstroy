<template>
  <div>
   <b-row class="pt-3 align-items-center">
      
      <b-col cols="8">
         <ChartLine />   
      </b-col>

      <b-col cols="4" class="h-100">   
         <div class="my-3 d-flex align-items-center">    
            <ChartDoughnut /> 
            <b>+90% capitalize</b>
         </div>       
         <div class="my-3 d-flex align-items-center">         
            <ChartBarUsers />
            <b>+75% new users</b>
         </div>   
      </b-col>
   </b-row>
   <b-container class="py-4 my-4">
        <b-row>
          <b-col cols="4" class="px-1 d-flex align-items-center text-dark text-decoration-none">
              <div class="rounded-circle bg-secondary p-4 mr-3 text-white font-weight-bold position-relative">
                  <div class="position-absolute" style="top: 50%; left: 50%; transform: translate(-50%, -50%);">
                     897
                  </div>
               </div>
              <div>
                <h6>Buildings</h6>
              </div>
          </b-col>
          <b-col cols="4" class="px-1 d-flex align-items-center text-dark text-decoration-none">
              <div class="rounded-circle bg-primary p-4 mr-3 text-white font-weight-bold position-relative">
                   <div class="position-absolute" style="top: 50%; left: 50%; transform: translate(-50%, -50%);">
                     2.4k
                  </div>
              </div>
              <div>
                <h6>Users</h6>
              </div>
          </b-col>
          <b-col cols="4" class="px-1 d-flex align-items-center text-dark text-decoration-none">
              <div class="rounded-circle bg-primary p-4 mr-3 text-white font-weight-bold position-relative">
                   <div class="position-absolute" style="top: 50%; left: 50%; transform: translate(-50%, -50%);">
                     8m
                  </div>
              </div>
              <div>
                <h6>Capitalize company</h6>
              </div>
          </b-col>
        </b-row>
      </b-container>
  </div>
</template>

<style>
canvas#doughnut-chart {
   width: 100px !important;
   height: 100px !important;
}
</style>

<script>
import ChartBarUsers from "@/components/ChartBarUsers";
import ChartDoughnut from "@/components/ChartDoughnut";

import ChartLine from "@/components/ChartLine";

export default {
  components: {
    ChartBarUsers,
    ChartDoughnut,
    ChartLine
  },
};
</script>