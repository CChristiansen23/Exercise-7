<template>
    <div class="container">
        <form>
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <!-- Part 1 5 Points-->
                    <!-- Create a Signup Form where you retrieve the following Information -->
                    <!-- Full Name (First Name + Last Name) -->
                    <!-- Mail -->
                    <!-- Password -->
                    <!-- Store Data? Yes/No -->
                    <div class="form-group">
                        <label for="name">First & Last Name</label>
                        <input type="text" id="name" class="form-control" v-model="userData.name">
                    </div>

                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="text" id="email" class="form-control" v-model="userData.email">
                    </div>

                    <div class="form-group">
                        <label for="password">Password</label>
                        <input type="password" id="password" class="form-control" v-model="userData.password">
                    </div>

                    <div>
                        <label for="password">Store Data?</label>

                        <app-OnOff v-model="dataSwitch"></app-OnOff>
                    </div>

                    <div>
                        <button class="btn btn-primary" @click.prevent="submitted">
                            Submit!
                        </button>
                    </div>


                    <!-- Part 2 5 Points -->
                    <!-- Only display the Form if it has NOT been submitted -->
                    <!-- Display the Data Summary ONCE the Form HAS been submitted -->


                    <!-- Part 3 5 Points -->
                    <!-- Edit the Example from above and create a custom "Full Name" Control -->
                    <!-- which still holds the First Name and Last Name Input Field -->
                </div>
            </div>
        </form>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <div class="panel panel-default">
                    <div class="panel-heading">
                        <h4>Your Data</h4>
                    </div>
                    <div class="panel-body">
                        <p>First & Last Name: {{userData.name}}</p>
                        <p>Full Name: {{userData.name}}</p>
                        <p>Mail: {{userData.email}}</p>
                        <p>Password: {{userData.password}}</p>
                        <p>Store in Database?: {{dataSwitch}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import OnOff from './OnOff.vue'
    export default {
        data(){
            return {
                userData: {
                    name: '',
                    email: '',
                    password: ''
                },
                dataSwitch: true,
                show: false
            }
        },
        methods: {
            submitted() {
                this.show = true
            }
        },
        components: {
            appOnOff : OnOff
        }
    }
</script>

<style>
</style>
