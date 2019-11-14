<template>
<div>
    <button id="classButton" v-on:click="getMyClass()">Vis/Fjern Klasseliste</button>
    <center>
    <table>
        <thead>
        <th>Fornavn</th>
        <th>Etternavn</th>
        <th>Klasse</th>
        </thead>

        <tbody>
            <tr v-for="person in persons" :key="person.id">
                <td>{{person.firstName}}</td>
                <td>{{person.lastName}}</td>
                <td>{{person.myClass}}</td>
            </tr>    
        </tbody>
    </table>
    </center>
    </div>
</template>

<script>
import mockData from '../mock-data/min-klasse.json'

export default {
    name: 'table',

    data(){
        return{
            persons: []
        }
    }, 

    methods: {

        //butttonAction(){

          //  state == 1;

            //if (state == 1){
              //  getMyClass();
                //state == 0;
            //}

            //else{
              //  remMyClass();
                //state == 1;
            //}
        //},

        getMyClass(){
            this.persons = mockData;
        },

        remMyClass(){
            this.persons = [];
        }
    }
}

</script>

<style>
    table{
        width: 90%;
        
        text-align: center;
        border-collapse: collapse;
    }

    th{
        background-color: #cf2115;
        color: white;

        width: 33.3%;
        padding: 8px;

        border: 1px solid black
    }

    tr:nth-child(even){
        background-color: #e8e8e8;
    }

    td{
        color: #000000;
        padding-top: 10px;
        padding-bottom: 10px;

        border: 1px solid #000000;
    }

    #classButton{
        margin: 10px;
    }

</style>
