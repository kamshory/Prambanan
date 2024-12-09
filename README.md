
# Prambanan: Revolutionizing Fast Application Development

## History and Introduction

Imagine a large application consisting of dozens of CRUD (Create, Read, Update, Delete) modules. Each module has the following mechanism:

1.  create new data
2.  change existing data
3.  delete existing data
4.  requires approval to create new data, change data and delete data
5.  have a rule that the user who approves the creation, change and deletion of data must be different from the user who creates, changes and deletes data
6.  Data can be exported to Microsoft Excel and CSV formats.

This project must be created in a very fast time, even less than 3 months.

In this situation, the project owner definitely needs a tool to create applications very quickly but without errors.

Prambanan is the answer to all this.

Of course. Because with Prambanan, a CRUD module that has the features mentioned above can be created in **less than 30 minutes**. Yes, you didn't read it wrong and I didn't write it wrong. 30 minutes is the time needed for developers to select columns from a module. Is the input in the form of inline text, textarea, select or checkbox and what filter is appropriate for that column. Of course, there is still plenty of time left and enough to edit the program code manually if necessary.

If a module can be created in 30 minutes, then in one day, a developer can create at least 16 new CRUD modules. Within 2 weeks, a developer can create 160 standard CRUD modules with the features above.

Of course, an application cannot contain only simple CRUD modules. But at least, a simple CRUD module won't take much time to create. Available time can be maximized for other tasks such as data processing, report creation and application testing.

Prambanan uses MagicObject as its library. MagicObjects is very useful for creating entities from a table without having to type code. Just select the table and specify the name of the entity to be created. Entities will be created automatically by Prambanan according to the names and column types of a table.

## System Requirements

-   **Web Server:** Apache Server
-   **PHP Runtime Version:** 5.6 or above
-   **Database:** MariaDB or MySQL

## Dependency

-   **Prambanan:** The core application that facilitates the rapid generation of CRUD modules.
-   **MagicObject:** A library for creating entities from database tables.
-   **Symfony/Yaml:** A library for serializing and deserializing YAML strings and files.

## Advantages of Prambanan

In just under 30 minutes, you can implement a powerful PHP-based data management system that includes a comprehensive set of features essential for managing and manipulating data in a modern application. This system is designed to handle various CRUD (Create, Read, Update, Delete) operations, data validation, and dynamic data presentation. Below is an overview of the key features of the system, which is flexible enough to support both monolithic and microservices-based architectures.

## Key Features Overview

**1. Create New Data**

The system allows users to create new data entries in the database. With minimal configuration, you can insert new records into your tables efficiently. The code is designed to be scalable, allowing easy integration with forms or APIs for creating data.

**2. Update Existing Data**

Updating data is a breeze with this system. Whether you need to update a single record or perform bulk updates, the system provides a flexible API to handle this. You can modify any record's attributes and ensure consistency and integrity during the update process.

**3. Activate Data**

In many business scenarios, records need to be toggled between an "active" and "inactive" state. The system includes an activate function to mark records as active, which can then be used for visibility in front-end applications, reports, or any part of your workflow that requires active data.

**4. Disable Data**

Similar to activating data, the system also provides functionality to disable data. This is especially useful for workflows where data needs to be temporarily hidden or disabled without being permanently deleted. You can mark records as inactive and keep them in the system for later reactivation or auditing purposes.

**5. Delete Data**

Deleting data is handled securely and efficiently. You can delete records from the primary data table, ensuring that the database remains clean and accurate. However, the delete operation is not permanent without further confirmation or approval (explained below).

**6. Move Deleted Data to the Trash Table**

Rather than completely removing deleted records, the system moves deleted data to a "trash" table. This feature adds an additional layer of safety to the data management process, allowing you to recover deleted records if needed. It is ideal for situations where you might need to restore or audit deleted entries later.

**7. Approve Creation, Update, and Deletion of Data**

