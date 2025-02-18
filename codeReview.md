## Code Review

### I. Category One: Software Engineering and Design

**Provide a clear, complete description of existing code functionality.**

*What does the code do?*

The `DominickMarquez_Playlist` class is designed to create a playlist of songs from different artists (e.g., Metallica, Sleeping With Sirens, and Stray Kids). The `studentPlaylist()` method creates a `LinkedList` of `PlayableSong` objects and populates it with a few songs from each band, retrieved using band-specific methods like `getMetallicaSongs()`.

**Analyze existing code using relevant code review criteria to support clearly stated findings.**

*Code Review Checklist:*

*   Code is not consistently formatted (indentations are off).
*   `studentPlaylist()` method name is inconsistent (should be camelCase).
*   Variable names are not consistent (should be camelCase).
*   Repeated code (adding songs from each band is very similar, violating the DRY principle).
*   Unnecessary variable declaration (`StrayKids` variable is declared but never used; the correct variable is `StrayKidsTracks`).
*   No error handling (lack of null checks and bounds checks).
*   Magic numbers/hardcoded indices (using `get(0)`, `get(1)` assumes bands always have at least two songs, which can lead to `IndexOutOfBoundsException`).
*   Missing thoughtful comments.

*Target Areas for Improvement:*

*   Structure (variables, methods)
*   Defensive programming (error handling, boundary checks)
*   Code reusability (DRY principle)
*   Code readability and maintainability (formatting, comments)

**Explain practical enhancements aligned with analysis findings in a clear and organized manner.**

*Say what you plan to do in your enhancement. What specific skills will you demonstrate, and which of the five course outcomes will your enhancements support?*

*Course Outcomes:*

1.  Employ strategies for building collaborative environments...
2.  Design, develop, and deliver professional-quality...communications...
3.  Design and evaluate computing solutions...managing the trade-offs...
4.  Demonstrate an ability to use...tools...in computing practices...
5.  Develop a security mindset...

*Plan:*

I will enhance the playlist Java file by:

1.  **Formatting:** Fixing the code formatting, ensuring consistent indentation.
2.  **Naming Conventions:** Ensuring consistent camelCase naming for methods and variables.
3.  **Code Reusability:** Implementing a private helper method to encapsulate the logic for adding songs from a band, reducing code duplication.
4.  **Defensive Programming:** Adding boundary checks using `Math.min` in the `addSongsFromBand()` method to prevent `IndexOutOfBoundsException`.  Adding null and empty list checks in the `getSongs` methods with user-friendly error messages.
5.  **Variable Correction:** Removing the unused `StrayKids` variable and replacing it with the correct `strayKidsTracks` variable.
6.  **Documentation:** Adding well-thought-out Javadoc comments to improve code understanding and reusability.

*Specific Skills Demonstrated:*

*   Code formatting and style
*   Code refactoring and reusability
*   Defensive programming
*   Variable management
*   Software engineering principles

*Course Outcomes Supported:*

*   **Outcome #3:** The error-handling enhancements improve the robustness of the solution.
*   **Outcome #4:** The refactoring and improvements demonstrate good coding practices.

### II. Category Two: Algorithms and Data Structures

**Provide a clear, complete description of existing code functionality.**

*What does the code do?*

The Java slideshow application displays a series of vacation destinations (top-five list), with each destination on a separate "slide."  Each slide includes an image, a short description, image credits, and navigation buttons. The application uses Swing components, and the original code used a series of `if-else` statements to manage image paths and descriptions.

**Analyze existing code using relevant code review criteria to support clearly stated findings.**

*   **Inefficient Data Handling:** The `if-else` structure is not scalable or efficient.
*   **Code Redundancy:** The `if-else` structure leads to repetitive code.
*   **Limited Maintainability:** The `if-else` structure makes the code harder to read and modify.
*   **Lack of Clear Data Separation:** Image path retrieval and HTML string construction are intertwined.
*   **Missing Error Handling:** No checks for empty or missing image paths.
*   **Inconsistent Naming:** Variable and method names could be improved.
*   **Limited Comments:**  Insufficient comments.

**Explain practical enhancements aligned with analysis findings in a clear and organized manner.**

*Course Outcomes:* (Same as above)

*Plan:*

I will refactor the Java slideshow application to use a `HashMap` to store the mapping between image indices and file paths, replacing the `if-else` structure.  I will use `Map.of()` for concise `HashMap` creation. I will separate image path retrieval from HTML construction.  I will add a check for empty image paths and improve comments.

*Specific Skills Demonstrated:*

*   Data structure selection and implementation
*   Code refactoring and optimization
*   Error handling
*   Code readability and maintainability
*   Object-oriented programming principles

*Course Outcomes Supported:*

*   **Outcome #2:** Improved code, comments, and UI contribute to professional communication.
*   **Outcome #3:** The `HashMap` choice demonstrates consideration of computing solutions and trade-offs.
*   **Outcome #4:** The project uses modern Java libraries and techniques.

### III. Category Three: Databases

**Provide a clear, complete description of existing code functionality.**

*What does the code do?*

The AAC Dashboard is an interactive web application built with Python, Dash, MongoDB, and Jupyter Notebook. It visualizes data from the Austin Animal Center's database, providing insights into animal breeds, demographics, and locations. The dashboard features a sortable and filterable data table, interactive charts (pie chart), and a map.

**Analyze existing code using relevant code review criteria to support clearly stated findings.**

*   **Deprecated Code:** Uses deprecated libraries/methods (`jupyter_dash`, `app.run_server`).
*   **Inconsistent Styling:** Inconsistent styling across elements.
*   **Limited Error Handling:** Error handling could be more robust.
*   **Responsiveness Issues:** Responsiveness across screen sizes needs improvement.
*   **Chart Enhancements:** Charts could be enhanced (titles, labels, empty data handling).
*   **Map Enhancements:** Map integration could be improved (missing/invalid data handling, popups, data indexing).
*   **Code Comments:** More detailed comments are needed.
*   **Layout Issues:** Chart and map layout needs adjustment.

**Explain practical enhancements aligned with analysis findings in a clear and organized manner.**

*Course Outcomes:* (Same as above)

*Plan:*

I will enhance the AAC Dashboard by:

1.  Removing deprecated code.
2.  Improving error handling.
3.  Enhancing responsiveness using Bootstrap.
4.  Improving chart styling and data handling.
5.  Enhancing map integration.
6.  Improving code comments.
7.  Fixing layout issues.

*Course Outcomes Supported:*

*   **Outcome #1:** Enhancements will make the dashboard a more effective decision-making tool.
*   **Outcome #2:** Improved code, error handling, responsiveness, and documentation contribute to a professional deliverable.
*   **Outcome #3:** Enhancements demonstrate my ability to evaluate and improve a computing solution.
*   **Outcome #4:** The project uses industry-standard tools and the enhancements demonstrate effective application.
*   **Outcome #5:** Implementing least privilege demonstrates understanding of security best practices.
