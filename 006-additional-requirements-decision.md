ADR 2:
    Additional Frameworks or Technology Stacks that might be required.

Status:
    Accepted

Context:
    There might be additional frameworks or technology stacks that are required for the application. The following will list out the decided ones.

Decision:
    Socket.IO - For real-time communication, enables bi-directional real-time communication between the server and clients

    Firebase Cloud Messaging (Android) and Apple Push Notification Service (iOS) - Manages push notifications

    Google Analytics for Firebase - To track user behaviour, engagement, metrics and app performance.

    Glide (Android) and SDWebImage (iOS) - To efficiently load images, caches and display product images.

    i18next or Native Platform localization Libraries - Localization support

Consequences
    Specialized Skill Requirements - There is a need to familiarize ourselves with these additional frameworks

    Compatibility - While not a big worry, there might be some compatibility issues that need to be addressed with this many additional frameworks.

    Complex Technology Stack - Integrating multiple frameworks may require additional time for setup and maintenance.