The system includes an approval workflow for managing data changes. Whether you are creating, updating, or deleting data, these operations can be configured to require approval from authorized personnel before they are executed. This ensures data integrity and accountability within the system.

**8. Reject Creation, Update, and Deletion of Data**

Just as data changes can be approved, they can also be rejected. If there is a need to halt a specific data change, the system provides functionality for rejecting creations, updates, or deletions. Rejected actions are logged for transparency, and the system ensures that no unwanted changes are made.

**9. Display Data Using Filters and Sorting**

Presenting data to the user is essential, and this system has built-in support for filtering and sorting. You can display data based on specific criteria (e.g., filter by date, category, status) and sort the results by different attributes (e.g., ascending or descending order). This feature helps users find and navigate through the data easily, enhancing the user experience.

**10. Update Sort Order**

The sort order of records can be dynamically updated. This is particularly useful for applications that rely on ordering data in a specific sequence, such as product listings, tasks, or blog posts. The system allows you to change the sort order of records easily, maintaining consistency across views.

**11. Join Entity**

The system supports the ability to join multiple entities together. This feature enables you to link related data across different tables (e.g., joining a users table with a posts table). You can efficiently fetch and display related data without needing to manually handle multiple queries, which is a common requirement in complex database systems.

**12. Select Control with Entity and Map**

In many web applications, dropdowns, select boxes, or multi-select controls are used to choose values from a set of entities. This system includes a powerful select control feature, which allows you to populate these controls with data from entities and maps, providing a seamless experience for users who need to select or filter by entity data.

**13. Export Data to Microsoft Excel and CSV Formats**

Data export is a crucial feature for many applications that require reporting and data analysis. This system supports exporting data to both Microsoft Excel and CSV formats, allowing users to download datasets for further analysis or integration into external tools. The export process is simple and can be triggered by the user with just a few clicks.

**14. Support for Both Monolith and Microservices Architectures**

Whether you are building a monolithic application or developing a microservices-based system, this data management system is flexible enough to support both architectures. It can be integrated into a traditional monolith where everything is handled within a single application, or it can be deployed in a microservices architecture, where different services manage distinct pieces of functionality.

-   **Monolithic Architecture**: In this setup, the entire application is managed in one place, and data operations are handled by the same service. This setup is simpler to maintain but may not scale as well as microservices.
-   **Microservices Architecture**: With this approach, different parts of the data management system can be isolated in separate services. For example, the creation and update of data might be handled by one service, while data display and export might be managed by another service. This offers scalability and flexibility but requires more complex architecture.

**15. Support for Multiple Languages**

The system is built with localization in mind. It supports multiple languages, allowing you to easily translate the interface and error messages into various languages. Whether your application is being used by a global audience or by users from different regions, this feature ensures that the system can adapt to various language preferences, improving accessibility and user engagement.

**16. Advanced Data Filters**

The system provides dynamic filters that adapt to the data type, ensuring accurate and efficient data querying based on user-defined criteria.

Apart from the features above, the module is also equipped with data filters that are adjusted to the data type.

## Using Prambanan

First of all, developers must create an entity relationship diagram or ERD. In a database, table relationships are not created explicitly. This means that a column from one table that refers to a column in another table does not have to be associated with a foreign key explicitly in the database. This relationship will be formed by the application.

After the ERD has been created, the developer then exports the ERD to SQL format to be executed on the target database. Some tables may need to be filled in for development needs.

Once the application data structure is ready, next the developer connects Prambanan to the target database then starts and creates the application configuration.

Next, the developer starts creating application modules by selecting tables from the database.

Prambanan will display all columns of the selected table. When a developer uses certain features of Prambanan, Prambanan may add several columns needed by the application. In this case, developers don't need to be afraid because AppBuilder will create a query to alter tables in the database. Developers can copy the query to run on the database.

As long as all database access by the application uses Prambanan, the developer does not need to worry about any specific validation or rule for the data. All validation rules such as validation of data types, null or unique checks will be automatically handled by Prambanan.

Prambanan allows developers to display and organize data from different entities or tables.
