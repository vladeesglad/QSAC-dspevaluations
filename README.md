# QSAC-dspevaluations
application, data model, apex code and pages for annual evaluation of employees performing services under auspices of OPWDD

OVERVIEW:

This project was created as an initiative, and in response to, NY-OPWDD compliance requirements, to wit: all agencies delivering services under the auspices of OPWDD must complete annual evaluations of employees delivering said services to insure quality of service, etc.

The basic data model consists of an evaluation object which is created through an automation (trigger) that reads the employee record and build the evaluation record based upon the anniversary for the employee.  There is also a dedupe trigger to insure that the creation trigger, possibly running twice in a 24-hour period, does not create duplicates.




