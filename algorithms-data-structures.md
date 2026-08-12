# Enhancement Two: Algorithms and Data Structures

## Artifact Description

The artifact selected for this enhancement is the Travlr Getaways Full Stack web application, originally developed during CS 465: Full Stack Development with MEAN. The application was developed throughout the course using MongoDB, Express, Angular, and Node.js to create both a customer-facing travel website and an administrative single-page application.

For this milestone, I used the Module Six version of the Travlr application as the original artifact. At this stage of the original project, the Angular administrative interface retrieved trip information from the REST API and displayed the available trips using reusable Angular components. While the application successfully retrieved and displayed the data, the administrator had limited ability to organize or locate specific trip information.

For my enhancement, I added searching, filtering, and sorting functionality to the Angular trip list. Administrators can now search the available trips and dynamically reduce the displayed results based on the entered search criteria. I also added sorting options that allow trips to be organized alphabetically, by start date, or by price in ascending or descending order. A result counter provides immediate feedback about how many trips match the current criteria, and a Clear function resets the search and sorting controls.

## Justification for Inclusion in the ePortfolio

I selected the Travlr application again because it allows me to demonstrate how an existing application can be improved instead of creating functionality that is disconnected from the rest of my ePortfolio. The original Module Six application already contained a working Angular SPA, making it a good foundation for demonstrating how algorithms can improve the way users interact with application data.

The original trip list essentially displayed the data in the order it was received from the API. This works with a small number of trips, but it becomes less practical as the amount of information increases. An administrator should not have to manually scan an entire collection to locate a particular trip.

The enhanced version processes the trip collection based on user-selected criteria before displaying the results. Search logic evaluates trip information against the administrator's search term, while sorting logic compares records according to the selected field. The application can reorganize trips alphabetically, chronologically, or numerically depending on the administrator's needs.

I also made an intentional design decision to preserve the original trip data rather than repeatedly modifying the source array during sorting. This keeps the retrieved API data separate from the processed collection displayed by the interface and reduces the possibility of creating unintended side effects.

The enhancement includes:

- Dynamic searching and filtering of trip data
- Sorting trips alphabetically by name
- Sorting trips by start date
- Sorting trips numerically by price from low to high or high to low
- Combining filtering and sorting so both operations can be applied to the same collection
- Displaying the number of matching trips
- Providing a Clear function that resets the search and sorting criteria
- Continuing to use reusable Angular components to render the processed trip collection

These improvements demonstrate how relatively simple algorithms can significantly improve the usability and efficiency of an application.

## Course Outcomes Achieved

This enhancement most directly supports the Computer Science program outcome of designing and evaluating computing solutions using algorithmic principles and computer science practices while considering the trade-offs involved in design choices.

Rather than simply adding another visual feature to the application, I had to determine how the trip collection should be processed and how multiple operations should interact. The application must first determine which records satisfy the search criteria and then organize those results according to the selected sorting method. This required me to think about the sequence of operations and how the data should move through the application before being presented to the user.

The enhancement also demonstrates progress toward implementing computing solutions using appropriate tools and software engineering practices. The algorithmic functionality was integrated into the existing Angular architecture rather than being implemented as unrelated code. Angular signals allow changes in search and sorting criteria to update the interface dynamically while maintaining the application's component-based structure.

My outcome coverage remains consistent with the plan established earlier in CS 499. This enhancement provides stronger evidence for the algorithms and data structures outcome, while the previous enhancement focused primarily on software design and engineering. The remaining enhancement will provide additional evidence of my skills in database development.

## Reflection

Completing this enhancement helped me better understand that algorithms do not always have to involve extremely complicated calculations. Before working through this enhancement, I often associated algorithms with larger or more abstract programming problems. This project showed me that algorithms are also present in everyday application functionality such as searching, filtering, sorting, and organizing information for a user.

One of the most useful parts of this enhancement was seeing the immediate effect of the logic I implemented. When I entered part of a trip name or other searchable information, the application reduced the displayed collection to the matching trip. When I changed the sorting option, I could immediately see the trip cards reorganized by name, date, or price. Testing these functions helped connect the code directly to the behavior of the application.

I also learned more about the importance of considering how operations work together. Searching and sorting individually were straightforward, but the application needed to produce predictable results when both were active. The data first had to be filtered based on the search criteria and then sorted according to the administrator's selection. Adding the result count and Clear function also made me think beyond whether the algorithm technically worked and whether the user could easily understand and control what the application was doing.

The biggest challenge was integrating the new logic without interfering with the existing API retrieval and Angular components. I wanted to improve the application while preserving the functionality that was already working. Working through that process strengthened my ability to modify existing code carefully instead of rebuilding working functionality unnecessarily.

Overall, this enhancement represents another stage in my growth as a computer science student. The original application could retrieve and display trip information. The enhanced application can now process that information based on user-defined criteria and return a more useful result. That difference demonstrates how algorithms and data structures can improve not only the technical functionality of an application but also the experience of the person using it.

---

## Artifact Files

The original and enhanced versions of the Travlr application demonstrate the progression of the artifact before and after the Algorithms and Data Structures enhancement.

- **Original Artifact:** [Download Original Travlr Application](PASTE-ORIGINAL-ZIP-FILENAME-HERE)
- **Enhanced Artifact:** [Download Enhanced Algorithms and Data Structures Application](PASTE-ENHANCED-ZIP-FILENAME-HERE)

[Return to ePortfolio Home](README.md)
