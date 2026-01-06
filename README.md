# Polymorphic Bakery Manager

Key Features

The Polymorphic Bakery Manager is a comprehensive digital interface designed to streamline the operations of a bakery by managing complex product orders and transaction history. At its core, the system facilitates the dynamic creation of customized cakes—accounting for base prices, specific fyllning selections, and portion sizes—alongside a variety of standardized bakery goods sold per unit. Organized through an intuitive split-panel GUI, the application allows users to browse menus, add diverse items to a current order, and receive real-time updates on the total cumulative cost. Beyond immediate transactions, the system maintains a robust order history archive, enabling administrators to revisit past selections and review detailed summaries of previous sales through an integrated history management module.

Technical Implementation

This project is built upon a sophisticated modular architecture in Java, strictly adhering to the Model-View-Controller (MVC) design pattern to ensure scalability and code clarity. The technical backbone of the system is the `Orderable` interface, which leverages polymorphism to treat disparate entities like `Cake` and `PerUnitItem` as uniform order components, significantly reducing logic duplication. Unlike previous iterations that relied on static arrays, this version utilizes `java.util.ArrayList` for flexible data storage and incorporates `java.util.regex` to parse and extract financial data from structured order strings. The user interface is managed via `javax.swing`, utilizing a centralized controller to handle button events and synchronize data between the backend models and the front-end list views.

Challenges & Reflection

One of the primary architectural challenges in this project was determining the most effective method for abstraction, ultimately choosing an interface over an abstract class to maximize the system's future flexibility and ease of implementation for new product types. The reflection highlights the benefits of this approach, noting that adding new categories like beverages would simply require implementing the `Orderable` contract without restructuring the existing hierarchy. However, the development also uncovered certain trade-offs, such as the limitations of using `Enum` classes for prices which necessitates manual code updates rather than dynamic external configuration. Furthermore, this project served as a significant exercise in collaborative development through pair programming, requiring synchronized design efforts and the reconciliation of different implementation strategies for GUI management and data parsing.

Getting Started

To run the Polymorphic Bakery Manager on your machine, ensure you have the JDK installed and execute the following commands in your terminal:

```bash
# Navigate to the source root directory
cd DA339A_U3_src_Grupp_4

# Compile the modular package structure
javac Controller/*.java Model/*.java View/*.java

# Run the application via the Main entry point
java Controller.Main
```
*Author: Alper Eken & Josef Zakaria Course: Objectoriented programming Semester: Autumn 2024*
