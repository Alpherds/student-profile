<template>
    <v-app>
        <v-main>
            <v-container>
                <v-row>
                    <v-col
                        cols="12"
                        md="12"
                    >
                        <v-text-field
                        label="Student No."
                        prepend-inner-icon="mdi-numeric"
                        variant="outlined"
                        ></v-text-field>
                    </v-col>

                    <v-col
                       cols="12"
                       md="4"   
                    >
                        <v-text-field
                        label="Last Name "
                        prepend-inner-icon="mdi-account-box-outline"
                        variant="outlined"
                        ></v-text-field>
                    </v-col>

                    <v-col
                       cols="12"
                       md="4"   
                    >
                        <v-text-field
                        label="First Name "
                        prepend-inner-icon="mdi-account-box-outline"
                        variant="outlined"
                        ></v-text-field>
                    </v-col>

                    <v-col
                       cols="12"
                       md="4"   
                    >
                        <v-text-field
                        label="Middle Name "
                        prepend-inner-icon="mdi-account-box-outline"
                        variant="outlined"
                        ></v-text-field>
                    </v-col>

                    <v-col
                       cols="12"
                       md="4" 
                    >
                        <v-combobox
                        label="Course"
                         prepend-inner-icon="mdi-account-details-outline"
                        :items="['BSCS', 'DCT']"
                        variant="outlined"
                        ></v-combobox>
                    </v-col>

                     <v-col
                       cols="12"
                       md="4" 
                    >
                        <v-combobox
                        label="Year"
                         prepend-inner-icon="mdi-account-details-outline"
                        :items="['1st year', '2nd year', '3rd year', '4th year']"
                        variant="outlined"
                        ></v-combobox>
                    </v-col>

                     <v-col
                       cols="12"
                       md="4" 
                    >
                        <v-combobox
                        label="Section"
                         prepend-inner-icon="mdi-account-details-outline"
                        :items="['A', 'B' , 'C' , 'D']"
                        variant="outlined"
                        ></v-combobox>
                    </v-col>

                     <v-col
                       cols="12"
                       md="4"   
                    >
                        <v-text-field
                        label="Address "
                        prepend-inner-icon="mdi-card-account-details-outline"
                        variant="outlined"
                        ></v-text-field>
                    </v-col>

                     <v-col
                       cols="12"
                       md="4"   
                    >
                        <v-text-field
                        label="Contact No "
                        prepend-inner-icon=" mdi-card-account-phone-outline"
                        variant="outlined"
                        ></v-text-field>
                    </v-col>

                     <v-col
                       cols="12"
                       md="4" 
                    >
                        <v-combobox
                        label="Gender"
                         prepend-inner-icon="mdi-gender-transgender"
                        :items="['Male', 'Female' , 'LGBTQ']"
                        variant="outlined"
                        ></v-combobox>
                    </v-col>
                    
                </v-row>

                        <v-btn
                        color="green"
                        size="small"
                        variant="outlined"
                        >
                            Save
                        </v-btn>

                         <v-btn
                        color="blue"
                        size="small"
                        variant="outlined"
                        >
                            Edit
                        </v-btn>

                        <v-btn
                        color="orange"
                        size="small"
                        variant="outlined"
                        >
                            Update
                        </v-btn>

                         <v-btn
                        color="red"
                        size="small"
                        variant="outlined"
                        >
                            Delete
                        </v-btn>

                         <v-card
                            title="Student Profile"
                            flat
                        >
                              <v-text-field
                                v-model="hanapstudent"
                                label="Search"
                                prepend-inner-icon="mdi-magnify"
                                variant="outlined"
                                hide-details
                                single-line
                            ></v-text-field>

                             <v-data-table
                                :headers="titlecolumn"
                                :items="nilalamanngcolumn"
                                :search="hanapstudent"
                            ></v-data-table>
                        </v-card>
            </v-container>
        </v-main>
    </v-app>
</template>


<script setup>

  const hanapstudent = ref('')

    const titlecolumn = [
        {
            key: 'studno', title: 'Student Number' 
        },
        {
            key: 'lname', title: 'Last Name' 
        },
            {
            key: 'fname', title: 'First Name' 
        },
        {
            key: 'mname', title: 'Middle Name' 
        },
            {
            key: 'ylevel', title: 'Year Level' 
        },
        {
            key: 'csection', title: 'Section' 
        },

    ]

    const nilalamanngcolumn = [
        {
            studno: 1400031,
            lname:'Dizon',
            fname:'Alpher',
            mname:'San Juan',
            ylevel:'1st year',
            csection:'A',
        },
         {
            studno: 1400032,
            lname:'Rizal',
            fname:'Jose',
            mname:'Santos',
            ylevel:'2nd year',
            csection:'A',
        },
    ]
</script>

