- link to the webpage https://andrefls.github.io/Workshop-task-2/

...
Synopsis

When I started working on this workshop task, my goal was to calculate the time it takes for the bouncing balls to complete the explosion. This would allow me to add a couple of extra seconds for the explosion itself and then effectively restart the animation cycle.

Additionally, I aimed to make the project interactive. I thought that by giving people the ability to stop the animation at any time, they could create unique moments, offering a new way to express art.

Summary/Problem-solving

I first watched our lecture video at https://canvas.auckland.ac.nz/courses/121821/pages/week-1-overview?module_item_id=2435967. From the video, I took useful notes to create my GitHub account and download VSCodium, and I also started working on it.

I began following the examples from our lecture, but I struggled with the counter and intervals concept. After getting frustrated with the examples, I went to https://p5js.org/reference/ to look for ideas to time my explosion.

After extensive reading, I still couldn't find anything that worked for me. I thought there must be something out there, but I just wasn't sure how to ask about it. So, I decided to search on Google at www.google.com and asked if p5.js has a reference for time intervals.

After several attempts, I found the p5.js reference for the millis() function at https://p5js.org/reference/p5/millis/. 

This was exactly what I was looking for, but the challenge began when I struggled to understand how to use it. I followed the instructions, but after several hours of trying, I encountered the error: "SyntaxError: Unexpected identifier 'explosionTime.' Expected ')' to end an 'if' condition." This was confusing for me.

After reading about millis() and analyzing the error a couple of times, I realized that the function was returning the total time cycle in milliseconds after the explosion. However, since there was no limit for the explosion time, the cycle kept running endlessly. I started incorporating mathematical functions like addition and division, and when I finally used the subtraction function, everything began to make sense. I subtracted a value from the infinite cycle to set a limit.

I established a threshold by adding a value greater than or equal to the explosion time, so as long as the explosion time was less than or equal to 420, it would restart. However, I still had a lot of questions. For instance, if I changed the value to something higher than 460, like Leo suggested in the workshop video (for example, 5000 milliseconds), mine wouldn't work, and I didn’t understand why.
After resolving the issue of the cycle restarting and watching my video, I found it a bit boring to wait for the cycle to restart. 

I followed the canvas video at https://canvas.auckland.ac.nz/courses/121821/pages/week-1-overview?module_item_id=2435967 and noticed some functions involving the mouse. I thought if I could allow people to pause my animation, they would see a different image each time they paused it. 

I searched for "loop" at https://p5js.org/reference/ because that was what I wanted to pause. I found the function at https://p5js.org/reference/p5/loop/. 

I then combined the functions so that a mouse click would stop the animation, and a double click would restart the cycle. It worked perfectly! 

I realized I needed to instruct viewers on how to interact with my video. Using Discord, I asked Leo if I could add some instructions on the canvas. He agreed, recommended a few options, and even shared an example I could use: 

Image

```javascript
fill(255, 255, 255); 
rect(0, height - 20, width, 25); 
fill(0); 
text('Create Art. Click to hold the frame. Double click to loop', 20, height - 8);
```

I integrated his example into my code and it fit in my project.

Future development

I'm still unclear about why, when I use a value over 420 in my millis function, the explosion continues indefinitely without reaching a limit to restart. I’ll need to read more about timing and cycles.
I need to use VScodium more.

Conclusion:

I am still using https://p5js.org for my coding. 
I learned a different way to handle timing using the new syntax called millis.
