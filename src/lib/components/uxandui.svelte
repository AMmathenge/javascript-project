<script>
    
    // let taskInput = document.querySelectorAll('#task-form')

    // function addTask(e) {

    //     e.preventDefault();

    //     if(taskInput.value === ''){
    //         alert('add a task');
    //     }
        
        
        
        
    // } 
    // console.log(taskInput)

        
</script>
<main>
    <title>Task List</title>
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="card" id="main">
                    <div class="car-content">
                        <span class="card-title">Task List</span>
                        <div class="row">
                            <form id="task-form"  action="./  ">
                               <div>
                                    <input type="text" name="task" id="task">
                                    <label for="task">New Task</label>
                               </div>
                               <input type="submit" on:click|preventDefault|once= {() => alert('you clicked the clicker')  } value="Add task" class="btn">
                            </form>
                        </div>
                    </div>
                </div>
                <div class="card-action">
                    <h5 id="task-title">
                        Tasks
                    </h5>
                    <div class="input-fie">
                        <input type="filter" name="filter" id="filter">
                        <label for="filter">filter Tasks</label>
                    </div>
                    <ul class="collection"></ul>
                    <a href="#"  class="clear-tasks btn black">clear-tasks</a>
                </div>
            </div>
        </div>

    </div>

</main>