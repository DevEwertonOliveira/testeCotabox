<template>
    <div>
        <input type="text" v-model="participant.firstName">
        <input type="text" v-model="participant.lastName">
        <input type="text" v-model="participant.participation" >
        <button type="submit" @click="addParticipant">
            Confirmar
        </button>
    </div>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            participant: {
                firstName: "",
                lastName: "",
                participation: ""
            }
        }
    },
    methods:{
        addParticipant(){
            const participant = {...this.participant};
            this.resetParticipant();
            this.$emit("added", participant)
            },
        resetParticipant(){
            this.participant = { 
                firstName: "",
                lastName: "",
                participation: ""
            }
          
        }
    }
}
</script>


<style>
    
</style>