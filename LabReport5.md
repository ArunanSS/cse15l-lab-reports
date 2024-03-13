# Lab Report 5
## **Arunachalam Senthil**

### Part 1

Student(Nirrbhay Raghavan): Hi am having some issues with my code. I ran the practice code from cse 11 and found a terminal output that needed me to run the bash file.
I see an error in the file code. I don't know where to go from here, what should be the designated output and how should I get there. Can you help me find the error and also debug it.

I included photos below with my code and error message that comes with it

<img width="666" alt="Screenshot 2024-03-12 at 10 54 48 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/244bc37e-0edf-4a13-9b96-443d616244f8">

<img width="572" alt="Screenshot 2024-03-12 at 10 55 11 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/dee06473-5753-49e7-b155-c8ffe3e83d02">

TA(Vikas Muruli): Hello! Don't stress buddy I'll help you out. Looking at the code that you have writen and the terminal I see an issue with the terminal file.
Now what I don't want to give it to you,but hears a hint to think about. We talked about different errors in class, one specific ArrayIndexOutofBounds. 
Now that you see the type of error, look in the code to check the lines where you get the error. To edit the file directly I want you to go to the professor's github and check
week 7 where we went over VIM. Now can you try that out for me then send it to me again. 

Student: Wow I can't believe I made such a simple error without registering that. You're right I see the ArrayIndexOutOfBounds error, and went on w3school to understand it better. 
I messed up on a part that I am usually very confident in, the for loop. I made a mistake with incrememnting where I went up until the index was eqaul to `place.length `. You cannot start with the array's length becayse that starts at 1, however indexes always begin counting from 0. We iterated one beyond the actual array which is why we get "indexOutOfBounds" as the error. I wasn't sure about the other part of the error initially for where it was called. But I realized that I wrote a method to take the average(shown on ln:26). That was why when called it showed as an error. The code was fixing the for loop to for(int i=0; i<place.length; i++). Now the way I edited this was with VIM. First thing I did was open the terminal, then type `vim finalTest.java`. I then finalTest and hit enter. Then I used the keyboard to navigate to the error. I then hit "i" so I could edit in vim. I made the change, and then hit "escape" on my keyboard. The final step was typing ":wq" which saved the file and exited. After I ran the code and did work, and printed the output. 

Initial Error: 

<img width="1139" alt="Screenshot 2024-03-12 at 10 55 34 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/33c01ad7-f32c-457a-8b73-4602ddfab0c9">


Correction Made:

<img width="685" alt="Screenshot 2024-03-12 at 10 56 00 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/d998f952-6f8c-4134-a5c8-629951105f7f">

<img width="565" alt="Screenshot 2024-03-12 at 10 56 19 PM" src="https://github.com/ArunanSS/cse15l-lab-reports/assets/83483462/a3ef29d6-fc99-439b-9dac-4cf3ebaf805d">





### Part 2: 

I think for me the coolest thing that I had 0 background experience with before had to be VIM. It was such a cool concept, with different commands that were so powerful. Along with that there were so mant short cuts, the first class I had no clue how to even save a file and exit VIM. By the end of class I could skip lines, edit easily, and of course save and exit the file. I believe this concept was the coolest to me because it was also very simple, and I learned it based on muscle memory and practice instead of just mugging and spitting out the information. 
