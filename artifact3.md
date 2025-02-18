## Artifact 3: Narrative

**Artifact Description:**

This artifact is an interactive web application, the Austin Animal Center (AAC) Dashboard, initially developed as the final project for my CS 340: Client-Server Side Application course (July 2024 - August 2024).  The dashboard aims to streamline the process of identifying suitable dogs for search-and-rescue training based on data from five animal shelters. Built using Python, Dash, MongoDB, and Jupyter Notebook, it visualizes data from the Austin Animal Center's animal shelter database, providing insights into animal breeds, demographics, and locations.  Key features include a sortable and filterable data table, interactive charts (including a pie chart for breed distribution), and a map displaying the location of selected animals.

**Justification for Inclusion:**

This project is a significant demonstration of my software development skills and abilities, showcasing the practical application of concepts learned in CS-340.  It goes beyond simple code examples to create a functional and informative tool.

**Showcased Skills and Abilities:**

*   **Data Handling and Processing:** The dashboard demonstrates proficiency in retrieving, processing, and manipulating data from a MongoDB database.  The use of Pandas DataFrames for structuring and cleaning data, including handling missing or inconsistent data (such as the `_id` column), highlights my data manipulation skills.
*   **Web Application Development:** Building the dashboard with Dash showcases my ability to create interactive web applications.  The use of Dash components (tables, graphs, maps) and callbacks to manage user interactions demonstrates understanding of front-end and back-end web development principles.
*   **Data Visualization:** The pie chart and interactive map effectively visualize data, demonstrating my ability to choose appropriate visualization methods and use libraries like Plotly and Dash Leaflet.
*   **Responsive Design:** The responsive layout adapts to different screen sizes, demonstrating understanding of responsive design principles and the use of Bootstrap for styling.
*   **Code Structure and Organization:** The well-structured code, with clear separation of concerns (data access, layout, callbacks), demonstrates my ability to write clean and organized code.

**Artifact Improvements:**

The dashboard was significantly improved through the following enhancements:

*   **Code Cleanup:** Removed deprecated code (jupyter_dash, app.run_server), cleaned up FIX ME comments, and improved code comments for clarity.
*   **Error Handling:** Enhanced `update_dashboard()`, `update_graphs()`, and `update_map()` with `try/except` blocks to prevent application crashes due to data issues or unexpected errors. Improved error messages provide more helpful debugging information.
*   **Responsiveness:** Improved responsiveness of the footer and logo/title section. Charts now resize responsively thanks to the Bootstrap grid layout.
*   **Styling:** Styled the data table header (bold, larger font) and added left margin to filtering options.
*   **Data Table Enhancements:** Added `virtualization=True` for better performance with large datasets and implemented a slider for pagination.
*   **Logo and Title:** Added a `try` block to handle potential `FileNotFoundError` for the logo and implemented a Flexbox layout for improved visual appeal and responsiveness.
*   **Chart Enhancements:** Added a title to the pie chart and handled cases where `viewData` is `None` or empty.
*   **Map Enhancements:** Added a nested `try/except` block for data conversion and validation, explicitly raising `ValueError` for invalid coordinates. Handled missing animal names by displaying "Unknown," corrected indices for accessing data, added checks for data and indices to prevent errors, and made the map width responsive. Added meaningful comments.
*   **Layout:** Fixed the layout to ensure the chart and geolocation chart are displayed side-by-side.

**Course Outcome Alignment:**

The enhancements directly address the following course outcomes:

*   **Course Outcome #1:** *Employ strategies for building collaborative environments that enable diverse audiences to support organizational decision-making...* The dashboard is designed to support organizational decision-making at the Austin Animal Center, providing insights into animal data for various purposes, including resource allocation and targeted outreach.
*   **Course Outcome #2:** *Design, develop, and deliver professional-quality...communications...* The dashboard itself is a professional deliverable. The code improvements and enhancements demonstrate my ability to communicate effectively about technical projects.
*   **Course Outcome #3:** *Design and evaluate computing solutions...managing the trade-offs...* The dashboard design and enhancements demonstrate my ability to evaluate and improve solutions based on best practices.
*   **Course Outcome #4:** *Demonstrate an ability to use...tools...in computing practices...* The use of Dash, Plotly, Dash Leaflet, and Bootstrap showcases my use of industry-standard tools and techniques.  The enhancements demonstrate my ability to apply these tools effectively.
*   **Course Outcome #5:** *Develop a security mindset...mitigate design flaws...ensure privacy and enhanced security...* The `mongodb_crud.py` file implements the principle of least privilege, limiting the database user's permissions to only those necessary for the application's functionality.

