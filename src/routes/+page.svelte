 <script>
let Punchline='';
let type='';
let Setup='';
let text='Click Button To Show Random Jokes !'
function Jokes() {
     const getRandomUser = async () => {
         var response = await fetch('https://official-joke-api.appspot.com/random_joke');
         var result = await response.json();
         console.log(result)
         console.log(result.type)
         type=result.type
         Setup=result.setup
         Punchline=result.punchline;
         
         return result;
     }
     
     let userPromise = getRandomUser();
 }   
 

</script>
 



<h1 id="title"> Random Jokes</h1>
<div class="main">
    <div id='spann'>
    Type: 
    <span >{type}</span>
    </div>

    <div class="divsetup">
        Person 1 <br>{@html Setup}
    </div>

    <div class="p2">Person 2 <br>{Punchline}</div>


    <button class="btn" on:click={Jokes}>Random Jokes</button>
    <div class="text">{text}</div>
</div>


<style>
    .text{
        color: red;
        filter:drop-shadow(10px 10px 10px red) ;
        margin-top: 3%;
    }
    .btn{
        height: 60px;
        width:200px;
        background-color: blue;
        color: white;
        margin-top: 8%;

    }
.p2{
    margin-top: 5%;
    height: 80px;
    width: 100%;
    background-color: rgba(11, 8, 78, 0.854);
    filter: drop-shadow(5px 10px 5px blue);
}

.divsetup{
    margin-top: 5%;
    height: 80px;
    width: 100%;
    background-color: rgba(11, 8, 78, 0.854);
    filter: drop-shadow(5px 10px 5px blue);
}

#spann{
    height: 50px;
    width: 100%;
    background-color: rgba(11, 8, 78, 0.854);
    filter: drop-shadow(5px 10px 5px blue);

}
.main{
    margin-top: 5%;
        height: 550px;
        width: 600px;
        margin-left: 30%;
        color: white;
        font-size: 24px;
        text-align: center;
    }
 #title{
        text-align: center;
        padding-top: 3%;
        color: white;
        filter: drop-shadow(5px 10px 6px blue);
    }


</style> 























