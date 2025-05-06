---
title: Reflections
tags:
---

# Reflections

## **Top 10 Things Learned in EGR 314**

Throughout the course of this project, our team learned several valuable lessons that extended far beyond just building hardware. One of the most important lessons was understanding how to use datasheets effectively—not just for verifying pinouts or voltage ranges, but also for identifying what circuits or configurations work best with a given component. This included selecting supporting components that complement our microcontroller and voltage regulator, ensuring both electrical and functional compatibility.

We also learned how structured communication protocols should be designed, particularly when constrained to 8-bit compilers and fixed-size message formats such as the 64-byte UART protocol we used. This experience gave us a deeper appreciation for the challenges and nuances of embedded communication. Related to this, we learned how to properly implement pull-up and pull-down resistors to ensure predictable digital behavior in input circuits.

As we moved deeper into design implementation, we became more proficient at extracting the exact information we needed from datasheets—such as electrical characteristics, timing diagrams, and setup conditions—and using that data to properly configure our components in code and hardware. Our coding skills grew significantly, not just in embedded C for microcontroller programming, but also in Python for testing and simulation purposes. Along the way, we gained experience in debugging using both software tools like breakpoints and hardware tools like oscilloscopes, which allowed us to verify functionality and troubleshoot difficult issues.

One major takeaway was the importance of clear communication within the team. It became essential to align our interpretation of assignment goals with our individual subsystem responsibilities, especially as integration deadlines approached. Time management also proved critical—we learned to use the lead time before checkoffs not just for implementation, but for researching unfamiliar concepts, refining our approach, and asking targeted questions.

Finally, one of the most practical lessons we learned was how to adapt on the fly. When things didn’t go as planned—whether due to a short circuit, a failed board, or unexpected behavior—we learned how to quickly troubleshoot, reroute connections, and implement fixes under pressure. This flexibility and fast problem-solving mindset proved just as important as our technical skills in meeting deadlines and achieving a successful final demonstration.



##  Top 5 Recommendations for Future Students

1. **Start Early and Stay Organized**  
   Work ahead on assignments and meet with your teammates regularly. The course timeline is fast-paced, and deadlines can pile up quickly if you fall behind.

2. **Complete All the Labs**  
   The lab exercises build foundational skills that become essential when working on your individual subsystem and during team integration. Don't skip them—they directly support your success in the final project.

3. **Master Datasheets and Leverage Tools**  
   Learn how to properly read and interpret component datasheets. When you're unsure, use tools like AI or forums to gain clarity on specifications, pinouts, or recommended usage.

4. **Practice Soldering Surface-Mount Components**  
   Many of the components used in this course are SMDs (Surface-Mount Devices). Practicing your soldering skills early will make hardware assembly much smoother and less stressful.

5. **Take Advantage of Office Hours**  
   Use office hours to ask questions and get help. Whether you're stuck on debugging, need clarification on a concept, or want feedback on your design, these sessions are a valuable resource.




- Lessons Learned: What are the top 10 most important things that your team learned from working on this project? You may use feedback received from the design review and content you discussed in status reports to address this section. (use full sentences, ½ page minimum)
- Recommendations for future students: Create a numbered list with the top five recommendations for future students of what they should learn or do to prepare themselves for taking this class. Each item must be at least one complete sentence long.
- Version 2.0: If you were to create a "Version 2.0" of your communication architecture, discuss what could be improved and why it should be improved. Use the included diagrams to support the discussion. What new functions would be necessary? How would you divide up your code? How would you improve its debuggability? What peripherals or system features would you like to use or set up to make your system more reliable, stable, functional, or robust? How would you simplify, improve, or update your protocol design to support this in software? (1/2 page minimum)
