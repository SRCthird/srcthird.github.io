# Sort and Filter

The artifact I selected is the Inventory Search/Filter/List feature, for the app originally created during CS 360: Software Development Lifecycle. It powers the home screen of the mobile application by displaying inventory items and allowing users to search or filter them by name or location. The original implementation used a straightforward linear scan across the list of items to perform filtering.

## Justification for Inclusion

I chose this artifact for inclusion in my ePortfolio because it demonstrates my ability to work with algorithms and data structures in a practical, real-world context. The feature showcases how algorithmic choices directly affect performance: a simple linear filter works well for small datasets but becomes inefficient at scale. By enhancing it with an inverted index (HashMap of token → list of item IDs) and a companion id → item map, I improved query performance from O(n·m) (n = number of items, m = number of tokens) to near O(m + k) (where k = number of matching results). This improvement highlights my ability to analyze algorithmic complexity, select appropriate data structures, and balance time vs. memory tradeoffs.

The enhancement also expanded the strength of the feature by adding incremental index updates on item insert/edit, which demonstrates understanding of dynamic data structure maintenance. Together, these components show both algorithmic reasoning and practical engineering skills in building scalable software features.

## Course Outcomes
I met the course outcomes I planned to address in Module One. Specifically, the enhancement demonstrates:
- Algorithmic thinking: analyzing time complexity of linear search vs. indexed search.
- Application of data structures: using HashMap, lists, and sets to store and query inventory efficiently.
- Software performance and correctness: testing against real datasets to confirm speedup and ensure functional accuracy.
- Scalability considerations: designing incremental index updates to keep queries fast as the dataset grows.
I do not have major updates to my outcome-coverage plan, but I can now also claim stronger alignment with the outcome involving strategies for collaborative environments. Indexing decisions and performance benchmarks are easy to communicate to technical and non-technical stakeholders, helping them understand how software design choices impact usability at scale.

## Reflection on the Enhancement Process

Enhancing and modifying this artifact taught me the importance of choosing the right algorithm and data structure for the problem size from the start. While the naive linear filter was simple, scaling the feature forced me to think about real-world performance and the tradeoffs between preprocessing time, memory use, and query speed.

The biggest challenge I faced was managing incremental updates to the index when items were added, edited, or deleted. This required actual thinking to avoid stale references and make sure correctness across all operations.