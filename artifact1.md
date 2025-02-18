## Artifact 1: Narrative

**Artifact Description:**

This artifact is a jukebox playlist application developed during my CS-310 Collaboration and Team Project course (October 2024 -   December 2024).  Its purpose is to create and manage a playlist of songs from various musical artists. The core functionality revolves around the `studentPlaylist()` method, which constructs a LinkedList of `PlayableSong` objects and populates it with tracks from different bands. This project was a collaborative effort utilizing a BitBucket repository.

**Justification for Inclusion:**

This jukebox playlist application is a valuable addition to my ePortfolio because it demonstrates several crucial software development skills, making it a strong example of my abilities in code improvement, error handling, and adherence to best practices.  The project showcases my ability to not only write functional code but also to refine and enhance existing codebases, making them more robust, maintainable, and efficient.

**Showcased Skills and Abilities:**

*   **Code Refactoring and Design:** The transformation of the initial code into a more structured, maintainable, and robust version showcases my ability to improve existing codebases.  The introduction of the `addSongsFromBand()` helper method to eliminate redundant code exemplifies effective design principles.
*   **Defensive Programming and Error Handling:** The implementation of boundary checks and handling for null/empty lists demonstrates a proactive approach to preventing common errors like `IndexOutOfBoundsException` and `NullPointerException`.  The inclusion of informative output messages for null or empty song lists enhances the user experience by providing clear feedback.
*   **Coding Standards:** Consistent formatting and adherence to naming conventions throughout the codebase underscores my commitment to coding best practices and producing readable, maintainable code.

**Improvements Implemented:**
The artifact was significantly improved through the following enhancements:

*   **Elimination of Redundant Code:** The `addSongsFromBand()` method consolidated repeated code blocks, resulting in a more concise and efficient implementation.
*   **Prevention of Exceptions:** The addition of boundary checks and null/empty list handling mitigates the risk of runtime exceptions, ensuring greater application stability.
*   **Improved Code Structure and Readability:** Consistent formatting, meaningful naming conventions, and the introduction of the helper method significantly enhanced the code's overall structure and readability, making it easier to understand and maintain.
*   **Enhanced Error Handling:**  The inclusion of output messages for handling null or empty song lists provides valuable feedback to the user, improving the overall user experience.

**Course Outcome Alignment:**
The enhancements implemented directly address the following course outcomes:

*   **Course Outcome #3:** *Design and evaluate computing solutions that solve a given problem using algorithmic principles and computer science practices and standards appropriate to its solution while managing the trade-offs involved in design choices.* The refactoring and design improvements clearly demonstrate my ability to meet this outcome.
*   **Course Outcome #4:** *Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals.* The application of established coding practices and defensive programming techniques showcases my proficiency in this area.

**Reflection on the Enhancement Process:**
The process of enhancing and modifying this artifact provided valuable insights into the importance of code reviews.  Initially, I struggled to identify areas for improvement.  However, using a code review checklist provided a new perspective, revealing opportunities for refactoring and enhancement.  This experience underscored the value of viewing code through a different lens.  The refactoring process, aimed at removing redundancy and improving structure, became clear after this shift in perspective.  Furthermore, implementing boundary checks and null/empty list handling reinforced the crucial role of defensive programming in building robust and reliable software.  Overall, this enhancement process was a valuable learning experience that solidified my understanding of good coding practices and provided practical application of software engineering principles.

## List of Enhancements

**Testing Enhancements:**

*   **Added Test File:** A dedicated test file was created to verify the correct functionality of artist album size checks.
*   **Artist-Specific Tests:** Three new tests were implemented, one for each artist (Metallica, Sleeping with Sirens, and Stray Kids) whose songs I contributed to the playlist.  These tests ensure that the artists' songs are being added to the playlist as expected.

**Error Handling Enhancements:**

*   **Exception Handling in `studentPlaylist()`:**  A `try-catch` block was added to the `studentPlaylist()` method to gracefully handle potential exceptions during playlist creation.  This prevents unexpected program crashes due to issues accessing song data from the `get[Band]Songs()` methods.
*   **Error Logging:**  Within the `catch` block, error messages are now printed to the standard error stream (`System.err.println()`).  This provides valuable logging information for developers and users to diagnose and resolve errors.
*   **Enhanced `addSongsFromBand()` Error Handling:** The `addSongsFromBand()` method now includes checks for `null` and empty song lists returned by the `get[Band]Songs()` methods. This prevents `NullPointerExceptions` and provides informative warning messages. Specific error messages are now included for both null and empty list cases, improving debugging.

**Code Readability and Maintainability Enhancements:**

*   **Javadoc Comments:**  Comprehensive Javadoc comments were added to the class and its methods, providing clear documentation of their purpose and functionality.
*   **Consistent Formatting:**  The code was reformatted for consistency, improving readability and making it easier to follow the logic.
*   **Meaningful Method Names:**  Method names were made more descriptive and accurately reflect their purpose.
*   **Redundant Code Removal:**  Redundant code related to creating and adding songs was eliminated, making the code more concise and efficient.

**Code Structure Enhancements:**

*   **Improved Code Structure:** The `studentPlaylist()` method is now focused solely on playlist creation, while the `addSongsFromBand()` method handles the logic for adding songs from a specific band. This separation of concerns significantly improves code organization and maintainability.
