## Implementation of A* Algorithm and applied to a self-driving car on Carla Simulator

![Pretend there is a A* algorithm image here ;) ](https://github.com/AlejandroSoumah/Maxim_Simulator_AstarAlgorithm/blob/main/A*.png)
I created my own implementation of the A* algorithm. At the start I used a "satellite map" of the map in the simulation, I took the image and segmented the road structure using classic visual perception techniques (skeletonize, erode… ) and did it using the pixels of the resulting image. I then transformed the pixel values to the global coordinate frame and created a path from there. This approach was pretty simple, and I did not find difficulties with it

Now a more accurate method is applied, instead of a "satellite map" the road structure is segmented by the vehicle being driven around the circuit. Then images are taken and the road is segmented online using a Convolutional NN structure. Then the border of the road is found using classical visual perception techniques the borders are transformed to the global coordinate frame. The resulting image is skeletonized, eroded and dilated to produce the Map in which A* takes place - As seen above - (Mapping is the video showing this)
