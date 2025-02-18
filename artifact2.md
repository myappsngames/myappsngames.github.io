## Artifact 2: Narrative

**Artifact Description:**

The artifact selected for category two is a Java slideshow application developed during my CS 250: Software Development Life Cycle course (May 2024 - June 2024). This application serves as a vacation booking tool, presenting a top-five destination list. Each destination listing includes an image, a brief description, image credits, and navigation buttons to move between destinations.

**Justification for Inclusion:**

This Java slideshow application is a valuable addition to my ePortfolio because it showcases my foundational programming skills and demonstrates proficiency in several key areas.  It highlights my ability to apply object-oriented principles, design user interfaces, effectively manage data, and write maintainable code.  This project demonstrates my ability to translate a real-world problem (presenting vacation destinations) into a functional software solution.

**Showcased Skills and Abilities:**

*   **Object-Oriented Principles:** The application's class structure and method utilization demonstrate a solid understanding of object-oriented programming principles.
*   **Event Handling and UI Design:** The implementation incorporates event handling and user interface design using Swing components, highlighting my ability to create interactive and user-friendly applications.
*   **Data Structures:** The effective use of a HashMap for data storage and retrieval demonstrates my understanding of data structure selection and its impact on application performance.
*   **Code Refactoring:** The code has been refactored to enhance readability and maintainability, showcasing my ability to improve code quality.

**Artifact Improvements:**

The artifact was significantly improved through the following enhancements:

*   **Elimination of Redundant Code:** Refactoring the code to use `Map.of()` for map creation, reducing redundant code, and adding meaningful comments improved readability and maintainability.
*   **Data Structure Selection:** Replacing a series of `if-else` statements with a HashMap significantly improved the efficiency and maintainability of the code, demonstrating the importance of choosing appropriate data structures.
*   **Improved Code Structure and Readability:** Consistent formatting, clear naming conventions, and the addition of concise comments enhanced the code's readability, making it easier to understand and modify.

**Course Outcome Alignment:**

The enhancements implemented directly address the following course outcomes:

*   **Course Outcome #2:** *Design, develop, and deliver professional-quality oral, written, and visual communications that are coherent, technically sound, and appropriately adapted to specific audiences and contexts.* The well-structured code with clear comments and meaningful variable names represents professional-quality written communication.  The visual output of the slideshow application demonstrates my ability to design and deliver effective visual communication.
*   **Course Outcome #3:** *Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution while managing the trade-offs involved in design choices.* The selection of `CardLayout`, HashMap, and Swing components demonstrates careful consideration of appropriate computing solutions and their trade-offs.
*   **Course Outcome #4:** *Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals.* The project utilizes modern Java libraries and techniques, such as `Map.of()` and HashMaps, showcasing my ability to use current tools and methods.

**Reflection on the Enhancement Process:**

The process of enhancing this artifact was a valuable learning experience.  The initial code, relying heavily on `if-else` statements, was inefficient and difficult to maintain.  Introducing a HashMap to store image paths and descriptions highlighted the importance of selecting appropriate data structures for efficiency and readability.  This change significantly reduced code redundancy and simplified the process of adding or modifying slides.  Refactoring the code to use `Map.of()` for map creation further demonstrated the value of leveraging modern language features for improved readability and maintainability.

A key challenge was ensuring proper alignment between displayed images and corresponding text.  This required careful consideration of layout managers and UI element positioning.  Through this process, I deepened my understanding of core Java concepts, including object-oriented programming, data structures, and UI design.  I also learned the importance of code refactoring and the value of choosing the right tools and techniques to improve code quality and maintainability.

## List of Enhancements

**UI Enhancements:**

*   **Destination Description Updates:** Destination descriptions were rewritten to be more appealing and engaging for users.
*   **Layout Improvements:** The layout of destination descriptions was improved for visual appeal and is no longer off-centered.
*   **Background Color Change:** The background color of the destination descriptions was changed for better visual presentation.
*   **Padding Added:** Padding was added to the left side of the destination description text for improved readability.

**Data Structure and Algorithm Enhancements:**

*   **Data Structure:** A HashMap (`imagePaths`) was introduced to store the mapping between the image index (`i`) and its corresponding file path. This allows for efficient lookups based on the index.
*   **Reduced Redundancy:** The repetitive `if-else` blocks used in the previous version were replaced by using the HashMap to retrieve the image path.
*   **Concise HashMap Creation:**  `Map.of()` was used to create the `imagePaths` HashMap in a concise and immutable way.

**Enhanced Readability:**

*   **Updated Comments:** Comments were updated to clearly explain the purpose of each code section.
*   **Concise HashMap Population:** The code is more concise by directly creating and populating the HashMap within the method.
*   **Clearer Image Path Handling:** Image path retrieval is now separated from HTML string construction.
*   **Empty Path Check:** A check for an empty `imagePath` was added to prevent potential errors.

**Maintainability Enhancements:**

*   **Improved Maintainability:** The use of a HashMap and the `getOrDefault()` method for handling potentially missing keys enhances maintainability.
*   **Simplified Path Management:** Adding or modifying image paths is now easier by only requiring updates to the `imagePaths` map.
*   **Clear Comments:** Clear comments make the code significantly easier to maintain and modify in the future.
