# Transfer feature

The artifact I worked on is the Inventory Transfer feature, which I originally built in CS360: Software Development Lifecycle. This feature was designed to allow employees or whoever is in control of inventory at a coffee shop to move item quantities between storage locations, for example, transferring cups from the back room to the front counter. The implementation includes multiple layers: an Activity/Fragment for the user interface, Java classes serving as the ViewModel/Controller to handle transfer logic, and a Repository layer to manage persistence through a SQLite database.

## Justification for Inclusion
I am including this artifact in my ePortfolio because it demonstrates a complete end-to-end solution that showcases all of the artifacts and other important skills in software development. It displays my ability to design a user interface that supports real business operations, and connect to a data persistence layer that makes sure that inventory data remains consistent even when wifi goes out. This artifact shows not only programming proficiency in Java and Android development but also design skills like separation of concerns, reusability, and maintainability.

The enhancement improved the artifact by refactoring the database layer to use a stronger model class (InventoryItem) instead of loosely structured HashMap objects. This change improved type safety, readability, and scalability while aligning the project more closely with modern software engineering practices.

## Course Outcomes

I think I bascially met the outcomes I planned to meet in Module One. I wanted to go more in depth and completely redesign the transfering and inventory portion, but I may have overlooked the amount of time I can actually spend on a project. 

I do not have major changes to my outcome-coverage plans, but I can now also point to this enhancement as evidence of applying design improvements and adhering to secure coding best practices.

## Reflection on the Enhancement Process

Enhancing and modifying the artifact taught me how important it is to start with a clear model system when working with persistent data. By moving from generic maps to a strongly typed InventoryItem class, I saw firsthand how code becomes easier to understand, less error-prone, and easier to extend. Also by touching the model I had to literally touch every other file that pertained to inventory. It would have been much easier to start with a model instead of adding one.
Another issue I faced was that my Android Studio was buggy. After creating the InventoryItem class, it kept giving me errors that I knew should not have existed. I basically had to code without an LSP and find out what the real errors were though compiling. After I could compile the code without any errors I then completely cleared the cache and it started working again.