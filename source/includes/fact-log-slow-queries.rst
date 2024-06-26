.. COMMENT: When included as part of options/settings, this is used by mongod and configuration file and not mongos. For mongos, see options-mongos.yaml.  This file is however included in other files where distinction between mongod/mongos is sufficient.

When :parameter:`logLevel` is set to ``0``, MongoDB records *slow*
operations to the diagnostic log at a rate determined by
:setting:`~operationProfiling.slowOpSampleRate`.

At higher :parameter:`logLevel` settings, all operations appear in
the diagnostic log regardless of their latency with the following
exception: the logging of slow oplog entry messages by the
secondaries. The secondaries log only the slow oplog
entries; increasing the :parameter:`logLevel` does not log all
oplog entries.
 