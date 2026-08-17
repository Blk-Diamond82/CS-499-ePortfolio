# Enhancement Three: Databases

## Travlr Getaways Full-Stack Application

### Artifact Description

The artifact selected for this enhancement is the Travlr Getaways full-stack web application originally developed in CS 465, Full Stack Development. The application uses a JavaScript-based full-stack architecture with an Express API, MongoDB database, Mongoose object data modeling, and an Angular administrative interface.

I selected the Trip data model and its supporting API operations for Enhancement Three because the database layer is responsible for preserving the accuracy and consistency of the trip information used throughout the application.

## Justification for Inclusion and Enhancement

I included this artifact in my ePortfolio because it demonstrates my ability to work with a persistent NoSQL database as part of a complete application rather than treating the database as an isolated component.

The original artifact already stored and retrieved trip records through MongoDB and Mongoose. For the CS 499 enhancement, I strengthened the way the application defines, validates, retrieves, creates, and updates those records.

The enhanced Trip schema establishes stronger data requirements and database integrity rules. Trip codes are protected by a uniqueness constraint and index, while required-field validation prevents incomplete trip records from being accepted.

I also improved the API controller logic so database conditions are communicated through meaningful HTTP responses:

- Missing records return `404 Not Found`.
- Invalid or incomplete trip data returns `400 Bad Request`.
- Attempts to create a duplicate trip code return `409 Conflict`.
- Unexpected server conditions remain distinguishable from expected validation and database conflicts.

An important improvement was extending duplicate protection to update operations as well as creation. During testing, I attempted to update the existing `MTN01` record so that its code became `SEA01`, which was already assigned to another trip.

MongoDB rejected the operation through its unique index with duplicate-key error code `11000`. I updated the controller to recognize that database error and return a `409 Conflict` response with a message explaining that a trip with that code already exists.

This demonstrates that the database itself enforces the integrity rule even when an update attempts to introduce a duplicate value.

## Course Outcome Coverage

This enhancement substantially supports Computer Science Program Outcome Four:

> Demonstrate an ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals.

MongoDB, Mongoose, Express, schema validation, database indexing, asynchronous controller operations, and HTTP status handling were used together to create a more reliable persistence layer.

The enhancement also contributes to Outcome Three because I had to evaluate where data rules should be enforced. Application-level checks can provide an understandable response before an operation is attempted, while a database-level unique index provides stronger protection because the integrity constraint remains in effect at the persistence layer.

Using both approaches created a more robust solution and demonstrated the trade-off between user-friendly application logic and authoritative database enforcement.

I also made progress toward Outcome Five involving a security mindset. Although this enhancement was not primarily an authentication or cybersecurity feature, protecting database integrity is part of securing application data. Required fields, controlled updates, uniqueness constraints, and predictable error handling reduce the possibility of malformed, duplicate, or inconsistent records entering the system.

Based on the completed enhancement, I do not need to change my overall outcome-coverage plan. However, I can now provide stronger evidence for Outcomes Three, Four, and Five in my final ePortfolio.

## Reflection on the Enhancement Process

The most important lesson from this enhancement was that database reliability requires more than successful CRUD operations.

At first, it was possible to view duplicate checking as a controller-level problem. Testing demonstrated why the database must also enforce the rule. When I intentionally attempted to reuse `SEA01` during an update, MongoDB correctly generated a duplicate-key error.

The first version of the controller treated that error as a generic server failure and returned a `500` response. Examining the terminal output showed error code `11000` and identified the unique code index as the source. I modified the update error handling so that this expected database conflict became a meaningful `409 Conflict` response instead.

Another challenge was ensuring that the model, controller, routes, and test requests remained consistent as the enhancement became more restrictive. Required fields caused intentionally incomplete requests to return `400 Bad Request`, while duplicate records returned `409 Conflict`. These results helped distinguish validation failures from uniqueness conflicts and true server errors.

Testing the endpoints in Postman allowed me to verify behavior from the API boundary instead of assuming that a schema change worked simply because the code compiled.

Overall, the enhancement changed how I think about database design in a full-stack application. I learned to treat the schema as an enforceable contract for persisted data, not simply a description of document fields. I also gained a better understanding of how database errors should be translated into API responses that are useful to the client.

The resulting artifact is more reliable, maintainable, and defensible as professional-quality work because its data rules are enforced at multiple layers and were verified through deliberate positive and negative testing.

---

[Return to ePortfolio Home](README.md)
