Hi!

I work at INSTITUTION in COUNTRY, emailing from my institutional account.

I would like to sign a data sharing agreement for the dataset doi:{{ include.doi }}, for use in ethical and legal medical diagnostics research. Could you please send me an agreement template?

Our planned use of the data can be summarized as:

BRIEF_DESCRIPTION_OF_PLANNED_ACTIVITIES_HERE
{% if include.coauthorship %}
We are aware that publications resulting from the use of this data must include indicated authors of this dataset in the author list.
{% endif %}
Dataset: {{ include.dataset_url }}

Example agreement template: {{ include.agreement_template_url | default:"https://datasets.aida.medtech4health.se/sharing/templates/" }}

Template placeholders:

Name of research PI ("Recipient Scientist"): RESEARCH_PI_FIRST_NAME RESEARCH_PI_LAST_NAME (cc here)
Title of research PI: RESEARCH_PI_TITLE (ph d or better, in relevant field)

Name of institution: INSTITUTION_NAME
Name of department: DEPARTMENT_NAME
Institution postal address: INSTITUTION_POSTAL_ADDRESS

Name of authorized signatory: SIGNATORY_FIRST_NAME SIGNATORY_LAST_NAME (cc here)
Title of authorized signatory: SIGNATORY_TITLE

Also, I would like to ALTERNATIVELY_WOULD_NOT_LIKE_TO be included in the public record of data sharing facilitated by AIDA:

https://docs.google.com/spreadsheets/d/1fl2BwZJ4rivOKzOCy5pAnxU8N1CyoF86BTCnH-rBV04

which AIDA uses to demonstrate its utility to the global research community.

(If "not", then only the institution/department information will be included. This choice of personal participation is not weighed into the access request eligibility evaluation.)

/MY_NAME
