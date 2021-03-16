# Juggling Performance Feedback

**  Introduction      **

One of the best ways to improve at a hobby is to measure your current performance and get feedback. Coaches for sports have increasingly advanced methods for analyzing performance, and technical tools can provide insight beyond the human eye, see this article: https://journals.sagepub.com/doi/full/10.1177/1747954118808081.   
This project's goal is to provide juggling performance feedback so that people can improve in their skill.   The first implementation of this feedback performance will be simple, and perhaps not deployable, but I'm excited to see where this will go. Hopefully it will become a web-app that the juggling community on Instagram can utilize, so they can share their results. 

**  Technical Overview**

When juggling, the objects make a sound as they hit the juggler's hand. In a quiet room, a simple measure of the number of catches a juggler makes could be determined by how many times this "slap" sound occurs in a stretch of audio.

R allows for audio processing and recording, and is a robust language for data analysis. This code will:
     
  1. Record baseline audio of juggling slaps
  2. Record juggling "performance"
  3. Process audio and determine catch metrics: number of total catches, number of       catches per second (or minute), and if a trick "qualifies".
  4. A qualify occurs when a juggler catches twice as many times as the object being      juggled, and is a basic standard for having "learned" a trick. The program will      ask how many balls are being juggled, and what trick they are attempting. Using      the simple Qualify = 2*Object formula, this metric will be calculated and given      to the user.
  5. The final report, after user queries, will look something like this:
  
 _ "Congratulations! You juggled 4 balls for 45.5 seconds. You had 52 catches, averaging 1.2 catches per second. You selected the Four Ball Fountain trick, and you qualified in 5 seconds with 8 catches."_

