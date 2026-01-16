**Links**

*D*

*C*

*R*

*A*

*C*

*O*

*_*

https://www.sumologic.com/help/docs/get-started/account-settings-preferences/

https://www.skills.google/

**Notes**

*D*

Tech Down" Meaning: submission fails via app, and they resort to paper documentation (e.g manually entering into SAP, working with clerk or coordinator, crew_complete thing

look at work type code (based on fda), in the job owner excel (533)

doctype-roadhazard CRUD

ca lambda is cap

a tag, 24 h to fix problem

First comes from sync gateway, revision 2, channelizing it to ec-create-backendstate-new
When it reaches gateway, this polling service receives a response from SGW,

*R*

*A*

inspect -> gas pieplines, some inspected annually, some frwuently, field inspectors; eletric transmission lines, distribution lines, sap is source of truth, work management will take up these work from SAP, work management uses construct app to submit the work, engage to assign work orders

initially, supervisor uses

before sap, uses couchbase for offline storage, saved locally (couchbase lite), then couchbase sync gateway

*C*

put everything you know about this together, document the flow of it, something solidified to present, work off that, if you dont have anything, you need to put the "crust" together, 
offer features such as data integration, customizable dashboards, and trend analysis. Provide actionable insights. outlines the service step by step to help me better understand it

inspection status update status - final log; Track this ID across multiple events/steps, See which step failed in the flow, Pinpoint exact failure location

*O*

7 nodes in each AZ, 21 total; multi az, dr ha test

Infra warning tab, groups to on call coverage, then sort out lambda wikis; shared links, Each dashboard Put excel on right side panel top and then reporting folder next to it

maintenance activities - SAP gateway (affects mytime), PR1, ECC; 

- turn off pollers: users doing stuff in app, replicate to cb (now in mrad platform, pollers subscribing to sgw _changes feed and processing the docs, poller - subcribing to changes on which are new/updated and sends to sqs queue. once in queue, sqs router is listening to these queues, to recieve and process messages, then sending stuff to sap. poller is one of the pipes and flow controls/valves, behind poller is sqs router, 

- if we turn off sqs router, poller is going to stack up in queue, but the queue has a dead letter, some kind of limit, so we don't want to overload the queue

- to know if sap is functioning, check docupload service (sap to mrad, sending stuff to sap, micropolling is making api calls to mulesoft and then mulesoft is hitting sap, docupload has multiple stacks (top - aqi gw (mulesoft), once sap sends api request to api gw, qpi gw validates, based on validation of headers, thats for docupload lambda, so it invokes director lambda, then director lamnda validates the headers, for this doctype i am going to invoke this, doctype i am going to invoke that), other one is scheduled tasks (deals with mytime, if sap is down, the requests, so the app will be working, it's going to do a 500, failed response, this service handles the communication from app, the volume also, if sap is down), also failed heartbeats

**every saturday, there is a weekly sap restart, DO 8 to 11pm, compare to major outage; december release lasted over 24hrs**

*_*

ben nu wah (benoit)

not following best practices, inconsistencies, we can possibly make it intuitive, 

decipher the syntax, write logic to parse the messages and extract the data we need

put everything you know about this together, document the flow of it, something solidified to present, work off that, if you dont have anything, you need to put the "crust" together, 
offer features such as data integration, customizable dashboards, and trend analysis. Provide actionable insights. outlines the service step by step to help me better understand it
