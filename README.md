# Thesis
SQL / NoSQL DBMS for mobile applications

## Databases

- Couchbase Lite: Most optimal NoSQL Document-Based database for IoT according to many sources, which makes it perfect for local storage and caching - 
  - Internal Structure: B+ Tree - Generic Index data-structure for most relational databases and document-based NoSQL databases
  - Usage: IoT local databases, memory-optimized NoSQL database
  - References:
    - https://github.com/couchbase/couchbase-lite-android
    - https://github.com/couchbaselabs/Android-Couchbase
    - https://docs.couchbase.com/couchbase-lite/current/android/quickstart.html
- ForestDB: Key-Value NoSQL database developed by the same people who developed Couchbase Lite specifically for caching use-cases, which makes it even better
  - Internal Structure: HB+ Tree - More optimal tree data-structure specifically for caching and key-value storage
  - Usage: Caching data as key-value pairs - Documentation specifically mentions mobile devices usage
  - References:
    - https://dbdb.io/db/forestdb
    - https://rustrepo.com/repo/couchbase-forestdb-rust-database
    - https://github.com/couchbase/forestdb
- LevelDB: A Key-Value storage engine that uses completely different approach with LSM Trees, which gets more and more recognition for efficient read-write operations
  - Internal Structure: LSM Tree - Write-optimized B Tree variant which uses log-structured storage of operations and data
  - Usage: Efficient Key-Value storage with Lob-based structure approach
  - References:
    - https://dbdb.io/db/leveldb
    - https://github.com/google/leveldb
    - https://github.com/hf/leveldb-android

Important: Even though traditional NoSQL approaches such as Couchbase Lite and ForestDB work well for IoT and are getting more and more recognition on mobile devices, LSM Tree based Key-Value stores seem like a brand new and extremely promising approach. Lots of papers I included focus on how it works, how to use it as a cache and some even go as **far as to reimplement SQLite using LSM Tree (meaning the only things left of SQLite is syntax, so it could just as easily be a NoSQL database with a SQL interface)**.
