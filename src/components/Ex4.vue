<script>
    export default { 
        data() {
            return {
                // Add code here
                id: "demo1",
                blueBoth: true
            }
        },
        methods: { 
   			// Add code here
            changeColor(){
                this.blueBoth = !this.blueBoth
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div :id="id" :class="{'blueBox': blueBoth, 'redBox': !blueBoth}" class="m-2">
            div ID : {{id}} 
        </div>
        
        <button type="button" :class="{'btn btn-primary': blueBoth, 'btn btn-danger': !blueBoth}" @click="changeColor()">Change Color</button>
        
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
