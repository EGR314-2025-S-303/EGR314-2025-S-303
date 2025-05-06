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




## Version 2.0: Communication Architecture and Project Direction Improvements

If we were to develop a Version 2.0 of our communication architecture, one of the first improvements would be setting a clearer foundation for the overall project direction. Early in the design process, our concept—focused on a heat-controlled cooling station—met the course requirements but lacked the kind of interactivity and engagement that might have made the system more dynamic and fun. In hindsight, selecting a more centralized and interactive concept would have motivated a more cohesive design and made demonstrations more compelling. For example, instead of simply toggling fan speeds based on temperature, a Version 2.0 project might involve user-controlled challenges, visual feedback, or gamified input—providing a better platform to showcase our technical work and creativity.

From a team dynamics perspective, we would also improve how we align subsystem roles with individual skills. A more intentional conversation early in the semester about each member’s strengths in C, Python, or debugging tools could have made a significant impact on productivity. This would have allowed us to assign team members to microcontroller platforms that best matched their experience. For instance, members comfortable with Python could take on ESP32-based subsystems, while those familiar with MPLAB and C could handle tasks like sensor interfacing on PIC.

One of the biggest architectural shifts would be to move most subsystems—especially the HMI and display module—to the ESP32 using MicroPython. Python’s terminal-based interface allows for easy debugging, print statements, and dynamic testing, which dramatically improves development speed and reliability. In contrast, MPLAB for PIC offers limited real-time feedback, making it harder to identify and resolve issues. This shift would make the system more developer-friendly and reduce time spent troubleshooting UART messages, peripheral registers, or mismatched settings.

That said, the PIC microcontroller still offers benefits in dedicated, one-way communication roles. For instance, the temperature sensor subsystem only needs to measure data and broadcast it at fixed intervals. By keeping this task isolated to the PIC using minimal C code, we reduce complexity and ensure reliable performance. In this configuration, the PIC would serve strictly as a transmit-only node, simplifying its firmware by removing the need to parse or respond to incoming messages.

On the protocol side, Version 2.0 would improve message structure by including checksums or message counters to validate data integrity, detect dropped messages, and improve synchronization. Additionally, we would modularize our codebase, separating low-level hardware interfaces, message parsing, and application logic into clean, reusable components. Most of this could be shared across Python-based subsystems, reducing duplication and improving team collaboration.

To further enhance reliability and system-level feedback, we’d implement heartbeat/status pings, watchdog timers, and perhaps an error-reporting protocol so subsystems could identify and respond to faults more effectively. These changes would help create a more robust, fault-tolerant system architecture.

In summary, Version 2.0 of our project would benefit from a better conceptual foundation, a more engaging project focus, smarter alignment of team skills, and a platform strategy built around the ESP32 for flexibility and debuggability. Coupled with refined message protocols, modular code, and added reliability features, this version would be more functional, easier to develop, and more impressive to demonstrate.



