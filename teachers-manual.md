# Aurifex Labs - Teacher's Manual - January 2023

## Common Strategies and Tips

- It's not expected that students get through any particular exercise or project. It's all fodder for learning. Getting evidence of the core outcomes for each course is all that matters. Even the importance of the final project as a portfolio piece is up to the individual student and their goals.

- Focus on [theory building](https://pages.cs.wisc.edu/~remzi/Naur.pdf) by guiding projects into teachable moments that force a lesson to be learned to solve a particular problem of interest to the student. An analog is in video game design where you are forced to learn a new skill to advance and this becomes an anchor for the design of puzzles in the next section. An example from frontend development is suggesting autocomplete as a feature to a student. It both is exciting and feels like "real" web development to the student, but it will create race conditions and allow the teaching of await/async and the task queue at a second level of depth.

- Express to the student that you really have to practice a concept multiple times (namely three) to really understand it, and be explicit about which topics are core to the course and therefore will be repeated, and which topics are interesting and form part of the fabric of solutions for a particular course, but don't need to be internalized the same way.

- Be sure to add in one concept at a time and dig deeper, always meeting the student where they are. This requires conversations about any programming background and observation during pair programming about how a student is trying to solve a problem right now, and asking "Why?" to force a student to explain their current mental model. There's a pacing to the introduction of big concepts that is both slower and more sporadic than feels necessary at first, but introducing a concept too early isn't a problem, if it's important it'll come up again naturally a few weeks or months later and just teach it again then when more context has been developed.

- Open a blank email to the student right before each session and use it to keep notes as the student works. Include any links that you find during the class. Anything put in the chat of the video call should be copied to the email so that it's recorded somewhere permanent. Recap any parts of the class you didn't capture in the notes in the last minutes of class and send the email to student right before ending class. These emails then form the foundation of lessons for future students and also a record that each class actually happened.

- The pacing of the course is primarily dependent on the student; both their natural pace of learning this type of material and the amount of time and effort put in outside the lessons determine how much they will learn by the end of the program. The goal should be to encourage students to spend as much time writing code as possible, but to remember that you have no idea how much time a student has outside of class. So the best approach is to be sure to give a student something concrete to read or a concrete next step on their current program at the end of every class, but don't expect it to be done.

- Each session needs to be dynamic by having a plan ready based on the student not doing anything since the last session and then starting each session by having the student present any work they did at home and always use that as the starting point for that days lesson. It's easier said that done because you need to already have the experience of teaching all the material, but it quickly spins up a positive feedback loop where a student wants to write code at home and show it off and they learn faster so they can write more code at home. The alternative of sticking to the plan discourages students from writing code on their own because it moves the project in a direction that is incongruent with the lesson of the day.

- For the long term planning of the courses, once you have gotten past the first few weeks of introductory content, you should fall into a pattern of project work where students naturally get far enough into a project or take a break and you suggest starting a new project with a concrete idea that fits the natural next set of topics given a course and a specific student's current understanding. Let the need for review of previous material present itself naturally as you get into the second and third courses of a program, but when that moment comes be sure to give it the time required to shore up foundational understanding of core topics.

- The third course in each program should end with a capstone project that facilitates review of all topics and the "theory" of the capstone project should be thought of as the single artifact that the student receives from the program.

## Web Developer Program

- Coding in Javascript
- Frontend Web Development
- Backend Engineering for Web

### Coding in Javascript: Introduction, Motivation, and Tips

This is by far the most important class. The "Coding in Python" and "Programming for Embedded Systems" courses are directly based on this course. And it serves as a prerequisite for the semiconductor courses.

- The most important thing is to get as many lines of code written as possible that use the basics of variables, assignment, lookup, conditionals, loops, functions, and operators. This is more important than covering all the core outcomes in this case. They can be backfilled in the final two courses of each program. The real teaching of higher level programming concepts can really only happen efficiently once these core elements of programming have become muscle memory.

- There is a progression with every language feature where you at first have to explicitly say out loud every symbol to type like "student dot name space equals space double quote Steve quote" and you slowly can start using higher level instructions like "assign the literal string Steve to student dot name" until you are pair programming with the student with statements like "let's set the student's name to Steve for now". Sometimes there will be a regression as well. Don't worry, but just be more verbose and a little annoying and it'll correct itself.

- Don't worry about Git. Introduce it, but don't let it get in the way until the advanced classes. Learn to code before version control. But get students in the habit of "git add -a && git commit && git push" at the end of every session once version control is set up.

### Coding in Javascript: Core Outcomes

The goal of this course is to practice the following topics as much as possible so that they become muscle memory before applying them in domain specific areas like web and mobile.

Mastery over these topics is proven by students being capable of using these language features unprompted to solve a problem where it is an appropriate tool for the job. An intermediate level of understanding of a topic can be shown if the student is able to code a solution to the problem and explain the solution even if prompting was required to point the student in the right direction. A basic understanding of the topic is evidenced by a student's ability to use the feature with correct syntax from being given only a high level instruction like saying "Use a for loop on the results".

- Variables: var, assignment, lookup
- Operators: arithmetic, %, comparison, equality, ===
- Conditionals: if/else, truthiness, logic, short circuit 
- Loops: for, forEach, while, nested, recursion
- Functions: arguments, return values, code reuse, abstraction
- Scope: global, local, this, lexical
- JSON Types: String, Number, Boolean, Array, Object, null, undefined
- Array, String, and Object Methods: split, join, keys, slice
- Functional Programming: map, filter, sort
- Class / Instance: class, extends, this, super, constructor, new
- Exception Handling: try, catch
- Architecture Principles: Loose Coupling, DRY, Dependency Inversion
- Debugging Techniques console.log, REPL

- async / await
- setTimeout / Task Queue
- Hoisting
- Arrow Functions
- let / const
- expressions vs statements

- Git basics
- VS Code Shortcuts: block commenting, find, go to line

- Math
- Date

### Coding in Javascript: Asynchronous Programming

Asynchronous programming deserves special attention.

#### Level 1: async / await

Motivation: fetch

Just use async/await. Use modules and import/export so that async is less of a problem. Don't worry about race conditions. Never use "then". Simple rule based approach:

- If a function returns a promise put await in front of a call to it. That expression will now evaluate to whatever the promise resolves to sometime in the future.
- When you use await put async in front of the closest function or () =>.
- Use try/catch for exception handling, and you can catch the error thrown when the promise is rejected.

#### Level 2: Task Queue

Motivation: Autocomplete

Race conditions. Deck of cards metaphor. Really explain how async/await and promises work.

#### Level 3: All Other Roads Lead to Callback Hell

Motivation: File Upload

So many callback patterns in the wild. Be honest how much of a mess it is, but emphasis using async/await wherever possible.

- Promises / then, catch
- last argument callback pattern with error
- File upload
- setTimeout
- nodejs pipes
- express middleware


### Coding in Javascript: Text Coding Exercises
- 10 programming lessons
- Hello World
- Fizz Buzz
- Print sum of squares
- Banner Printing
- Guess the number
- Bowling Scorer
- warrior.js
- Roman Numerals
- Chatbot
- Project: Text Adventure Game

### Coding in Javascript: Visual Coding Exercises
- Dice
- Pong
- Fish Bowl (flock/particles)
- Visualized Sorting and Pi
- Tic Tac Toe
- Project Arcade Game

### Coding in Javascript: Day One Lesson Plan
1) Hello, world!
> Let's dive right in and write some code.
> 
> - Open a browser tab
> - Press F12 to open the developer tools
> - Open the Console tab
> - At the prompt, type: console.log('Hello, world!')

