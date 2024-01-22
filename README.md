# CPP_CellularAutomata_pt3_SierpinskiTriangle
A CPP OpenGL project in which uses cellular automata to draw fractal triangles according to Sierpinski's triangles.
This project really annoyed me as was trying to calculate fractal triangles based on random selected points with a indexing system going from top-left pixel to bottom-right pixel. What I realized was my designs were upside down and tried trouble shooting. I've been seeing "dripping" visual anomalies but chaulked it up to something random with probaility or the rand() function with concurrent entries. I didn't realize that I was calulating technically the peak before the base, so was always getting upside down fractal triangles and tried religiously to find out how to keep the same indexing of 0 -> size but realized this stradegy was the problem as indexing this way with neighbors means it wouldn't know where the base was and would treat this peak point as a base point causing problems. What I realized I had to do was simply reverse index as this was the only way to do this without complexing the problem unneccessarily as then it would be calculating the base before the peak of any given triangle. (this again will be relying in libraries stated in previous cellular automata.

![fractalTriangle-ezgif com-optimize](https://github.com/Kingerthanu/CPP_CellularAutomata_pt3_SierpinskiTriangle/assets/76754592/88aaf283-9c14-4935-a187-34eb19e2dde8)
