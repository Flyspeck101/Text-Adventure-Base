# How to use Text Adventure Base

To use Text Adventure Base, you'll first want to clone this repository. To do so, click on the "Code" Button, and select HTTPS. Then, copy the URL in the text area (or just copy this: https://github.com/Flyspeck101/Text-Adventure-Base.git). Next, in the top right corner of your GitHub page, click the + button, and select "Import Repository". Paste the URL into the text area labeled "Your old repository’s clone URL". Name your repository, make sure the repo's visibility is public, and click "Begin Import". Wait for the import to finish. This may take some time, so be patient. I'm calling mine "WotM" (War of the Muffins).

![image](https://user-images.githubusercontent.com/74536088/140626196-e24a6056-a860-469f-a37b-169563ceafb3.png)

When your repo has finished importing, find it, and edit `index.js`. 

![image](https://user-images.githubusercontent.com/74536088/140626227-d5bde16b-d669-4711-b6f7-2af1821ac922.png)

In `index.js`, scroll to the very bottom of the code, until you find the `notify` function. Feel free to edit this. 

![image](https://user-images.githubusercontent.com/74536088/140626297-959d4819-d404-4883-95b8-5d6ab81285e5.png)

When you have finished, commit your changes, and go into `index.html`. 

![image](https://user-images.githubusercontent.com/74536088/140626306-92acdb2b-3eb8-4122-9153-2612caa50267.png)

Change the title to whatever you want it to be by editing the contents of the `<title>` tag. 

![image](https://user-images.githubusercontent.com/74536088/140626330-7233fa68-b414-4848-a544-8b8ce52ca0d4.png)

Then, go down into the `<style>` tag and edit the CSS to whatever you like. 

Finally, edit the first `<p>` tag in `<body>` to whatever you want the notification bar to display when the page loads. 

![image](https://user-images.githubusercontent.com/74536088/140626373-93c17f8d-8ba2-487d-8d28-e2863c81270c.png)

Commit your changes, and then go into `rooms.js`. 

![image](https://user-images.githubusercontent.com/74536088/140626393-fb8c39b1-9e4e-49a8-9b46-23df88aeadb5.png)

In the object `rooms`, you can add as many rooms to the game as you like. The default room structure is as follows:

---------------
| Lab |    |
---------------
| Hole |    |
----------------
| Forest | Clearing |
------

To add rooms, you must follow this structure: 

```
<roomId>: {
  name: "<Room Name>",
  description: "<Room Description>",
  items: {
    <itemId>: {
      name: "<Item Name>",
      onGrab: () => {
        <What happens when the item is picked up>
      },
      onDrop: () => { 
        <What happens when the item is dropped>
      }
    }
  },
  exits: {
    north: {
      to: "lab",
      locked: true
    },
    up: {
      to: "windyPath",
      locked: true
    }
  }
}
```
You do not need to include any items. If you don't, then `items` should look like this:
```
items: {

}
```
The same applies to `onGrab` and `onDrop`.

Now, you can add as many rooms and items as you like. by changing `index.js`, you can even add inventory limits or other fancy stuff. 

When that is all done, you just need to activate GitHub Pages, via Settings -> Pages. 
