# Project HBmB

This project was carried out by: Roger G. Rosado

Project Description: HBnB Evolution Documentation

Context and Objective: This project focuses on developing comprehensive technical documentation for the HBnB Evolution application, which is a simplified version of an AirBnB-like platform. The primary goal of this documentation is to serve as a blueprint for the system's architecture and design, guiding future implementation phases and ensuring clarity in the development process.

Key Features of HBnB Evolution:

User Management:
Users can register, update profiles, and be assigned roles (regular users or administrators).
Place Management:
Users can list properties with details such as name, description, price, and location.
Review Management:
Users can leave reviews for properties they have visited, including ratings and comments.
Amenity Management:
The system allows the creation and management of amenities associated with places.

Business Requirements:

User Entity: First name, last name, email, password, and administrator role.
Place Entity: Title, description, price, location, and a list of amenities.
Review Entity: Rating, comment, and association with a user and place.
Amenity Entity: Name and description.
System Architecture: The application is designed with a three-layered architecture:

Presentation Layer: API services to manage user interactions.
Business Logic Layer: Core logic, handling entities like users, places, reviews, and amenities.
Persistence Layer: Database interactions for storing and retrieving data.
Tasks and Deliverables:

High-Level Package Diagram: Illustrates the layered architecture and communication via the facade pattern.
Detailed Class Diagram: Depicts entities and their relationships in the Business Logic layer.
Sequence Diagrams: Visualizes the flow of API calls for key operations like user registration, place creation, review submission, and place listing.
The final technical document will compile these diagrams and explanations, offering a detailed and professional reference for HBnB Evolutions development.


