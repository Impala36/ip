# User Guide - Duke

A Personal Assistant Chatbot that helps a person to keep track of various things. It's named after the Java mascot _Duke_. Given below are instructions on how to use it.

## Setting up in Intellij

Prerequisites: JDK 11, update Intellij to the most recent version.

1. Open Intellij (if you are not in the welcome screen, click: `File` >: `Close Project` to close the existing project dialog first)
1. Set up the correct JDK version, as follows:
   1. Click: `Configure` >: `Structure for New Projects` and then: `Project Settings` >: `Project` >: `Project SDK`
   1. If JDK 11 is listed in the drop down, select it. If it is not, click: `New...` and select the directory where you installed JDK 11
   1. Click: `OK`
1. Import the project into Intellij as follows:
   1. Click: `Open or Import`.
   1. Select the project directory, and click: `OK`
   1. If there are any further prompts, accept the defaults.
1. After the importing is complete, locate the: `src/main/java/duke/Duke.java` file, right-click it, and choose: `Run Duke.main()`. If the setup is correct, you should see something like the below:
  ```
 ____        _        
|  _ \ _   _| | _____ 
| | | | | | | |/ / _ \
| |_| | |_| |   <  __/
|____/ \__,_|_|\_\___|


⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢
Hello! I'm Duke.
I can help you manage a list of tasks!
What you can tell me to do is listed below:
  ⬡  Create a Todo task     | todo <your task>
  ⬢  Create a Deadline task | deadline <your task> /by <dd/MM/yyyy HHmm>
  ⬡  Create an Event task   | event <your task> /at <dd/MM/yyyy HHmm> /to <HHmm>
  ⬢  Complete a task        | done <task index number>
  ⬡  Delete a task          | delete <task index number>
  ⬢  List down all tasks    | list
  ⬡  Find tasks with word   | find <word>
  ⬢  Exit my program        | bye or hit Enter
⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢⬡⬡⬢⬢

It looks like it's your first time as I could not find any existing task file.
Get started by creating a task!
```

## Features    
  - Create a Todo task    : `todo`
  - Create a Deadline task: `deadline`
  - Create an Event task  : `event`
  - Complete a task       : `done`
  - Delete a task         : `delete`
  - List down all tasks   : `list`
  - Find tasks with word  : `find`
  - Exit my program       : `exit`
  
 #### Create a Todo task    : `todo`
 Creates a Todo task and adds it to the task list.
 
 Format: `todo <your task>`
 
 Examples:
 - `todo feed a dodo`
 
 #### Create a Deadline task: `deadline`
 Creates a Deadline task and adds it to the task list.
 
 Format: `deadline <your task> /by <dd/MM/yyyy HHmm>`
 - `HHmm` ranges from 0000 to 2359.
 
 Examples:
 - `deadline dead /by 28/09/2020 2359`
 
 #### Create an Event task  : `event`
 Creates an Event task and adds it to the task list.
 
 Format: `event <your task> /at <dd/MM/yyyy HHmm> /to <HHmm>`
  - The first `HHmm` is referred as the starting time of the event.
  - The second `HHmm` is referred as the ending time of the event.
  
 Examples:
 - `event internal meeting /at 28/09/2020 0900 /to 1100`
 
 #### Complete a task       : `done`
 Completes a task and sets its status to ✓.
 
 Format: `done <task index number>`
 - The first task starts from index number 1 and so on.
   
 Examples:
 - `done 2`
 
 #### Delete a task         : `delete`
 Removes a task from the task list and shifts the remaining tasks accordingly.
 
 Format: `delete <task index number>`
 
 Examples:
 - `delete 3`
 
 #### List down all tasks   : `list`
 Lists down all tasks in the task list.
 
 Format: `list`
 
 #### Find tasks with word  : `find`
 Finds all tasks that matches with the search word(s).
 
 Format: `find <word>`
 - `find` works like a filter too. You can find tasks according to their type.
 - You can also find tasks by date, month, time and status.

 Examples:
 - `find deadline`
 - `find meeting`
 - `find 28 Sep`
 - `find ✓`
 
 #### Exit the program       : `exit`
 Exits the program.
 
 Format: `bye`, `exit`, `<hit Enter>`
 
 
 ## Command Summary
 Action | Format, Examples
 ------------ | -------------
 **todo** | `todo <your task>` <br> e.g. `todo feed a dodo`
 **deadline**   | `deadline <your task> /by <dd/MM/yyyy HHmm>` <br> e.g. `deadline dead /by 28/09/2020 2359`
 **event**   | `event <your task> /at <dd/MM/yyyy HHmm> /to <HHmm>` <br> e.g. `event internal meeting /at 28/09/2020 0900 /to 1100`
 **done**   | `done <task index number>` <br> e.g. `done 2`
 **delete**   | `delete <task index number>` <br> e.g. `delete 3`
 **list**   | `list`
 **find**   | `find <word>` <br> e.g. <br> `find deadline` <br> `find meeting` <br> `find 28 Sep` <br> `find ✓`
 **exit**   | `exit`
