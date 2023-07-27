## Javascript Object Conversion.

**Below is JavaScript Object** 
<pre class="notranslate">
<code>
const book= {
    name:'Ego is enemy',
    author: 'Ryan holiday'
}
</code>
</pre>

* **JSON.stringify() can be used to convert the javascript object to JSON.**
<pre class="notranslate">
<code>
const bookJson=JSON.stringify(book);
console.log(bookJson);// Result --> {"name":"Ego is enemy","author":"Ryan holiday"}
</code>
</pre>

*  **When we try to get the attribute of json object like below it will give undefined.**
<pre class="notranslate">
<code>
console.log("Second Result: "+ bookJson.name); //undefined
  
//but the javascript object attributes can be accessed like below.
console.log("Third Result: "+ book.name); //Ego is enemy
</code>
</pre>

* **JSON.parse -To convert the JSON back to javascript object**
<pre class="notranslate">
<code>
const parseData=JSON.parse(bookJson)
console.log(parseData) //Result --> { name: 'Ego is enemy', author: 'Ryan holiday' }
</code>
</pre>
