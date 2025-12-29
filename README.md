**Links**

https://www.skills.google/

https://github.com/rjury-sumo/sumologic-query-examples

https://loggingsucks.com/?utm_source=tldrdev

**Notes**

Tech Down" Meaning: submission fails via app, and they resort to paper documentation (e.g manually entering into SAP, working with clerk or coordinator, crew_complete thing

look at work type code (based on fda), in the job owner excel (533)

unique invocation, instance of flightdetailID request, want to pull like that, if something fails, this step failed, now we know where to look at, need that sort of traceability
Need
Flight Detail ID = unique request identifier (like requestId, tranId, traceId)
Track this ID across multiple events/steps
See which step failed in the flow
Pinpoint exact failure location

7 nodes in each AZ, 21 total; multi az, dr ha test

**Other**

not following best practices, inconsistencies, we can possibly make it intuitive, 

decipher the syntax

write logic to parse the messages and extract the data we need

logs should be self explanatory

processing - done creating asset images, extracting geojson, say ingestion is complete

parameters

ben nu wah (benoit)

transaction ID, what went wrong for a given flight
retries managing to queue (dead letter queue), retries the same message 3 times, if after 3 times, message goes to dlq, we ccan manually iunspect those messages and retry them back to source queue to process again

ternary operator 

doctype-roadhazard CRUD
