**Links**

https://www.skills.google/

https://github.com/rjury-sumo/sumologic-query-examples

https://loggingsucks.com/?utm_source=tldrdev

**Notes**

Tech Down" Meaning: submission fails via app, and they resort to paper documentation (e.g manually entering into SAP, working with clerk or coordinator, crew_complete thing

look at work type code (based on fda), in the job owner excel (533)

7 nodes in each AZ, 21 total; multi az, dr ha test

**Other**

not following best practices, inconsistencies, we can possibly make it intuitive, 

decipher the syntax

write logic to parse the messages and extract the data we need

logs should be self explanatory

processing - done creating asset images, extracting geojson, say ingestion is complete

parameters

ben nu wah (benoit)

**16th**

db tips:
unique invocation, instance of flightdetailID request, want to pull like that, if something fails, this step failed, now we know where to look at, need that sort of traceability
Need
Flight Detail ID = unique request identifier (like requestId, tranId, traceId)
Track this ID across multiple events/steps
See which step failed in the flow
Pinpoint exact failure location

review:
there's a scans project where ibhrahim is working on the design, and meet is ooo until friday i believe; 

improvements:
Need unique identifier (UUID) across all events to track flight processing requests end-to-end; Unify logging with consistent UUID across all events, improve event naming conventions (e.g ingest structures)
e.g for mine, Transaction IDs only hit some events, not all - filtering on transaction ID causes missed data
as ibhrahim discussed, Many logs are from old code and don't match new architectural expectations

Approach Decided
Full refactor pushed to backlog, Defer logging improvements to later sprint when scan project allows bandwidth, Make logging changes immediately only if there's a bug or if we are blocked

transaction ID, what went wrong for a given flight
retries managing to queue (dead letter queue), retries the same message 3 times, if after 3 times, message goes to dlq, we ccan manually iunspect those messages and retry them back to source queue to process again

**Misc**

ternary operator

doctype-roadhazard CRUD
