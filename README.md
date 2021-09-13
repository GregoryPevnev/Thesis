# Thesis
SQL / NoSQL DBMS for mobile applications

## Databases

- Couchbase Lite: Most optimal NoSQL Document-Based database for IoT according to many sources, which makes it perfect for local storage and caching - 
  - Internal Structure: B+ Tree - Generic Index data-structure for most relational databases and document-based NoSQL databases
  - Usage: IoT local databases, memory-optimized NoSQL database
  - References:
    - https://github.com/couchbase/couchbase-lite-android
- ForestDB: Key-Value NoSQL database developed by the same people who developed Couchbase Lite specifically for caching use-cases, which makes it even better
  - Internal Structure: HB+ Tree - More optimal tree data-structure specifically for caching and key-value storage
  - Usage: Caching data as key-value pairs - Documentation specifically mentions mobile devices usage
  - Reference: https://github.com/couchbase/forestdb
- LevelDB: A Key-Value storage engine that uses completely different approach with LSM Trees, which gets more and more recognition for efficient read-write operations
  - Internal Structure: LSM Tree - Write-optimized B Tree variant which uses log-structured storage of operations and data
  - Usage: Efficient Key-Value storage with Lob-based structure approach
  - Reference: https://github.com/google/leveldb

Important: Even though traditional NoSQL approaches such as Couchbase Lite and ForestDB work well for IoT and are getting more and more recognition on mobile devices, LSM Tree based Key-Value stores seem like a brand new and extremely promising approach. Lots of papers I included focus on how it works, how to use it as a cache and some even go as **far as to reimplement SQLite using LSM Tree (meaning the only things left of SQLite is syntax, so it could just as easily be a NoSQL database with a SQL interface)**.

## Resources

TODO: Write annotations and quick descriptions for each resources some time

1. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/8717652
2. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/6625441
3. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/8094443
4. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/8428922
5. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/8622920
6. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/7110563
7. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/8327122
8. https://link.springer.com/article/10.1007/s002360050048
9. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/7352511
10. https://ieeexplore-ieee-org.library.sheridanc.on.ca/document/8411471
More are going to be added
