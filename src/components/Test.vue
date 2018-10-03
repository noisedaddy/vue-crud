<template>
    <div id="test">
        <input type="text" v-model="title">
        <h1>{{ title }}</h1>
        <p>{{user.first_name}}</p>        
        <p v-if="show">{{user.last_name}}</p>
        <p v-else>NoBOdy</p>
        <ul>
            <li v-for="item in items">{{ item.title }}</li>
        </ul>
        <button v-on:click="greet('hello world local arg')">Say Greet</button>  
        </br>      
        <input type="text" v-on:keyup="pressKey" v-on:keyup.enter="pressEnter"/>
        </br>
        <label>First Name:</label><input type="text" v-model="user.first_name"> 
        </br>
        <label>Last Name:</label><input type="text" v-model="user.last_name">
        </br>
        <h3>{{fullName}}</h3>
    </div>
</template>

<script>

export default {
    name: 'test',
    data() {
        return {
            title: 'Hello World',
            user: {
                first_name: 'John',
                last_name: 'Doe'
            },
            show:true,
            items: [
                {title: 'Item One'},
                {title: 'Item Two'},
                {title: 'Item Three'},
            ]
        }
    },
    methods: {
        greet: function(greeting){
            alert(greeting);
        },
        pressKey: function(e){
            alert(e.target.value);
        },
        pressEnter: function(){
            alert('press Enter');
        }
    },
    computed: {//Computed properties
        fullName: function(){
            return this.user.first_name+" "+this.user.last_name;
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