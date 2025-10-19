# Database

The artifact is the local persistence layer of my Android inventory management app, originally created for CS 360. It uses SQLite to store and manage inventory items, locations, and transfers locally on the device. The database allows the app to function offline by caching data and later synchronizing it with the “cloud-based” API.

## Justification for Inclusion

I selected this artifact because it demonstrates my understanding of database schema design, versioned migrations, and data synchronization between a local store and a remote API. The enhancement focused on normalizing the schema, adding versioned migrations to prevent data loss during upgrades, and introducing fields for synchronization tracking such as server_id, client_id, updated_at, and deleted_at. This improvement also included defensive schema validation using PRAGMA table_info to ensure column integrity and compatibility with future updates. Together, these changes show my ability to design reliable persistence systems that support both offline-first behavior and scalable synchronization.

## Course Outcomes

I met my planned outcomes. The enhancement applied database normalization principles, enforced constraints, and implemented a pretty strong migration strategy, directly aligning with the course outcome of designing and managing relational databases for data integrity and reliability.

## Reflection on the Enhancement Process

Through enhancing the database, I learned how critical version control and migrations are for preserving user data during schema evolution.The main challenge was handling runtime crashes caused by schema mismatches (like, missing columns like server_id) after updating the app. I somewhat broke the previous version of the sqlite database so I had to wipe the data of the emulator for the new database updates to solve the issue. I also gained experience balancing local persistence with “cloud” (not really cloud – but in production it would be cloud) synchronization, making sure that the app could remain functional offline and update seamlessly once connectivity is restored. This experience deepened my understanding of data integrity, schema evolution, and the importance of backward compatibility in mobile app databases.