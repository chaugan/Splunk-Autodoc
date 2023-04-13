
# Splunk Autodoc for Atlassian Confluence Wiki

## Autodoc: Create and Update.spl

Alert used to create and update Atlassian Confluence Wiki based installations.

The alert returns zero results when everything went fine. If some error occured, the following email is sent out:

Message subject:
```
Unable to process new or updated Autodoc for $result.title$
```

Message body:
```
The Autodoc feature "Create and Update" failed with the following messages:

HTTP code:
$result.curl_status$

REST method:
$result.curl_method$

Curl message:
$result.curl_message$

Curl payload:
$result.curl_data_payload$
```

A common problem (Internal Server Error - 500) is that there is some characters in your REST query to the Wiki that it does not accept. You need to find those special character(s) and sort it out with the HTML code for it.




## Autodoc: Delete.spl

Alert used to delete Wiki pages when you remove alerts in Splunk or remove the Autodoc tag in the alert itself.


## Results

### Normal SPL
![Normal](../static/Normal_autodoc_page.png)


### Abnormal SPL
![Abnormal](../static/Makeresults_first_autodoc_page.png)
