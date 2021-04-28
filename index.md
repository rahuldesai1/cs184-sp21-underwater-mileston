## CS 184 Milestone Deliverable 

### What We Have Accomplished

In the past two weeks we worked on two main tasks: using blender to generate a variety of scenes containing water and implementing an algorithm for rendering caustics. 

After reading and watching videos on ways to represent water, we found the most straightforward way was to build on the 3-2 dae files, treating water as a glass material with the appropriate IOR. We imported files into blender to maintain the scene structure, added stretched cubes to represent the water, then edited the exported dae files to give the objects the correct material. While we were able to render our results, they were not what we expected, and most of our time was spent playing with the geometries and dae files to get a proper looking result.

For rendering caustics, we spent the first week reading papers and learning about 3 potential implementations for this. We finally settled on implementing photon mapping because it seemed to provide the best and most efficient results. After putting together a detailed design doc, we were able to implement both phases of the photon mapping algorithm for both the global and caustic photon map. We are working on debugging our implementation because we are currently only able to render a black screen. 


### Preliminary Results

The results were not what we expected, and we were running into two main issues. The first was that the glass material applied to the cube seemed to incorrectly refract the light. This problem was seemingly fixed by greatly increasing the number of vertices in the cube, and learning that in blender, cubes by default don’t have “sharp vertices.” The second main issue was as we increased the volume of our glass cubes, the result would get noisier and become dark. This issue was somewhat alleviated by the previous two edits, however still persists in our larger renders. One alteration that did help with noise was to extend the edges of the water slightly past the walls. This helped prevent clipping and bounces between the water edge and wall edge, creating a darker image.

As mentioned, above we do not yet have any successfully rendered scenes because we have run into some trouble while debugging the photon mapping implementation. 

### Reflect on Progress

Creating the dae files definitely took more work than expected. Although we currently have files that look decent enough to use in the final product, we are planning to spend the next few days playing around with various sample sizes to see if we can combat the noise and make it a bit more clear.

Although we would have liked to have presented some results with realistic caustics by the milestone, we underestimated the difficulty of completing such an open-ended project. Fortunately, after utilizing office hours and spending quite a bit of time doing research, we have a more clear direction going forward and are confident that we can have results by the final presentation. We are only about a day or two behind schedule which may prevent us from achieving our stretch goals; however, we are hoping to finish the caustics and move on to implementing the shafts of light (god rays) by the end of this week.

### Updated Work Plan
 
#### Week 3: (Finish Coding)
- Finalize scenes to use in final renders
- Finish debugging the photon map implementation 
- Design doc for implementing underwater shafts of light 
 
#### Week 4: (Write up and Polish)
- Debug shafts of light implementation 
- Write up and Final Deliverable 

### Links
[Milestone Slides](https://docs.google.com/presentation/d/1JgAd3lilTmoiufPZnNeRONZorxrhZchyqbbxGdDlDOc/edit?usp=sharing)

[Milestone Video](https://drive.google.com/drive/folders/122pEE70aHWoHjTOr0-Znot9TadbaRrT7?usp=sharing) 
