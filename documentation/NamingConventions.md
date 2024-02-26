APIs
Attribute	Convention	Example
Display Name	<API Type> - <Backend System/Consumer?> - <Process?> - <Entity?> - <Internet Facing or Not>

API Type – Mandatory for all API Names
Backend System – Only applicable for System APIs
Consumer – Only applicable for Consumer APIs
Process – Only applicable for Process APIs
Entity – Only applicable for Data or may be System APIs	•	System Events - SmartRecruiters - External
•	System Aggregate - SmartRecruiters - Internal
•	System Read Proxy - SmartRecruiters - Internal
•	System Write Proxy - SmartRecruiters - Internal
•	System Read - SuccessFactors - Employee Central - Internal
•	System Write - SuccessFactors - Employee Central – Internal
•	Data Read - Employee – Internal
•	Process – Order Fulfilment – External
•	Consumer – Smart Recruiters - External
API Name	<apiType>-<system?>-<domain?>-<entity?>	•	sysevents-srec
•	sysrdpxy-srec-candidates
•	sysrdpxy-srec-jobs
•	syswtpxy-sapsf-employeeCentral
API URL Suffix	/<Internet Facing or Not>/<API Name>/<version>	•	/internal/sysevents-srec/v1
•	/external/sysevents-srec/v1
Operation Display Name	<Relevant Verb> <Entity> <Relevant Context>	•	Get Candidate
•	Create Candidate
•	Update Candidate
•	Delete Candidate
Operation Name	<relevantVerb>-<entity>-<relevantContext>	•	get-candidate
•	create-candidate
•	update-candidate
•	delete-candidate
Operation URL	/entity/{id?}	/candidate/1234

Types of APIs
API	Short Identifier	Description
System Events	sysevents	An API Provider that acts as an intermediary interface to receive events from another system and then publish them to message broker to be processed by other components.
System Read Proxy	sysrdpxy	An API Provider that acts as an intermediary interface that provides read access to another system’s API as it is, for the sake of standardisation and single point of entry. There is no transformation of data in such APIs.
System Write Proxy	syswrtpxy	An API Provider that acts as an intermediary interface that provides write access to another system’s API as it is, for the sake of standardisation and single point of entry.
System Aggregate	sysagg	An API Provider that provides access to aggregated data or functionality within a system. It accepts an input, enriches it by interacting with other systems and provides an aggregated output.
System Read	sysrd	An API Provider that acts as an intermediary interface that provides read access to a system’s data/functionality. It does not need to represent the end system API as it is and can be used to cater to a common information model if required.
System Write	syswrt	An API Provider that acts as an intermediary interface that provides write access to a system’s data. It does not need to represent the end system API as it is and can be used to cater to a common information model if required.
Data Read	datrd	An API Provider that provides read access to a business data entity following a common information model collating data from multiple system or system APIs.
Process	prcs	An API Provider that exposes the functionality required to service a business process. Usually, a Process API orchestrates one or more calls to various System APIs to fulfil end to end process functionality.
Consumer	cnsr	An API Provider that is created to expose a functionality catered to a specific consumer as the consumer does not have the ability to consume the process, data or system APIs directly.
Utility	util	An API that is created for the general purpose and is used across many integration applications.  For example, Reference Data API.


Products
•	Include target audience or scope.
For example, “internal-”, “external-”, “public-”
•	Include specific business units if necessary.
For example, “internal-hr”, “external-finance”
•	Use hyphen (-) to segregate between the above identifiers.
•	Use camel casing to segregate different words in system’s name or context.
•	Avoid special characters.


•	
Named Values
•	Use a prefix for all the named valued.
For example, “nv--”
•	Include relevant contextual information in the name.
For example, “nv--orderProcessingTimeout”
•	If the named value is for a specific external system/application, include the system identifier.
For example, “nv--apiKey--SFCandidates”
•	Use double hyphen (--) to segregate between the above identifiers.
•	Use camel casing to segregate different words in system’s name or context.
•	Avoid special characters.
