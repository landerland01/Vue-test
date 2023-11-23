
<script>

  
  export default{
    data(){
       return{
         name:"",
         list:[],
     }
   },
  methods:{
    sayHello(){
      // this.list[this.list.length-1]=this.name;
      this.list.push(this.name);
      // alert(this.list[this.list.length-1]);    
      // console.log(this.list);
      // console.log(this.list.length);
      // document.write(1);

    }
  } 
  }
  
</script>

<template>
<!-- 
<h1>Список задач {{ name==''?'____' :name }}</h1>
<p>Тот самый список задач</p>
<input type="text" v-model="name"><br>
<button v-if="name==''" disabled>введите данные</button>
<button v-else @click="sayHello()">кнопка</button> -->


<h1>Список задач {{ name==''?'____' :name }}</h1>
<p>Тот самый список задач</p>
<input type="text" v-model="name"><br>
<button v-if="name==''" disabled>введите задачу</button>
<button v-else @click="sayHello()">добавить в список</button>

<ul>
  <li v-for="item in list">
  {{ 
    item
  }}
  </li>
</ul>




</template>

<style scoped>

.content{
  width: 800px;
  height: 80vh;
  background-color: #fff;
  border-radius: 20px;
  text-align: center;
  margin-top: 50px;
}
.content h1{
  text-transform: uppercase;
  padding-top: 30px;
  padding-bottom: 30px;
  font-size: 40px;
  
}

.content p{
  padding-bottom: 20px;
}

.content input{
  width: 80%;
  height: 40px;
  font-size: 24px;
  margin-top: 30px;
  border: 0;
  border-bottom: 2px solid gray;
  padding: 2px;
}

.content button{
  width: 300px;
  margin-top: 30px;
  font-size: 24px;
  text-transform: uppercase;
  border: 0;
  padding: 4px;
}



</style>
