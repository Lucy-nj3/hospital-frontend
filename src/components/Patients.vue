<script setup>
import { ref } from 'vue'

const patients=[
{
    id:1,
    firstName:"John",
    lastName:"Doe",
    email:"johndoe@example.com",
    phone:"0708123222",
    residence:"123,Main Street",
    nationalId:"123456",
    dob:"2000-04-03"
},
{
    id:2,
    firstName:"Kim",
    lastName:"Kings",
    email:"kimkings@example.com",
    phone:"0734524313",
    residence:"140, Main Street",
    nationalId:"123456",
    dob:"1998-04-03"
},
{
    id:3,
    firstName:"Joseph",
    lastName:"Dan",
    email:"josephdan@example.com",
    phone:"079834341",
    residence:"142,Main Street",
    nationalId:"123456",
    dob:"1995-04-03"
},
{
    id:4,
    firstName:"Joy",
    lastName:"kim",
    email:"joykim@example.com",
    phone:"0702134222",
    residence:"132,Main Street",
    nationalId:"124356",
    dob:"1978-04-03"
},
{
    id:5,
    firstName:" James",
    lastName:"Jack",
    email:"jamesjack@example.com",
    phone:"0706145222",
    residence:"1292,Main Street",
    nationalId:"125656",
    dob:"2006-04-03"
}


]

const showAddDialog = ref(false)

//models
const firstName =ref(null)
const lastName =ref(null)
const email =ref(null)
const phone =ref(null)
const residence =ref(null)
const nationalId =ref(null)
const dob=ref(null)

function handleAddPatient(){
    const data ={
        id:5,
        firstName:firstName.value,
        lastName:lastName.value,
        email:email.value,
        phone:phone.value,
        residence:residence.value,
        nationalId:nationalId.value,
        dob:dob.value,

    } 
    patients.push(data)
    showAddDialog.value =false
    console.log(patients)
}

</script>

<template>
    <v-container class="mt-6">
        <v-row>
            <v-col md="10">
                <h1>patients</h1>
            </v-col>
            <v-col md="2">
                <v-btn class="ma-2" color="primary" icon="mdi-plus" @click="showAddDialog = true"></v-btn>
            </v-col>
        </v-row>

        <v-row>
            <v-col>
                <v-table class="border" stripped="even">
                    <thead>
                        <tr>
                        <th>Name</th>
                        <th>Phone</th>
                        <th>Email</th>
                        <th>Residence</th>
                        <th>National ID</th>
                        <th>Date of Birth</th>
                        <th>Action</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="item in patients">
                            <td>{{ item.firstName+" "+item.lastName }}</td>
                            <td>{{ item.phone }}</td>
                            <td>{{ item.email }}</td>
                            <td>{{ item.residence }}</td>
                            <td>{{ item.nationalId }}</td>
                            <td>{{ item.dob }}</td>
                            <td>
                                <v-btn color="primary" size="small" to="/viewpatient">
                                    <v-icon icon="mdi-eye"></v-icon>
                                    View
                                </v-btn>
                            </td>
                        </tr>
                    </tbody>
                </v-table>
            </v-col>
        </v-row>
    </v-container>
<!-- Add Patient -->
<v-dialog v-model="showAddDialog" max-width="50%">
    <v-form>
        <v-card class="pa-4">
            <v-row>
                <v-card-text>Add patient</v-card-text>
                <v-spacer></v-spacer>
                <v-btn class="ma-2" color="secondary" icon="mdi-close" @click="showAddDialog = false"></v-btn>
            </v-row>
            <v-divider class="mb-4" color="primary" opacity=".7" thickness="3" gradient></v-divider>
            <v-row>
                <v-col md="6">
                    <v-text-field label="First Name" v-model="firstName" variant="outlined"prepend-icon="mdi-account-outline"></v-text-field>
                </v-col>
                <v-col md="6">
                    <v-text-field label="Last Name" v-model="lastName" variant="outlined" prepend-icon="mdi-account-outline"></v-text-field>
                </v-col>
            </v-row>
            <v-row>
                <v-col md="6">
                    <v-text-field label="Email" v-model="email"variant="outlined"prepend-icon="mdi-email-outline"></v-text-field>
                </v-col>
                <v-col md="6">
                    <v-text-field label="Phone" v-model= "phone"variant= "outlined"prepend-icon="mdi-phone-outline"></v-text-field>
                </v-col>
            </v-row>
            <v-row>
                <v-col md="6">
                    <v-text-field label="Residence" v-model="residence" variant="outlined"prepend-icon="mdi-home-outline"></v-text-field>
                </v-col>
                <v-col md="6">
                    <v-text-field label="National ID" v-model="nationalId" variant="outlined"prepend-icon="mdi-account-outline"></v-text-field>
                </v-col>
            </v-row>
            <v-row>
                <v-col md="6">
                    <v-date-input label="Date of Birth" v-model="dob" variant="outlined"prepend-icon="mdi-calendar-outline"></v-date-input>
                </v-col>
            </v-row>
            <v-divider class="mb-4" color="primary" opacity=".7" thickness="3" gradient></v-divider>
            <v-row>
                <v-col>
                    <v-card-actions>
                        <v-btn color="primary"variant="outlined">
                            <v-icon icon="mdi-close"></v-icon>
                            Close</v-btn>
                        <v-spacer/>
                        <v-btn color="primary" variant="outlined"@click="handleAddPatient">
                        <v-icon icon="mdi-content-save-outline"></v-icon>
                        Save </v-btn>
                    </v-card-actions>
                </v-col>
            </v-row>
        </v-card>
    </v-form>
</v-dialog>
    </template>