2) Coding in 10 Lessons
https://aurifexlabs.com/learn/programming.html

3) The Four Major Tools
- Variables (state, scope, data, JSON)
- Conditionals (if, else, switch, logic and comparison operators)
- Loops (iteration, for, forEach, while, cursors, recursion)
- Abstraction (temporary variables, functions, classes)

4) For next time:
> Write a function that simulates rolling two dice 100 times and prints the distribution of the sum of the two dice

### Frontend Web Development: Core Outcomes
- HTML Basics
- CSS Basics
- DOM Manipulation
- Event Listeners
- Query Selectors
- Web Components
- Model-View-Controller Concept
- Single Page Application Pattern
- Response Design
- Style Strategy: Cube CSS
- fetch and third party API use
- MDN and API docs

### Frontend Web Development: Projects
- 7 web dev lessons
- Hello World
- Weather app (or similar)
- Parse engineering text file -> JSON -> display
- Upload file -> ML classification
- Styled portfolio page
- Use third-party APIs - Sports / Animal Pictures / Weather / Flights / list of colleges

### Backend Engineering for Web: Core Outcomes
- node.js / npm
- HTTP
- Routing (Express)
- Environment Variables
- REST
- MongoDB basics
- CAP Theorem
- ACID vs BASE
- Linux environment
- Invoking scripts with child_process
- Authentication and Authorization
- Production deployment

