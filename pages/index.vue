<template>
  <div>
  
    <v-container>
      <v-content>
  
  
        <h1 class="text-xs-center mt-2 pt-2">Create New User </h1>
        <form>
          <v-layout justify-center mt-3 pt-3>
  
            <v-card width=600>
              <v-card-text>
                <v-layout row wrap>
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="FirstName " v-model="un.firstname" label="First Name" hint="Please insert Name"></v-text-field>
                  </v-flex>
  
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Surname" v-model="un.lastname" label="Surname"></v-text-field>
                  </v-flex>
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Username" v-model="un.username" label="Username"></v-text-field>
                  </v-flex>

                   <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Company" v-model="un.company" label="Company"></v-text-field>
                  </v-flex>

                  
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Department" v-model="un.department" label="Department"></v-text-field>
                  </v-flex>
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Job" v-model="un.job" label="Job"></v-text-field>
                  </v-flex>

                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Description" v-model="un.description" label="Description"></v-text-field>
                  </v-flex>
                 
  
   <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Office" v-model="un.office" label="Office"></v-text-field>
                  </v-flex>
                  <v-flex xs12 sm6 pr-5>
                     <v-select v-bind:items="results" v-model="a1" label="Manager" autocomplete></v-select>
                  </v-flex>


                  
  
  
      <!--            <v-flex xs12 sm6 pr-5>
                    <v-select v-bind:items="items" v-model="e1" label="Select" dark item-value="text"></v-select>
                  </v-flex>
  
                  <v-flex xs12 sm6 pr-5>
                    <v-text-field name="Location" label="Location"></v-text-field>
                  </v-flex>
  
                  <v-flex xs12 sm6 pr-5>
                    <v-select v-bind:items="states" v-model="a1" label="Select" autocomplete></v-select>
                  </v-flex> -->


                  
                </v-layout>
                <v-btn @click.prevent="addUser">submit</v-btn>
                  <v-btn @click="clear">clear</v-btn>
              </v-card-text>
            </v-card>
          </v-layout>
  
        </form>
  
      </v-content>
  
  
    </v-container>
  
  
  
  </div>
</template>


<script>

import axios from 'Axios'


  export default {
    layout: 'default',
    data() {
      return {
        results: [],
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
        ],

         un: {
        value: '',
        rawValue: '',
        firstname: '',
      lastname:'',
      username:'',
    //  selected: 'Permanent',
      date:'',
      company:'',
      job:'',
      title:'',
      description:'',
      department:'',
      office:'',
      manager:'',
      picked:'One',
      man:'',
      dspl: true,
      seen:true
      }
  
      }
    },

     mounted() {
    axios.get("http://localhost:3000/api/adUsers")
    .then(response => {this.results = response.data;
    console.log(this.results);
    
    
    })

    
  },

    methods: {

       addUser() {





           axios.post('http://dst00649:3000/api/adUsers', {"username": this.un.username,
   "company": this.un.company,
   "firstName": this.un.firstname,
   "lastName": this.un.lastname,
   "department": this.un.department,
   "description": this.un.description,
   "office": this.un.office,
   "manager": this.un.manager,
   "job": this.un.job}

).then(
  (response) => {
      console.log(response)
  



   })
   .catch(error => {
 console.log(error.response)
 


    
   });




  }




    }
  
  }
</script>


