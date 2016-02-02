# QSAC-dspevaluations
application, data model, apex code and pages for annual evaluation of employees performing services under auspices of OPWDD

for Visual Samples of the Work see: 'Visual Samples: Dropbox link'

OVERVIEW:

This project was created as an initiative, and in response to, NY-OPWDD compliance requirements, to wit: all agencies delivering services under the auspices of OPWDD must complete annual evaluations of employees delivering said services to insure quality of service, etc., and do so in such a manner that periodic audits of evaluations may be conducted by the Department.

Because the required evaluation record is a rather long and windy affair, consisting of something on the order of 100 user-entered data fields, certain stylings were added to the evaluation page that would permit the user to:

1) complete a partial eval and return later
2) upon return, highlight blank fields to enable visual scanning and parsing with some degree of efficiency

The basic data model was built on Force.com platform, and consists of an evaluation object which is created through an automation (trigger) that reads the employee record and builds the evaluation record based upon the anniversary for the employee.  There is also a dedupe trigger to insure that the creation trigger, possibly running twice in a 24-hour period due to batch jobs and whatnot, does not create duplicates.

There is test code to accompany the triggers; bear in mind however, that the test code is specific to an environment that includes a 3rd party application by Financial Force - HCM.  This application utilizes HCM objects and the test code is designed to replicate them, as well.  

The application also utilizes apex MetadataType records, which govern some of the CSS on the VisualForce page.  There is a proto-type .mdt object to permit limited manipulations of the page CSS using apex getters in the controller extension which references and uses the values set in the .mdt color styling record for this VisualForce page.  This permits manipulations of the page appearance without redeployment of code.









