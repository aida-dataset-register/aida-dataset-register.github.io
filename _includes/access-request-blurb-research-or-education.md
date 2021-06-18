{%- capture body -%}
Hi!

I work at INSTITUTION department of DEPARTMENT in COUNTRY, emailing from my institutional account.

I would like to request access to the dataset doi:{{ include.doi }}, for use in research or education.

Our planned use of the data can be summarized as:

BRIEF_DESCRIPTION_OF_PLANNED_ACTIVITIES_HERE

Dataset: {{ include.dataset_url }}

I would like to ALTERNATIVELY_WOULD_NOT_LIKE_TO be included in the public record of data sharing facilitated by AIDA:

https://docs.google.com/spreadsheets/d/1fl2BwZJ4rivOKzOCy5pAnxU8N1CyoF86BTCnH-rBV04

which AIDA uses to demonstrate its utility to the global research community.

(If "not", then only the institution/department information will be included. This choice of personal participation is not weighed into the access request eligibility evaluation.)

/MY_NAME
{%- endcapture -%}
You are invited to send an
<a href="mailto:{{ include.to }}?cc={{ include.cc }}&subject=Requesting access to dataset doi:{{ include.doi }}&body={{ body | url_encode | replace: '+','%20' }}">access request email</a>
from your institutional account.

Clicking the access request email link above should open a draft email message
in a new window, to help you provide relevant information for efficient request
evaluation.
