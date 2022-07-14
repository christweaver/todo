# todo

//HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ToDo App</title>
   
</head>
<body>
 <h1>My todo list :)</h1>
 <form>
 <div id="container">
     <p>Add to do here</p>
<input type="text" name="" id="inputs">
<button class="submit">Submit</button>
</div>   

<div id="output">
    <div class="posty">
       
     
</div>
</form>

<script src="practice.js"></script>    
</body>
</html>




// SCRIPT

let submitBtn=document.querySelector('.submit')
let post=document.querySelector('.posty')
let input=document.getElementById("inputs")
 

let data=[]
 
let acceptData = () => {
   data.push({Name:'my todo',text:input.value })
 console.log(data)
};


let arrayLoop=()=>{
  for(let i=0; i<data.length; i++){
   let list=document.createElement('li')
   post.appendChild(list)
   let deleteBtn=document.createElement('button')
   deleteBtn.innerHTML='Delete'
    list.innerText=data[i].text
 deleteBtn.setAttribute('id', data[i].id)
  
     
    post.appendChild(deleteBtn)
 console.log(deleteBtn)
   }
    
 }

submitBtn.addEventListener('click', (e) =>{
e.preventDefault()
acceptData()
input.value=''
arrayLoop()

data.forEach((item, index)=>{
  item.id = index+1;
  console.log(item.id)
 
 
});
