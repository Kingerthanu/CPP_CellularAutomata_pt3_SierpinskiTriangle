# CPP_CellularAutomata_pt3_SierpinskiTriangle
A CPP OpenGL project in which uses cellular automata to draw fractal triangles according to Sierpinski's triangles.
This project really annoyed me as was trying to calculate fractal triangles based on random selected points with a indexing system going from top-left pixel to bottom-right pixel. What I realized was my designs were upside down and tried trouble shooting.

<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/ef802780-e99e-4cc3-99d2-3d460fb3d8f2" alt="Cornstarch <3" width="85" height="89">


I've been seeing "dripping" (as seen in the gif demo) visual anomalies but chaulked it up to something random with probability or the rand() function with concurrent entries. I didn't realize that I was calulating technically the peak before the base, so was always getting upside down fractal triangles and tried religiously to find out how to keep the same indexing of 0 -> size but realized this stradegy was the problem as indexing this way with neighbors means it wouldn't know where the base was and would treat this peak point as a base point causing problems. What I realized I had to do was simply reverse index as this was the only way to do this without complexing the problem unneccessarily as then it would be calculating the base before the peak of any given triangle. (this again will be relying in libraries stated in previous cellular automata.


----------------------------------------------
<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49">


**The Breakdown:**

  A C++ Program In Which Uses OpenGL And GLSL In Order To Make A Window In Which To Represent Sirpinski's Triangles With.


<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49">

----------------------------------------------

<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49">



**Features**

![fractalTriangle-ezgif com-optimize](https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/88aaf283-9c14-4935-a187-34eb19e2dde8)


<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49">

