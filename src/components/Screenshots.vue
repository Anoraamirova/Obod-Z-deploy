<template>
<div class="screenshots">
<h3 style="margin-bottom:50px" >Qo'llanma</h3>
    <v-sheet
      class="mx-auto"
      elevation="8"
      max-width="800"
      mb-30
    >
      <v-slide-group
        v-model="model"
        class="pa-4"
        show-arrows
      >
        <v-slide-item
      
        >
          <v-img
            :color="active ? 'primary' : 'grey lighten-1'"
            src="@/assets/step_1.png"
            class="ma-4"
            height="400"
            width="205"
      
          >
            <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
             
            </v-row>
          </v-img>
        </v-slide-item>
        <v-slide-item
         
        >
          <v-img
            :color="active ? 'primary' : 'grey lighten-1'"
            src="@/assets/step_2.png"
            class="ma-4"
            height="400"
            width="330"
           
          >
            <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
            
            </v-row>
          </v-img>
        </v-slide-item>
          <v-slide-item
        
        >
          <v-img
            :color="active ? 'primary' : 'grey lighten-1'"
            src="@/assets/step_3.png"
            class="ma-4"
            height="300"
            width="350"
        
          >
            <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
 
            </v-row>
          </v-img>
        </v-slide-item>
      </v-slide-group>
  
      
        <v-sheet
          v-if="model != null"
          height="200"
          tile
          
        >
         
        </v-sheet>
 <v-row
            class="fill-height pa-5"
            align="center"
            justify="center"

          >
            <h4 class="title" style="text-align:left">
            1. Muammoni suratga oling! <br>  2. Rasmga olingan fotoga izoh qoldiring. <br> 3. Natijalarni kuzatib boring
            </h4>
          </v-row>
    </v-sheet>
</div>

</template>

<script>
export default {
data: () => ({
    model: null,
  }),
}
</script>
<style >
.screenshots{
    margin-bottom: 50px;
}
</style>