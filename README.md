# example

Usage of Redux DevTools:
In this document we will see some basic step by step process to achieve things (with screenshots), so it will speed up development and debugging. 
Step 1
Go to the following links and install the browser add-on or extension:
•	Firefox: <Replace link>
•	Chrome:  <Replace link>
This extension is important for connecting your browser to the Redux application. Without it, you will not be able to load the tools from your console.

Step 2
If you’ve installed the browser extension correctly, you will see a Redux option in the console.
  
  ![image](https://user-images.githubusercontent.com/67333630/126805396-db7596d9-57c2-42e7-bc27-d24a272f5ffe.png)

 

When you click on this new option (Redux), you will see one of two things. If you installed everything correctly in your store initialization, it would show you something like this:  
  
  ![image](https://user-images.githubusercontent.com/67333630/126805920-ed9ccac9-c276-4d0c-87d8-4ee679057575.png)


If there is an error in your set-up, including exceptions thrown from your code, you will see this:
  ![image](https://user-images.githubusercontent.com/67333630/126805966-cd4c4454-ec07-46e3-8cbb-0179269ada08.png)

 

Step 3

We will see how to debug the state using this DevTools in this step.
The left-hand column of the Devtools is showing in real time the actions that are firing on the current page (as defined by the action creator types).
 ![image](https://user-images.githubusercontent.com/67333630/126806016-1414c713-1995-49b5-b0e5-cc5d0e21245b.png)


Right-Side Console Tools The four tabs at the top right are in my opinion the most helpful of the tools.
  
  ![image](https://user-images.githubusercontent.com/67333630/126806081-a0346bfa-c916-4cf6-9e8d-0f2d9fc7b1aa.png)

 
Action:
Clicking on the Action tab will show the individual action type and any data it is carrying along to the reducers.
It contains three sub tabs Tree, Chart, Raw within this master Action tab. These display the same data just in different formats.
•	The Tree view is the default view and summarizes the data into single lines.
•	The Chart tab shows the up-to-date store tree. Including all of the combined reducers and their corresponding data branches.
•	The Raw ab shows the action creator in a code view.
State
The state tab shows the entire state tree at the time of the action selected in the left-hand side of the console. 
Diff: 
When an action is selected in the left-hand side of the console, the Diff option will show only what that individual action changed in the state tree.
Trace:
This is called the action stack trace, it helps you track where a particular Redux action was dispatched from
Test
This will create a test format in some pre-provided testing frameworks. It takes your root state and provides a written test on what the end state should hold



Top Console
 ![image](https://user-images.githubusercontent.com/67333630/126806115-4c1e6386-64e9-49f2-a4f5-2d3861238d4b.png)


The top of the console offers two more sets of tabs. The right tab lets you flip between different instances of running apps on the page. If you have different stores running on the same page.
The left set of tabs shows different modes:
•	Inspector: the most used and is the default mode. Shows all the tools that have been discussed here.
•	Log Monitor shows complete state and actions, as opposed to the Inspector mode where it just shows the diffs. (Try using the slider while in this view and watch your state tree grow/shrink!)
•	Chart shows the state in a tree-like structure.

Bottom Toolbar
 ![image](https://user-images.githubusercontent.com/67333630/126806159-584fe015-2568-4b13-b9cc-125860356dcf.png)

The bottom of the console provides more functionality for diving into your actions and state. It allows for time travel, dispatching actions, importing/exporting state, and remote control. Starting from the far left, the first three options are for creating a new console view ether to the left, right, or bottom.
•	The Pause recording does not stop other actions from firing within your app, it is just stopping the recording of actions within the console. Unlike other abilities within the console it does not control the state of your running browser page.

•	The Lock changes will actually freeze the running app’s other/future actions. So it takes Pause recording to the next level by locking any future state changes in your app.


•	The Persist option will keep the current state even when the page reloads

•	The Dispatcher option will ether show or hide the dispatching module. Which can be used to fire a custom action with custom data.

 ![image](https://user-images.githubusercontent.com/67333630/126806197-bf545269-c070-4d54-b022-ca89b44ae51d.png)


•	The Slider option will give you a smooth scroll through the actions. This will time travel through the actions that have fired and update the running app to show the current state and certain points in time. This comes packed with an auto-play, one step action arrows, and a speed interval play-through time.

![image](https://user-images.githubusercontent.com/67333630/126806226-18bcc6f7-b6d7-4409-90b9-5bdf95611a16.png)

 

•	The import and export options are for importing/exporting state as JSON into the application. Which enables you to run your app off custom state.

•	The Remote option creates a separate console, not connected to the browser console tools. This will run the same actions but “remotely” away from the dev-tools.

