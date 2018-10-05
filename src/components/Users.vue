<template>
    <div id="users">
        <h1>Users:</h1>
        <form v-on:submit="addUser">
            <input type="text" v-model="newUser.name" placeholder="Enter name">
            <br />
            <input type="text" v-model="newUser.email" placeholder="Enter email">
            <br />
            <input type="button" value="Submit">
        </form>        
        <ul>
            <li v-for="user in users">
                {{user.name}}:{{user.email}}
            </li>
        </ul>
    </div>
</template>

<script>

export default {
    name: 'users',
    data() {
        return {
            newUser: {},
            users : [
                {
                    name: 'John Doe',
                    email: 'johndoe@mail.com',
                    contacted: false,

                },
                {
                    name: 'James Smith',
                    email: 'jsmith@mail.com',
                    contacted: false,

                },
                {
                    name: 'Steve Johnson',
                    email: 'sjonhson@mail.com',
                    contacted: false,

                }
            ]
        }
    },
    methods: {
        addUser: function(e){
            console.log('addd user');
            e.preventDefault();
            
            this.users.push({
                name: this.users.name,
                email: this.users.email,
                contacted: false
            })
        }
    }
}
</script>

<style scoped>
#test {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>