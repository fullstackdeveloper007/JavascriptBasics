## Write a method TaskToDo inside tasks Javascript object to get incomplete tasks.


<pre>
  <code> 
 const task = {
  tasks: [{
        text: 'Grocery Shopping',
        completed: true
    },{
        text: 'GraphQl Course',
        completed: false
    },{
        text: 'Node course',
        completed: false
    }]
};
</code>
</pre> 

# Answer:

<pre class="notranslate">
  <code> 
const task = {
    tasks: [{
        text: 'Grocery Shopping',
        completed: true
    },{
        text: 'GraphQl Course',
        completed: false
    },{
        text: 'Node course',
        completed: false
    }],
    getTasksToDo:function(){
        return this.tasks.filter(task => !task.completed).map(task => task.text);
        //This will only return tasks names which are not completed.
    },
    getTasksToDo2:function(){
        const taskTodO=this.tasks.filter((task)=>{
            return task.completed==false;
        })
        return taskTodO; //This will return array of tasks which are not completed.
    },
    getTasksToDo3:function(){
       return this.tasks.filter((task)=> task.completed==false);
       //This will return array of tasks which are not completed.
    }
}
console.log(task.getTasksToDo3());
</code>
</pre> 
