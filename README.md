**Links**

https://www.skills.google/

https://github.com/rjury-sumo/sumologic-query-examples

**Notes**

Tech Down" Meaning: User submits via app, submission fails, and they resort to paper documentation

look at work type code (based on fda), in the job owner excel (533)

unique invocation, instance of flightdetailID request, want to pull like that, if something fails, this step failed, now we know where to look at, need that sort of traceability
Need
Flight Detail ID = unique request identifier (like requestId, tranId, traceId)
Track this ID across multiple events/steps
See which step failed in the flow
Pinpoint exact failure location

POSSIBLE points of failure
s3, sap, geomart, 
there was also a failure in qa pipeline, by any chance, was it logged (want to see the failure looks for flightID), any way to pull that up
rethrowing error with diff messages, might see a diff message with the logging (code)
