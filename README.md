# Splunk Auto Documentation

## Disclamer
### This tool is still under development/conversion to be public.

## Welcome

With the Splunk Autodoc, you can convert your Alerts to pretty auto documentated pages in tools like Atlassian Confluence Wiki.
The documentation is one-way: from Splunk and to the documentation software. Any changes made in the documentation software will be overwritten by Splunk.

The tool automatically documents the alerts that have been tagged with the tag "autodoc" and creates/updates/deletes the pages in your documentation software.

![Photo](./static/Normal_autodoc_page.png)


## Prerequisites
You need to be able to send REST queries to your documentation software.
For Atlassian Confluence Wiki (only testet on OnPrem) you need to create the ParentPage and one dummy child page. This dummy child page can after first update to Wiki be deleted.
