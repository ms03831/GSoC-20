---
title: Final Milestone - Adding Drag-Drop-Connect canvas for circuit equations
date: 2020-07-19
tags: GSoC
---

<hr>

- Second milestone is now complete! DNA sequences have been incorporated. See the [post](https://ms03831.github.io/GSoC-20/update/milestone-2-dna-sequence-sbol/) for more details.

- Opened a pull request for the second milestone and merged the code.

- Cleaned the repository. 
  - Removed the Java code and any traces of it from the repository to make sure it's python only
  - Removed modules (such as file_writer.py) that were unused from the code
  - Added a bit more organisation, generated xml files are now saved in user_files folder which is generated in runtime.
  - For future:
    - Look into the issue that GeneTech sometimes doesn't generate circuits (optimisation issue)
    - The functions.py by previous contributors $MAY$ have some bugs, look into that!
	
# Final Milestone 
- To get a feel of what we are trying to do, see the image below: 
![Wireframe]({{ "assets/images/wireframe.png" | absolute_url }})

- A “Draw” push button has been added to the main GeneTech window. Clicking on the “Draw” button, as shown below, the user
would be directed to a new page to construct a genetic circuit using the standard glyphs of digital electronic gates.
![Draw button]({{ "assets/images/draw.png" | absolute_url }})

- I have already made the icons for the gates that we are going to use, they are: 
![AND]({{ "assets/images/AND.png" | absolute_url }})
![OR]({{ "assets/images/OR.png" | absolute_url }})
![NOT]({{ "assets/images/NOT.png" | absolute_url }})
![NOR]({{ "assets/images/AND.png" | absolute_url }})
![NAND]({{ "assets/images/NAND.png" | absolute_url }})


- To actually build the canvas, I started out by first learning a bit of PyQT5. 

- I started with a QtWidget and layout structure to first build the canvas. I got here: 
![qt_widget]({{ "assets/images/qt_widget.png" | absolute_url }})

- This canvas allowed drag and drop.. But there was a problem. As soon as you drag the object from right pane to left pane, it is not dropped where you place it, 
rather it is first dropped at the top left corner of the left pane, and then only you can drag it where you want. I tried but couldn't fix this issue. 
So I abandonded using QtWidget directly. This decision took some time to take. But it's for the better hopefully.

- To overcome this issue, I have come around a workaround for this. I will now build a Graphics Scene inside of the widget. 
The Graphics scene allows extensive functionality.. right now this is how it looks :) The graphics scene also allowed me to add 
a extending canvas (look at the scroll bars)
![qt_graphics]({{ "assets/images/qt_graphics.png" | absolute_url }})




