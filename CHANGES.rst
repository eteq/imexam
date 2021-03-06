version 0.3.dev (unreleased)
----------------------------
- added suggested changes from 2to3, and set use_2to3 to False

- restructured docs for astropy style and added more detailed example information

- general bugs fixed as they were found

- full imexam() support for arrays loaded from memory added

- restructured how the code tracks what is in the viewer. It used to track just the
  current frame, now it keeps a dictionary of what's loaded into the viewer which also
  contains some specifics about the data in each respective frame. This was necessary to 
  allow user display and tracking of arrays, but also is a nicer way to store the information
  and give users access to more details about the viewer in general if they are scripting something
  themselves. 
  
- the logging method dropped a reference in one of the last commits, this was fixed and logging the 
  session to a file for reference should be functioning correctly again.

version 0.2.dev (unreleased)
----------------------------

- zero-indexing bug fixed for data pixel display

- added support for x-D image cubes. They display, and are correctly tracked through
  the imexam loop. Several new functions were added to support this.
  
- fixed the zoom(int) bug, you can supply an int or string to the zoom function and it will be happy



version 0.1.dev (unreleased)
----------------------------

This update should address all of the issues that chanley raised,, including:

- Removing the remaining blind exceptions

- Removing unused imports

- Setting an appropriate default value for the connect.current_frame

  - the code now calls to the active window to set the frame

  - I also updated related ds9 module frame method to set the frame to a decent default if not set

- the astropy.io.fits import was simplified

- In addition, some minor typos and bugs were fixed that appeared when making these updates.
