# CPP_CellularAutomata_pt3_SierpinskiTriangle
A CPP OpenGL project in which uses cellular automata to draw fractal triangles according to Sierpinski's triangles.
This project really annoyed me as was trying to calculate fractal triangles based on random selected points with a indexing system going from top-left pixel to bottom-right pixel. What I realized was my designs were upside down and tried trouble shooting.

<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/ef802780-e99e-4cc3-99d2-3d460fb3d8f2" alt="Cornstarch <3" width="85" height="89">


I've been seeing "dripping" (as seen in the gif demo) visual anomalies but chaulked it up to something random with probability or the rand() function with concurrent entries. I didn't realize that I was calulating technically the peak before the base, so was always getting upside down fractal triangles and tried religiously to find out how to keep the same indexing of 0 -> size but realized this stradegy was the problem as indexing this way with neighbors means it wouldn't know where the base was and would treat this peak point as a base point causing problems. What I realized I had to do was simply reverse index as this was the only way to do this without complexing the problem unneccessarily as then it would be calculating the base before the peak of any given triangle. (this again will be relying in libraries stated in previous cellular automata.

----------------------------------------------
<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/3f5af5d3-f82b-41a1-b625-d559f1624d15" alt="Cornstarch <3" width="55" height="49">


**The Breakdown:**

  A C++ Program In Which Uses OpenGL And GLSL In Order To Make A Window In Which To Represent Sirpinski's Triangles With.

  This Program Starts By Defining A Predefined Amount Of Hexagons In Which Will Represent Individual Cells In Which Can Be Either Alive Or Dead.

  All These Hexagons Will Be Stored In A Single VAO, VBO, And EBO As Because Our Drawing Format Won't Change We Can Easily Rely On All These Vertexes Being Positions A Cell Could Be On And Can Just Say To Color It Black To Simulate No Cell There.

  We Also Will Feed In The Offset Each Individual Index Has This Will Tell Us Where To Jump To In A Dynamically-Sized Buffer Of Hexagons To Find "Our" Hexagon Vertexes. Because We Know Our Hexagons Will Always Be Of Equal Segments We Can Easily Use A "Hard-Coded" Count Of **n** Vertexes To Update After Our Offset In Which Will Say Where These Indexes Start. 

  Using The Simple Ruleset Outlined By Siepinski's Triangles In Which Strives For 3-Alive-Neighbor Stable States, We Will Get A Shape In Which Will Represent These Infinetley Fractal Triangles.

  Other Than Being A Cool Visual, Doesn't Really Do Much... Is Dynamic To Shifting Globals Defining Its Scale But Going To Probably Update This To Fix Compounding As Well As Make It So It Can Zoom In Infinetly.

This Version Taught Me A Lot, Not Really About Siepinskis Triangles As I Saw It's Implementation Not As Hard As Actually Grasping WHAT To Actually Do. And When I Got It Done The Flipping Of The Triangles Really Confused Me.

 To The Point Presented In The Intro Statements Above I Mentioned This Way Of Having To Index Because Of How A Triangle Naturally Has To Generate Using This Algorithm But I Also Think I Could See Benefits Implementing A Flag System Check To Cells Bleeding As I Saw The Bleeding In This Procect Generally To The Same Degree As The Water Compound Effect.

<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/eb9d0b27-6ad2-4f5d-b3c9-c0258d770c56" alt="Cornstarch <3" width="55" height="49">

----------------------------------------------

<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/0e45f915-5f4a-4c39-bff9-7f49df8a88c0" alt="Cornstarch <3" width="55" height="49">



**Features**

![fractalTriangle-ezgif com-optimize](https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/88aaf283-9c14-4935-a187-34eb19e2dde8)


<img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49"> <img src="https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/d76bbd81-e0ce-460f-ad43-e86fef8ad59e" alt="Cornstarch <3" width="55" height="49">

