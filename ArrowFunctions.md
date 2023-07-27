## ES6 Arrow functions.

* **Normal javascript function to get square.**
<pre class="notranslate">
<code>
const square=function(x){
    return x*x
}
console.log(square(5));
</code>
</pre>

* **Arrow function for square.**
<pre class="notranslate">
<code>
const square=(x)=>{
    return x*x;
}
console.log(square(5));

--> If our function will have single statement and return a value. It can also be written as below.
  
const square=(x) => x*x;
console.log(square);
</code>
</pre>

* **Creating a javascript object and converting into arrow function**
<pre class="notranslate">
<code>
const event={
  name:'Birthday party'
  printGuestList:function(){
  console.log('Guest list for '+this.name);
  }
}
event.printGuestList()// calling the guestlist it will print : Guest list for Birthday party.
</code>
</pre>

* **Below is arrow function of above**
<pre class="notranslate">
<code>
const event={
  name:'Birthday party'
  printGuestList:()=>{
  console.log('Gues list for '+this.name);
  }
}
event.printGuestList()// out put: Guest list for **undefined**..
</code>
</pre>
Note: We are getting undefined because array function do not bind to there own this value.

* **There is a alternate way to write it in arrow function and this will bind.**
<pre class="notranslate">
<code>
const event={
  name:'Birthday party',
  printGuestList(){
  console.log('Gues list for '+this.name);
  }
}
event.printGuestList()// output: Guest list for Birthday party
</code>
</pre>

* **More demontration on arrow function and this.**
<pre class="notranslate">
<code>
const event = {
    name: 'Birthday Party',
    guestList: ['Andrew', 'Jen', 'Mike'],
    printGuestList() 
      {
        console.log('Guest list for ' + this.name);
  
        // this.guestList.forEach(function(guest) {
        //     console.log(guest + ' is attending ' + this.name)
        // }) this will not work as "this" will be binding to local function and looking for name inside foreach and  name is not defined inside foreach loop   
   
        this.guestList.forEach((guest)=> {
            console.log(guest + ' is attending ' + this.name)
        }); //this will work here "forEach((guest)=>" is used as arrow function and in arrow function "this" is not binded.
      }
  }
event.printGuestList();
</code>
</pre>
  
  