### Backend Engineering for Web: Projects
- Authenticated App
- REST API
- Capstone Project

### Mobile App Development: Core Outcomes

Mostly it's the same as web with React Native replacing HTML/CSS.

Plus:
- React Native / Android Studio Toolchain
- Java Basics (classes and import)
- Gradle / Android SDK Manager
- Android Manifest (permissions)
- Android Deployment and Test

### Mobile App Development using React Native: Notes

#### General Tips
- Mobile is a lot more about config and x-platform build issues
- Pick only 1 or 2 native features

#### Dev Environment Setup Tips
- Follow the React Native setup instructions
- Check all the environment variables
- be sure gradlew has +x permissions

### Embedded Systems: Core Outcomes
- State Machines
- RTOS (Tasks/Queues)
- Debugging
- Garbage Collection and real time deadlines
- Boot firmware
- Using blackbox firmware (vendor supplied)
- Module init / run pattern
- IC2, UART, SPI, JTAG
- Reading Datasheets
- BOM cost and supply chain -> Heroics
- Using Dev Boards
- Signal conditioning
- Build Systems
- Simulators
- Hardware-in-the-Loop Testing
- Basic Circuits (LRC model)
- RC delay (long wires have high C)
- PCB Design concepts
- ADC/DAC concepts
- Basics of V=IR and P=IV
- Input/Output Impedence
- Power and Boot
- Audio Circuits
- Debounce
- Using Edge TPUs with PyTorch
- Memory and Code Size Contraints
- Hard Real-Time Systems (interrupts/timers/RTOS)
- Pre-allocated buffers
- Deterministic Memory Management (no malloc after boot)
- No cost / Low cost abstractions (metaprogramming)
- OTA updates
- Trustzone
- Memory Ownership (pony types)

### Embedded Systems: Projects
- Hello, World! via UART
- Blink LED
- Read Temp Sensor
- Hello, Triangle!
- Temp Graph to Display
- Send temp data to cloud
- Add a button
- Pressing the button should cycle through views
- Firmware update
- Emulate a gas sensor using a Raspberry PI and Python
- Write a full E2E HIL test

For the capstone project, start with [this example project](https://github.com/steve-aurifexlabs/mixing-tank-controller) for an example architecture.

### ML: Core Outcomes
- PyTorch Basics
- Neural Network Basics
- Layers / Deep Neural Nets
- Gradient Descent
- Tensors
- Convolutional Neural Nets (CNN)
- Classification / Detection
- Transfer Learning
- Standard Data / Models (ImageNet/ResNet)
- Recurrent Neural Nets (RNN)
- Reinforcement Learning (RL)
- Generative Adversarial Networks (GAN)
- RL from Human Feedback (RLHF)
- Linear Algebra
- Statistics
- Hyperparameter Tuning
- Experiment Design
- Cloud Training
- Edge Inference
- Hardware / Power / Cost Calculations

### ML: Projects
- Food Classifier (CNN)
- Household object detector (CNN)
- Command Detector (RNN)
- Phoneme Detector (RNN)
- Parser (RNN)
- Map Generator (DCGAN)
- Gym/Controls (RL)
- Hex AI (RL)
- Chatbot (RLHF)
- Speech Synthesizer (mixed)
- Datasheet Analyser (mixed)
- Circuit Generator (mixed)

### Semiconductor: Core Outcomes
- Digital Design Basics
- Nand Logic
- Registers
- Clock
- Reset
- Power
- Delay
- Low-Power Design
- Verilog Basics
- Parameterization
- Code Generation
- Place and Route
- Static Timing Analysis
- Memory
- I/O
- State Machines
- Fast Adders
- Multipliers
- Muxes -> False/Multicycle Path Removal
- Bus Design
- Memory Hierarchy Design
- Clock Domains
- Pipelining
- RISC
- Formal Verification
- Functional Verification
- Design for Test
- Post-Si Debug
- Process
- PDKs

### Semiconductor: Projects

- ALU
- SPI Controller
- CPU Control Unit
- Systolic Array
- ALU (optimized adder)
- Multiplier
- Bus
- Full SoC
- ISA Design
- ASIC