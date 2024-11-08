ADR 4:
Selection of Backend Language

Status:
Accepted

Context:
The development team is creating a food delivery app that allows users to order food from local restaurants for delivery or pickup. Key functionalities include user account creation, secure payment handling, real-time order tracking, and an easy-to-navigate interface. Given the following requirements, a reliable and efficient backend language is essential:

    Real-Time Order Tracking: The backend must support real-time updates to track the order’s progress, ensuring users have up-to-date status information.

    Location Tracking: The app needs to access the user’s location to provide accurate restaurant recommendations and estimate delivery times.

    Payment Integration: The backend must securely integrate with multiple payment gateways.

    Menu Synchronization: The backend should seamlessly integrate with restaurant inventory management systems to ensure users see accurate, up-to-date menus.

    User Reviews and Ratings: The backend must manage and display user-generated reviews and ratings.

    Order History: Efficient storage and retrieval mechanisms are required for displaying users' order history, allowing them to reorder their favorite items.

    Push Notifications: The backend must handle timely notifications about order status updates, confirmations, and promotions.

Decision:
Node.js is chosen as the backend language.

Justification:

    Real-Time Capabilities: Node.js is well-suited for handling real-time applications due to its non-blocking, event-driven architecture, which is essential for live order tracking.

    Efficiency with I/O Operations: Node.js’s asynchronous capabilities allow efficient handling of numerous concurrent I/O requests, such as API calls for location tracking and menu synchronization.

    Extensive Library Support: The Node.js ecosystem includes a wide range of libraries for integrating payment gateways, location services, and WebSocket for real-time updates.

    Cross-Platform Flexibility: Node.js is compatible with various front-end frameworks, making it adaptable for mobile platforms, and enabling a unified development approach across iOS and Android.

    Scalability: Node.js supports horizontal scaling, which will be beneficial as the user base expands and the app requires more resources to handle a high volume of orders.

    Developer Familiarity: The team has experience with JavaScript, so Node.js is a natural choice that leverages existing expertise, minimizing the learning curve and reducing development time.

Consequences:

    Potential Performance Constraints for Heavy Computations: Node.js is not optimized for CPU-intensive tasks. However, given that this app primarily requires I/O-bound operations, this limitation is manageable.

    Concurrency Management: Effective concurrency handling may be challenging in Node.js for complex workflows, though leveraging frameworks such as NestJS can mitigate this.
