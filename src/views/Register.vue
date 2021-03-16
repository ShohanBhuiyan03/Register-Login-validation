<template>
    <div class="container">
    <h1>Register to NEU Twitter</h1>
    <br>
    <br>
    <div class="row">
        <div class="col-md-3"></div>
        <div class="col-md-6">
            <form>
                <div class="mb-3">
                    <input type="text" 
                    class="form-control" 
                    id="fullName" 
                    required
                    placeholder="Full Name">
                </div>
                <div class="mb-3">
                    <input type="email" 
                    class="form-control" 
                    id="email"
                    v-model="email"
                    required
                    placeholder="Enter Email">
                </div>
                <div class="mb-3">
                    <input type="password" 
                    class="form-control" 
                    id="password"
                    v-model="password"
                    required
                    placeholder="Enter Password"/>
                    <div v-if="password.length>1 && password.length<6" 
                    class="text-danger">Password lenght should be greater than 6 character</div>
                </div>
                <div class="mb-3">
                    <input type="password" 
                    class="form-control" 
                    id="reenterPassword"
                    v-model="reenterPassword"
                    required
                    placeholder="Confirm Password"/>
                    <div v-if="password != reenterPassword" 
                    class="text-danger">Password don't match</div>
                </div>
                <button type="submit" class="btn btn-primary">SignUp</button>
            </form>
        </div>
        <div class="col-md-3"></div>
    </div>
</div>
</template>

<script>
    export default {
        name: "register",
    data() {
        return {
            email: "",
            password: "",
            reenterPassword: ""
        }
    },
    methods: {
        login: function() {
            console.log ("Email: " + this.email);
           
            
        },
    },

}    
</script>

<style lang="scss" scoped>

</style>