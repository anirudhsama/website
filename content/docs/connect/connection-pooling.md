---
title: Connection pooling
enableTableOfContents: true
redirectFrom:
  - /docs/get-started-with-neon/connection-pooling
---

## PostgreSQL connection limits

Each PostgreSQL connection creates a new process in the operating system, which consumes resources &mdash; memory, open file descriptors, etc. For this reason, PostgreSQL limits the number of open connections. The Neon [Technical Preview Free Tier](/docs/reference/technical-preview-free-tier) allows 100 simultaneous PostgreSQL connections by default (`max_connections=100`), with a small number of those connections reserved for administrative purposes.

Some applications open numerous connections, with most eventually becoming inactive. This behavior can often be attributed to database driver limitations or to running many instances of the application. To handle these situations, Neon supports connection pooling.

## Connection pooling in Neon

Enabling connection pooling allows PostgreSQL to accept up to 1000 connections. The connections are routed to a smaller number of real PostgreSQL connections. Neon uses `pgbouncer` in `transaction mode` for connection pooling. For information about `pgbouncer`, refer to [https://www.pgbouncer.org/](https://www.pgbouncer.org/).

## Enable connection pooling

To enable connection pooling for a Neon project:

1. Navigate to the [Neon console](https://console.neon.tech/).
2. On the **Dashboard**, select your project.
3. Select **Settings** > **General**.
5. Toggle **Enable pooling** to the on position.
6. Click **Save**.

### Limitations

PostgreSQL features such as prepared statements and [LISTEN](https://www.postgresql.org/docs/15/sql-listen.html)/[NOTIFY](https://www.postgresql.org/docs/15/sql-notify.html) are not supported with connection pooling. For a complete list of limitations, refer to the "_SQL feature map for pooling modes_" section, in the [pgbouncer.org Features](https://www.pgbouncer.org/features.html) documentation.

## Need help?

Send a request to [support@neon.tech](mailto:support@neon.tech), or join the [Neon community forum](https://community.neon.tech/).
