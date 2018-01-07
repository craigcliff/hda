<template>
<div>

    
  <v-content>
      <v-container fluid fill-height>
        <v-layout justify-center align-center>
        adGroup
          <v-tooltip right>
            <v-btn icon large :href="source" target="_blank" slot="activator">
              <v-icon large>code</v-icon>
            </v-btn>
            <span>Source</span>
          </v-tooltip>
        </v-layout>
      </v-container>
    </v-content>

    
   
   


</div>

</template>


<script>
export default {
  layout: 'default'
}
</script>
