<script>
    export default { 
        data() {
            return {
                // Add code here
                id : "demo1",
                divColor : "blue",
                btnColor : "btn-primary"
            }
        },
        methods: { 
   			// Add code here
            changeColor() {
                if (this.divColor == 'blue'){
                    this.divColor = "red", 
                    this.btnColor = "btn-danger"
                }
                else {
                    this.divColor = "blue",
                    this.btnColor = "btn-primary"
                }
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" :style="{'background-color': divColor}" class="m-2">
            div ID : {{id}} 
        </div>
        
        <button v-on:click="changeColor" :class="btnColor" class="btn" type="button">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
