
# APIs

## Display Name

### Convention
<API Type> - <Backend System/Consumer?> - <Process?> - <Entity?> - <Internet Facing or Not>

API Type – Mandatory for all API Names
Backend System – Only applicable for System APIs
Consumer – Only applicable for Consumer APIs
Process – Only applicable for Process APIs
Entity – Only applicable for Data or may be System APIs

### Examples

* System Events - SmartRecruiters - External
* System Aggregate - SmartRecruiters - Internal
* System Read Proxy - SmartRecruiters - Internal
* System Write Proxy - SmartRecruiters - Internal
* System Read - SuccessFactors - Employee Central - Internal
* System Write - SuccessFactors - Employee Central – Internal
* Data Read - Employee – Internal
* Process – Order Fulfilment – External
* Consumer – Smart Recruiters - External

## API Name

### Convention
<apiType>-<system?>-<domain?>-<entity?>

### Examples

* sysevents-srec
* sysrdpxy-srec-candidates
* sysrdpxy-srec-jobs
* syswtpxy-sapsf-employeeCentral


## API URL Suffix

### Convention
"/<Internet Facing or Not>/<API Name>/<version>"

### Examples

* /internal/sysevents-srec/v1
* /external/sysevents-srec/v1


## Operation Display Name

### Convention
<Relevant Verb> <Entity> <Relevant Context>

### Examples

* Get Candidate
* Create Candidate
* Update Candidate
* Delete Candidate


## Operation Name

### Convention
<relevantVerb>-<entity>-<relevantContext>

### Examples

* get-candidate
* create-candidate
* update-candidate
* delete-candidate

## Operation URL

### Convention
/entity/{id?}

### Examples

* /candidate/1234

# Types of APIs

### API
System Events
### Short Identifier 
sysevents
### Description
An API Provider that acts as an intermediary interface to receive events from another system and then publish them to message broker to be processed by other components.


### API
System Read Proxy
### Short Identifier 
sysrdpxy
### Description
An API Provider that acts as an intermediary interface that provides read access to another system’s API as it is, for the sake of standardisation and single point of entry. There is no transformation of data in such APIs.

