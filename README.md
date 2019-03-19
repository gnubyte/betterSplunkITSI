# splunk-toolbox

## Version 1.1.2
A better wrapper around the Splunk ITSI Rest API and Splunk Core API for anyone feeling the pain



## Version table
 - 1.0.0 initial PoC/format
 - 1.1.0 added Post update to ITSI Notable Event Group
 - 1.1.1 bugfix & clarification of requirements for post_update_to_notable_event_group
 - 1.1.2 added handler for status code interpretation to post update to notable event group

Intended to solve stability issues produced by the product itself.


## Splunk Toolbox Bio

This is a wrapper around the ITSI API. Where the ITSI API is not 
functioning, we are using sftp calls instead or core API.

## Example Uses



#### Retrieve active search jobs from ITSI
```
splunk_server = splunkInstance(authPass='mypass')
splunk_server.retrieve_search_jobs(recordSearches=1)
```


#### Post updates to ITSI Notable Event Group


```
splunk_server = splunkInstance(authPass='mypass')
payload ={"status":"5"}
splunk_server.post_update_to_notable_event_group(payload=payload, )
```