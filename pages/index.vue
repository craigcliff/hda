<template>
  <div>
  
    <v-container>
      <v-content>
  
  
        <h1 class="text-xs-center mt-2 pt-2">Create New User </h1>
        <form>
          <v-layout justify-center mt-5 pt-5>
  
            <v-card width=600>
              <v-card-text>
                <v-layout row wrap>
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Name " label="Name" hint="Please insert Name"></v-text-field>
                  </v-flex>
  
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Surname" label="Surname"></v-text-field>
                  </v-flex>
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Username" label="Username"></v-text-field>
                  </v-flex>
  
  
                  <v-flex xs12 sm6 pr-5>
                    <v-select v-bind:items="items" v-model="e1" label="Select" dark item-value="text"></v-select>
                  </v-flex>
  
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Location" label="Location"></v-text-field>
                  </v-flex>
  
                  <v-flex xs12 sm6 pr-5>
                    <v-select v-bind:items="states" v-model="a1" label="Select" autocomplete></v-select>
                  </v-flex>
                  <v-btn @click="submit">submit</v-btn>
                  <v-btn @click="clear">clear</v-btn>
                </v-layout>
              </v-card-text>
            </v-card>
          </v-layout>
  
        </form>
  
      </v-content>
  
  
    </v-container>
  
  
  
  </div>
</template>


<script>
  export default {
    layout: 'default',
    data() {
      return {
        e1: null,
        e2: null,
        e3: null,
        e4: null,
        items: [{
            text: 'State 1'
          },
          {
            text: 'State 2'
          },
          {
            text: 'State 3'
          },
          {
            text: 'State 4'
          },
          {
            text: 'State 5'
          },
          {
            text: 'State 6'
          },
          {
            text: 'State 7'
          }
        ],
  
        a1: null,
        states: [
          "Alabama",
          "Alaska",
          "American Samoa",
          "Arizona",
          "Arkansas",
          "California",
          "Colorado",
          "Connecticut",
          "Delaware",
          "District of Columbia",
          "Federated States of Micronesia",
          "Florida",
          "Georgia",
          "Guam",
          "Hawaii",
          "Idaho",
          "Illinois",
          "Indiana",
          "Iowa",
          "Kansas",
          "Kentucky",
          "Louisiana",
          "Maine",
          "Marshall Islands",
          "Maryland",
          "Massachusetts",
          "Michigan",
          "Minnesota",
          "Mississippi",
          "Missouri",
          "Montana",
          "Nebraska",
          "Nevada",
          "New Hampshire",
          "New Jersey",
          "New Mexico",
          "New York",
          "North Carolina",
          "North Dakota",
          "Northern Mariana Islands",
          "Ohio",
          "Oklahoma",
          "Oregon",
          "Palau",
          "Pennsylvania",
          "Puerto Rico",
          "Rhode Island",
          "South Carolina",
          "South Dakota",
          "Tennessee",
          "Texas",
          "Utah",
          "Vermont",
          "Virgin Island",
          "Virginia",
          "Washington",
          "West Virginia",
          "Wisconsin",
          "Wyoming"
        ]
  
      }
    }
  
  }
</script>


