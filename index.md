# User Guide - The Duke Who Manages Tasks

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
1. After the importing is complete, locate the: `src/main/java/Launcher.java` file, right-click it, and choose: `Run Launcher.main()`. If the setup is correct, you should see something like the below:
   
   ![GUI](https://github.com/Impala36/ip/blob/master/docs/images/DukeGUI.png)

## Features    
  - Create a Todo task    : `todo`
  - Create a Deadline task: `deadline`
  - Create an Event task  : `event`
  - Complete a task       : `done`
  - Delete a task         : `delete`
  - List down all tasks   : `list`
  - Find tasks with word  : `find`
  - Add a note to a task  : `note`
  - Exit my program       : `exit`
  
 #### Create a Todo task    : `todo`
 Creates a Todo task and adds it to the task list.
 
 Format: `todo <task>`
 
 Examples:
 - `todo feed a dodo`
 
 #### Create a Deadline task: `deadline`
 Creates a Deadline task and adds it to the task list.
 
 Format: `deadline <task> /by <dd/MM/yyyy HHmm>`
 - `HHmm` ranges from 0000 to 2359.
 
 Examples:
 - `deadline dead /by 28/09/2020 2359`
 
 #### Create an Event task  : `event`
 Creates an Event task and adds it to the task list.
 
 Format: `event <task> /at <dd/MM/yyyy HHmm> /to <HHmm>`
  - The first `HHmm` is referred as the starting time of the event.
  - The second `HHmm` is referred as the ending time of the event.
  
 Examples:
 - `event internal meeting /at 28/09/2020 0900 /to 1100`
 
 #### Complete a task       : `done`
 Completes a task and sets its status to D for Done.
 
 Format: `done <index>`
 - The first task starts from index number 1 and so on.
   
 Examples:
 - `done 2`
 
 #### Delete a task         : `delete`
 Removes a task and its note from the task list and shifts the remaining tasks accordingly.
 
 Format: `delete <index>`
 
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
 - `find D`
 
 #### Add a note to a task  : `note`
 Adds a note to an existing task, recording the textual information that the user inputs.
 
 Format: `note <index> <text>`
 - Adding a note to a task will replace any existing note.
 - Deleting a task will also delete any attached note.

 Examples:
 - `note 1 This is a note.`
 - `note 2 This note exists because it can.`
 
 #### Exit the program       : `exit`
 Exits the program.
 
 Format: `bye`, `exit`, `<hit Enter>`
 
 
 ##Command Summary
 Action | Format, Examples
 ------------ | -------------
 **todo** | `todo <task>` <br> e.g. `todo feed a dodo`
 **deadline**   | `deadline <task> /by <dd/MM/yyyy HHmm>` <br> e.g. `deadline dead /by 28/09/2020 2359`
 **event**   | `event <task> /at <dd/MM/yyyy HHmm> /to <HHmm>` <br> e.g. `event internal meeting /at 28/09/2020 0900 /to 1100`
 **done**   | `done <index>` <br> e.g. `done 2`
 **delete**   | `delete <index>` <br> e.g. `delete 3`
 **list**   | `list`
 **find**   | `find <word>` <br> e.g. <br> `find deadline` <br> `find meeting` <br> `find 28 Sep` <br> `find D`
 **note**   | `note <index> <text>` <br> e.g. <br> `note 1 This is a note.` <br> `note 2 This note exists because it can.`
 **exit**   | `exit`
