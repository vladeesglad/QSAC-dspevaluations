# QSAC-dspevaluations
application, data model, apex code and pages for annual evaluation of employees performing services under auspices of OPWDD

OVERVIEW:

This project was created as an initiative, and in response to, NY-OPWDD compliance requirements, to wit: all agencies delivering services under the auspices of OPWDD must complete annual evaluations of employees delivering said services to insure quality of service, etc., and do so in such a manner that period audits of evaluations may be conducted by the Department.

The basic data model was built on Force.com platform, and consists of an evaluation object which is created through an automation (trigger) that reads the employee record and builds the evaluation record based upon the anniversary for the employee.  There is also a dedupe trigger to insure that the creation trigger, possibly running twice in a 24-hour period, does not create duplicates.

There is test code to accompany the triggers; bear in mind however, that the test code is specific to an environment that includes a 3rd party application by Financial Force - HCM.  This application utilizes HCM objects and the test code is designed to replicate them, as well.  










