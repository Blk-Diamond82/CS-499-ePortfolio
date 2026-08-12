# Enhancement One: Software Design and Engineering

## Travlr Getaways Full Stack Application

### Artifact Description

The artifact I selected for this enhancement is the Travlr Full Stack web application, which I originally developed during CS 465: Full Stack Development with MEAN. Throughout the course, this project was built in stages to demonstrate the development of a full stack web application using Node.js, Express, Handlebars, MongoDB, and Mongoose.

For this milestone, I used the Module Three version of the project as my original artifact. At that stage, I had successfully converted the static HTML pages into dynamic Handlebars templates that displayed trip information from a local JSON file.

For this enhancement, I focused on the work completed in Module Four, where I redesigned the application's data layer by replacing the JSON file with a MongoDB database using Mongoose models and schemas.

This enhancement was an important step because it changed the application from simply displaying static data to using a real database, creating a stronger foundation for the REST API and Angular application that were developed later in the course.

## Justification for Inclusion in the ePortfolio

I selected this artifact because it demonstrates one of the biggest improvements I made as a software developer during this program. Instead of simply showing a completed application, it highlights how my design decisions evolved as I learned better software engineering practices.

In the original version of the project, trip information was stored in a static JSON file. While this worked for rendering data dynamically with Handlebars, it would not be practical for a real-world application where information needs to be added, updated, or managed efficiently. Replacing the JSON file with MongoDB allowed the application to become much more scalable and maintainable.

This enhancement also introduced several software engineering concepts that were new to me at the time. I created a dedicated database connection using Mongoose, designed a reusable Trip schema, migrated the existing trip data into MongoDB, and separated the presentation layer from the data layer.

By accessing information through a model instead of directly reading from a file, the application became much easier to maintain and positioned it for future enhancements, including RESTful APIs and the Angular administrative interface. Looking back, this was the point where the project started feeling like a true full stack application instead of a collection of web pages.

## Course Outcomes Achieved

This enhancement demonstrates meaningful progress toward several Computer Science program outcomes identified during Module One.

The outcome that is most evident is my ability to implement computing solutions using sound software engineering techniques and tools. Replacing local file storage with MongoDB and Mongoose improved the overall architecture of the application and aligned it more closely with industry standards for modern web development.

This enhancement also supports the outcome of designing and evaluating computing solutions by reducing the dependency between the user interface and the application's data source. Separating these responsibilities created a cleaner architecture that is easier to maintain, test, and expand.

Although later milestones focus more heavily on APIs, security, and Angular development, this enhancement established the foundation that made those improvements possible. It represents the transition from building a functional website to developing a scalable software solution.

## Reflection

This enhancement helped me realize how important application architecture is in software engineering. When I first built the project, storing trip information in a JSON file seemed like the simplest solution because it allowed me to focus on learning MVC routing and dynamic page rendering. As the project continued to grow, I began to understand why professional applications rely on databases instead of static files.

Migrating to MongoDB changed the way I thought about managing data. Instead of simply reading information from a file, I learned how schemas and models provide structure, validation, and consistency across an application. I also developed a much better understanding of how Express, Mongoose, and MongoDB work together as part of a full stack architecture.

One of the biggest challenges during this enhancement was configuring the database connection and making sure the application was pulling data from MongoDB instead of the original JSON file. Troubleshooting those issues required patience and a lot of testing, but it also strengthened my debugging skills and gave me more confidence working with backend technologies.

Looking back, I see this enhancement as the point where I started thinking more like a software engineer. Rather than simply making the application work, I began making design decisions based on scalability, maintainability, and future development. Those lessons were carried forward into the remaining milestones, where I expanded the project with RESTful APIs, Angular, and JWT authentication to create a complete full stack application.

## Artifact Files

The original artifact demonstrates the Module Three implementation of Travlr Getaways using Handlebars templates and local JSON data.

**[View Original Artifact - Module Three](<Travlr_Original_Module 3 (1).zip>)**

The enhanced artifact demonstrates the Module Four implementation using MongoDB and Mongoose for persistent data storage.

**[View Enhanced Artifact - Module Four](<Travlr_Enhancement_Module 4 (1).zip>)**

---

[Return to ePortfolio Home](./)