**Reflection on the Enhancement Process:**

Enhancing the AAC Dashboard was a valuable learning experience.  I gained a deeper understanding of the Dash framework and how to effectively link components for an interactive user experience.  The importance of writing maintainable code became clear when revisiting earlier iterations. Working with real-world MongoDB data and using Pandas for cleaning and transformation reinforced my data handling skills.  I also gained a better understanding of data visualization principles, learning how to choose appropriate chart types and present data effectively.

Challenges included managing the complexity of Dash callbacks, ensuring data consistency across components, and debugging interactive elements.  Maintaining data consistency between the data table, charts, and map during filtering and sorting required careful attention.  Overall, this process was challenging but rewarding, improving my web application development, data visualization, and problem-solving skills, and increasing my confidence in tackling complex projects.

## List of Enhancements

**Deprecated Code Removal:**

*   `jupyter_dash` dependency was removed as its features are now integrated into `dash`.
*   `app.run_server` was replaced with the updated `app.run` command.
*   Leftover `FIX ME` comments were cleaned up.
*   Code comments were made more meaningful and informative.

**UI and Styling Enhancements:**

*   A left margin was added to the filtering options for improved visual organization.
*   A horizontal slider was implemented for pagination in the data table, enhancing user experience.
*   The data table header was styled with bold text for better visual hierarchy.

**`update_dashboard()` Method Enhancements:**

*   **Try/Except Block:** A `try/except` block was added to catch potential errors during database queries, DataFrame creation, or column manipulation.  This prevents application crashes and provides more robust error handling.  The `except` block prints a descriptive error message using an f-string, including the specific exception type.
*   **`_id` Column Handling:** The code retains the check and removal of the `_id` column.
*   **Clearer Comments:**  Comments were refined to further clarify the function's purpose, the `try/except` block, and the handling of the `_id` column.

**`update_graphs()` Method Enhancements:**

*   **Responsive Graph Resizing:** The `style` dictionary was removed, leveraging Bootstrap's grid layout (`col-md-6`) for automatic and responsive graph resizing.
*   **Try/Except Block:** A `try/except` block was implemented to handle potential errors during data processing, such as unexpected data formats.
*   **Data Validation:** The code now checks if `viewData` is `None` or empty. This prevents errors when the DataTable has no data to display.
*   **Pie Chart Title:** A title ("Animal Breed Distribution") was added to the pie chart for improved clarity.
*   **Responsive Graph Container:** The `style` attribute was removed from the `dcc.Graph` component. This allows the graph to responsively fill its container thanks to the Bootstrap grid.
*   **Empty Data Handling:** The callback now returns an empty list `[]` if an error occurs or if there is no data to display.

**`update_map()` Method Enhancements:**

*   **Nested Try/Except Block:** A nested `try/except` block was implemented. The inner `try` block handles data conversion (e.g., `float()`) and validation (latitude/longitude range), explicitly raising `ValueError` for invalid coordinates. The outer block catches other unexpected errors.
*   **Missing Name Handling:** The code checks for missing animal names (either `None` or an empty string) and displays "Unknown" in the popup if the name is missing.
*   **Corrected Data Indexing:** The code was corrected to use the proper indices for retrieving latitude, longitude, and name data.
*   **Data Validation:** Checks for `viewData`, `dff`, and `index` were added to prevent errors.
*   **Row Index Check:** A check was added to ensure the row index is within range.
*   **Responsive Map Width:** The map width was made responsive using `style={'width': '100%', 'height': '100%'}`.
*   **Meaningful Comments:**  Meaningful comments were added to explain the method's logic.

**Logo and Title Enhancements:**

*   **Try Block for Logo:** A `try` block was added to handle `FileNotFoundError` if the logo image is not found.
*   **Image Check:** A check was added to ensure the `encoded_image` variable is not `None`.
*   **Flexbox Layout:** A Flexbox layout was implemented to improve the visual appeal and responsiveness of the logo and title section.
*   **Meaningful Comments:** Meaningful comments were added to explain the changes.

**Layout Enhancements:**

*   The code was adjusted to ensure the chart and geolocation chart are displayed side-by-side.
