+++
title = "Database"

[extra]

level = 1

intro = "Proper Database support is crucial for modern web development. This page gives an overview of the various drivers, ORMs, integrations and tools."

drivers = [
  "mysql",
  "couchbase",
  "mysql_async",
  "postgres",
  "redis",
  "darkredis",
  "rusqlite",
  "tokio-postgres",
  "leveldb",
  "rocksdb",
  "sled",
  "influx_db_client",
  "cassandra-cpp",
  "cdrs",
  "memcache",
  "mongodb",
  "sqlx"
]

orms = [
  "diesel",
  "quaint",
  "rustorm",
  "tql"
]

pools = [
    "mobc",
    "deadpool",
    "bb8",
    "r2d2"
]

tools = [
  "diesel_migrations",
  "migrant",
  "refinery",
  "oapth"
]

newstag = "database"
+++

<h2 id="drivers">Drivers</h2>

{{ packages(packages='drivers') }}

<h2 id="orms">ORMs</h2>

{{ packages(packages='orms') }}

<h2 id="pools">Connection pools</h2>

{{ packages(packages='pools') }}

<h2 id="tooling">Tooling</h2>

{{ packages(packages='tools') }}
