# CS 230: Operating Platforms

This repository contains the software design documentation for **Draw It or Lose It**.

## Client and Requirements

The client for this project was **The Gaming Room**, a game studio that originally created Draw It or Lose It as a mobile-only application for Android. They wanted to expand the game into a **web-based application** that could run on multiple platforms (Windows, Mac, Linux, and mobile devices) while still meeting their original game rules.

Draw It or Lose It is a team-based guessing game inspired by the 1980s show *Win, Lose or Draw*. The system renders images from a library of stock drawings as clues, and players try to guess the puzzle before time runs out. The client's main software requirements were:

- A game can have one or more teams.
- Each team can have multiple players.
- Game names and team names must be unique.
- Only one instance of the game can exist in memory at any given time.

## Project Reflection

### What I did well

I think I did a good job at structuring the document in a clear, organized way and making sure each section connected to the next. The Executive Summary and Design Constraints set up the problem, the Domain Model and UML explained the architecture, and the Evaluation and Recommendations sections built on top of that to justify the chosen platform. I also made sure to base my recommendations on real research instead of just opinions, and I included references to back up the technical claims.

### How the design document helped with the code

Working through the design document first was really helpful because it helped me to have a better picture of how the application should be built. One of the most important parts was the UML diagram and Domain Model section which contains the base for the code implementation. Even though this repo only contains the documentation, going through the design process step by step is what makes the eventual code easier to write, because the structure, relationships, and design patterns are already worked out before a single line of code is written.

### What I would revise

If I could go back and revise one part, it would be the **Evaluation** section. I would improve it by either breaking each cell into shorter bullet points (advantages, weaknesses, cost) or adding a small summary row at the bottom that highlights the winner of each category. That would make the comparison much easier to read and would make the link to my final recommendation more obvious.

### Interpreting user needs

I interpreted the client's needs by carefully reading the original problem description and pulling out the specific requirements (unique names, only one game instance, support for multiple teams and players). Then for each design decision I made, I checked it against those requirements. For example, the Singleton pattern on GameService directly answers the "only one instance" rule.

Considering the user's needs is so important because the software exists to solve their problem. If I had built the most technically impressive system but ignored what the client actually asked for, the project would have failed even if the code worked perfectly.

### Software Design Approach

My approach was to start broad and then get more specific. First I made sure I understood the problem and the client's requirements. Then I looked at the existing UML diagram and identified the object-oriented principles. After that I evaluated the platforms, picked the one that best fit the requirements, and explained how the operating system would actually support the application at runtime (memory, storage, networking, security).

For future projects, I would use a similar approach:

- **Start with the requirements in writing.** Even a short bulleted list helps to understand what success looks like before any choices are made.
- **Sketch the UML or domain model early.** Drawing the classes and relationships before coding makes it much easier to spot missing pieces.
- **Identify the design patterns that fit the problem**
- **Evaluate trade-offs explicitly.** Every platform or tool choice has pros and cons, and writing them down helps justify the final pick.
- **Plan for non-functional requirements** like scalability, security, and reliability from the start.
