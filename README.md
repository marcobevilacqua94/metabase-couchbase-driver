# metabase-couchbase-driver
Draft of a Couchbase driver for Metabase

Leveraging Couchbase JDBC driver.

To install it on Metabase, download Metabase sources from here https://github.com/metabase/metabase and add the folder couchbase as a module inside metabase/modules/drivers, then run ./bin/build-driver.sh couchbase as explicated in Metabase guide to build drivers. 

Also add 

metabase/couchbase          {:local/root "couchbase"}

to drivers/deps.edn

At the moment the driver has some authentication issue.

There could be something wrong with the sql-jdbc.conn/connection-details->spec :couchbase method.

The exception (providing right credentials):

2024-03-19 18:15:18,302 ERROR api.database :: Cannot connect to Database
clojure.lang.ExceptionInfo: Authentication/authorization error - please check credentials. {:message "Authentication/authorization error - please check credentials."}
