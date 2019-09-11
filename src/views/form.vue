<template>
    <div class="mt-5">

        <h1>Formularios</h1>
        <form>
            <b-row>
            <b-col md="3">
            <b-form-input type="text" v-model="texto" :state="comprobar"></b-form-input>
            <small>minimo 3 caracteres</small>
            </b-col>

                        <b-col md="3">
                <b-form-select v-model="animal" :options="animales">

                </b-form-select>
                <p>Seleccion : {{animal}}</p>
            </b-col>

            
                        <b-col md="3">
                <b-form-radio-group v-model="animalRadio" :options="animalesRadio">

                </b-form-radio-group>
                <p>Seleccion : {{animalRadio}}</p>
            </b-col>

            <b-col md="3">
                <b-form-checkbox-group v-model="animalCheck" :options="animalesCheck">

                </b-form-checkbox-group>
                <p>Seleccion : {{animalCheck}}</p>
            </b-col>
            </b-row>
        </form>
        <p>texto : {{texto}}</p>
    </div>
</template>

<script>
    export default {
        name:'Grid',
        data(){
            return{
                texto:'',
                select:null,
                animales: [{value:null,text:"Seleccione un animal"},
                {value:1,text:"Perro"},
                {value:2,text:"Gato"},
                {value:3,text:"Zorro"}],
                                animalesRadio: [,
                {value:1,text:"Perro"},
                {value:2,text:"Gato"},
                {value:3,text:"Zorro"}],
                animalesCheck: [,
                {value:1,text:"Perro"},
                {value:2,text:"Gato"},
                {value:3,text:"Zorro"}],
                animal : null,
                animalRadio : null,
                animalCheck: null
            }

        },
        computed:{
        comprobar(){
            return this.texto.length>2 ? true :  false ;
        }
        }
    }
</script>