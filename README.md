# Assignment_1_ImageJ

# Step 1: Selecting Image  
Open Fiji  
File --> Open Samples --> Embryo  
<img width="545" height="453" alt="image" src="https://github.com/user-attachments/assets/21e88006-24cb-43c6-8125-8381b7966404" />  

# Step 2: Subtracting Background  
Process --> Subtract Background  
Rolling Ball Radius: 12.0   
After playing around with it, I realised 12 was the perfect size as the image as the original image is already well contrasted, requiring only fine tunings.  
<img width="250" height="274" alt="image" src="https://github.com/user-attachments/assets/486ed518-dc87-4791-be9b-52f69402a96d" />  
<img width="545" height="453" alt="image" src="https://github.com/user-attachments/assets/5ed3f0c0-5bfb-4151-9534-7427b956b496" />  

# Step 3: Converting Image to 8-bit  
Image --> Type --> 8-bit  
<img width="545" height="453" alt="image" src="https://github.com/user-attachments/assets/a72e4eba-f5e5-473c-9240-d3442bbf4d67" />  

# Step 4: Setting Image Threshold  
Image --> Adjust --> Threshold  
Slider 1: 0  
Slider 2: 158  
<img width="280" height="311" alt="image" src="https://github.com/user-attachments/assets/cf971a67-8064-4f3f-bb70-27d0aef13190" />  
<img width="545" height="453" alt="image" src="https://github.com/user-attachments/assets/5a0bdac3-48ae-4b05-8e39-d2cb024e8db5" />  
Although by increasing the value Slider 2 I was able to fill in the hollow spaces within embryos, it also ended up making the edges of embryos (especially clustered ones at the bottom left) less defined as well as selecting unnecessary noise particles in the background. Hence, I decided to go with the auto setting of 158, and compensate the hollow embryos using the "Fill Holes" feature in the next step.  
I would also like you to note that although the instructions you gave asked the embryo to be black and the background to be white in your protocol (I did so by selecting the "Dark Background" checkbox in Threshold Settings), on further processing I was not getting the results I wanted at the "Analyze Particles" step. It seemed to be analysing tiny particles around the embryo cell rather than the embryo itself. To troubleshoot, I tried following the same steps without selecting "Dark Background", and it worked, and hence that is what I'm following. 
<img width="545" height="453" alt="image" src="https://github.com/user-attachments/assets/d1187ac9-920e-41bd-8dfc-77b193258a46" />  

# Step 5: Fill Holes and Convert to Mask  
To fill the hollow embryos remaining.  
Process --> Binary --> Fill Holes  
<img width="545" height="453" alt="image" src="https://github.com/user-attachments/assets/fec1bd18-6070-4aa1-a6c4-7bf57286e54c" />  
Process --> Binary --> Covert to Mask  
After careful consideration, I decided not to proceed with using the Watershed function, as it was separating two cells of the same embryo as well, which was undesirable. The image is better as it is.  

# Step 6: Setting the Scale using Line Tool  
The image I have selected already has a scale at the bottom right, so I can use it as a reference to measure all cell sizes in their actual metric units rather than pixels.
I start by zooming into the bottom right corner by hovering my cursor over it and using Ctrl + Scroll Wheel to zoom in. Then, I use the Line Tool to draw a line, making sure I align both ends of each line (the line is in yellow) accurately to the ends of the scale. For panning around the image, I used the Scrolling Tool (the icon that looks like a hand).  
<img width="545" height="453" alt="image" src="https://github.com/user-attachments/assets/420a3e5c-0f60-4dc5-83ff-ef7b042e033d" />  
Next, I went to Analyze --> Set Scale
Fiji automatically gave me the distance in pixels of the line I had drawn.  
I set the known distance to "100", and the Unit of Length to "um" (micrometre), corresponding to the scale in the original picture.
<img width="249" height="290" alt="image" src="https://github.com/user-attachments/assets/4c749601-cf35-4371-bf2d-ae5aeafbe8d3" />























