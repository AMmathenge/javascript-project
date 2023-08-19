<script>

//    localStorage.setItem('name','john')

  

  
//    let name = localStorage.getItem('name') || ''; // Initialize with the stored value, or an empty string if not present
    let  task = '';
    let tasks;

        if (localStorage.getItem('tasks ') == null) {
            tasks = [];
        } else {
            tasks = JSON.parse(localStorage.getItem('tasks'));
        }
    // let tasks;

    //     if (localStorage.getItem('tasks') == null) {
    //         tasks = [];
    //     } else {
    //         tasks = JSON.parse(localStorage.getItem('tasks'));
    //     }

    function addTask(e) {
        tasks.push(task);

        localStorage.setItem('task' , JSON.stringify(tasks));
        alert('Task saved')

    } 
    const getTasks = JSON.parse(localStorage.getItem('tasks'));

    getTasks.forEach((task) => {
        console.log(task);
    });
       

</script> 

<main>
    <div>
        <div>
            <h1>
                Task list
            </h1>
            
            <form action="" id="task" on:submit={addTask} >
                <div>
                    <input type="text" bind:value={task}  name="task">
                    <label for="task">New Task</label>
                </div>
                <input type="submit" value="Add Task" >
            </form>
            
        </div>
    </div>
</main>