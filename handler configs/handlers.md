### Core Handlers

M2 defines the following core hander definitions for which example configs can be found in this folder.

#### Logging

Describes how the event processor should log events of this type, this includes log level and log retention period.

#### Classification

The data or security classification applied to the event, this ranges from public to restricted.

#### Caching

If the event details should be cached.

#### TTL

How long after the event has been produced it should be considered valid for processing, defined in seconds and/of valid until date-time.

#### Failure

How to handle event processing failures, number of retries and retry intervals plus how to handle when failed.

#### Ordering

Provides context on how events of this type should be ordered or grouped for processing.

#### Range

Enables event processing to be restricted to a range of events with processFrom and processTo indentifiers.

