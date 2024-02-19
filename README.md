# SNHU_CS350
## CS350 Emerging Systems Architectures & Technologies


### Summarize the project and what problem it was solving.
The purpose of this project is to develop a prototype of a low-level thermostat for SysTec. Embedded systems are an integral part of almost everything we use on a daily basis. Technology is increasing involving and Internet of Things (IoT) is already part of our lives. Developing a Wi-Fi enabled thermostat has numerous uses including being integrated as part of a Smart-Home or Smart-Buiding IoT infrastructure. 

### What did you do particularly well?
I had a lot of fun implementing the Task Scheduler, and this is probably what I am most proud of. The Task Scheduler demonstrates how multiple tasks can be implemented in an embedded system using state machine's. In this project, we sample the temperature sensor, button presses, and update the LED/UART, all on separate timers. The process of implementing scheduler also demonstrates how to program efficiently, which is necessary in embedded systems.

### Where could you improve?
I could have improved on bit manipulation to improve efficiency. For example, in some of the assignments, I just use a char to represent the state. I could have represented that as hex instead, and potentially made the overall algorithm more efficient.

### What tools and/or resources are you adding to your support network?
Something we learn in embedded systems is the use of header files and that we need to rely on them for implementation details to be successful. I learned more by reading documentation in manufacturer header files than from any other source. Texas Instruments (TI) has a good support forum where customers can ask questions. I think this is big consideration for the future if I need to research and/or purchase something for my company.

### What skills from this project will be particularly transferable to other projects and/or course work?
There are several transferable skills that I learned in this course. First, one of the key things we learned in the course is how embedded systems use timers. This is extremely close to the "bare metal", and is analogous to how we use threading in high-level languages. Understanding how it is done in embedded programming prepares us for more efficient programming. Second, the use of bit manipulators can lead to much more efficient programs as well. Our Zybook provided great lessons on how to use bit manipulation, which I will use in the future.

### How did you make this project maintainable, readable, and adaptable?
The primary way that we made this project maintainable, readable, and adaptable is by implementing the cooperative task scheduler to manage the three main tasks. We could have implemented this project by micromanaging tasks individually in the main code loop, however this type of solution leads to "spaghetti code". It would be extremely difficult to maintain, troubleshoot, and understand as the code base matures.  
By implementing a cooperative task scheduler, our code is organized based on the three main tasks. In each task, we set up the timers and control variables. The scheduler is configured to "tick" based on the GCD period of all three timers. In this implementation, managing the three tasks is clear, organized, and demonstrates a system that can scale to as many tasks as we need in the future.
