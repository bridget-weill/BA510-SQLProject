# Course Data Dictionary
__Bridget Weill & Chris Lametta__


## Class

| Key | Field | Definition | Type |
| :--- | :--- | :--- | :--- |
| PK | ClassID | ID number to specific class | Integer |
| FK | CourseCatalogID | ID number for course catalog| Integer |
| FK | ProfessorID | ID number identifying professor | Integer |
|-| CatalogID | ID number for each catalog |Text |
|-| Term | The length of time a course lasts | Text |
|-| CRN | Course Registration Number: Specific to an individual class | Integer |
|-| Section | An individual course offering, distinguished from other course sections | Integer |
|-| Credits | The recognition for having taken a course at school or university; measures if enough hours have been made for graduation | Integer |
|- | Title | Name of the class | Text |
|- | Timecodes | Code distinguishing time, location and date| Text |
|- | Meetings | Meeting code for days; Tuesday-Friday | Text |
| -| Capacity | Maximum number of students per class | Integer |
| -| Actual | Actual number of students enrolled in the class | Integer |
|- | Remaining | Remaining capacity for students to enroll in the class | Integer |

## CourseCatalog
| Key | Field | Definition | Type |
| :--- | :--- | :--- | :--- |
| PK | CourseCatalogID | ID value for each course catalog | Integer |
| FK | ProgramID | ID for program | Integer |
|- | CatalogID | ID for catalog | Text |
|- | Catalog_Year | The catalog by year | Text |
|- | Title | The title of the course | Text |
|- | Credits | Thr number of credits for each course | Text |
|- | Prereqs | Prereqs for the course | Text |
|- | Coreqs | Coreqs for the course | Text |
|- | Fees | Fees associated with the application | Text |
|- | Attributes | Signify a course meets a requirement, an emphasis area, or any other major/minor or program requirement | Text |
|- | Description | A short statement that informs a student about the subject matter, approach, applicability of the course | Text |

## Meeting
| Key | Field | Definition | Type |
| :--- | :--- | :--- | :--- |
| PK | MeetingID | Number identifying a meeting | Integer |
| FK | ClassID | Number identifying class | Integer |
| FK | LocationID | NUmber identifying location | Integer |
|- | Day | Day of the week in which the class meets |Text |
|- | StartTime | The time at which the class starts | Text |
|- | EndTime | The time at which the class ends  | Text |

## Program
| Key | Field | Definition | Type |
| :--- | :--- | :--- | :--- |
| PK | ProgramID | Number to identify program | Integer |
| FK | Program_Name | Name of the program | Text |
| FK | Program_Code | Code used for the program | Text |

## Location
| Key | Field | Definition | Type |
| :--- | :--- | :--- | :--- |
| PK | LocationID | Number to distinguish location | Integer |
|-| Location | The location of the class | Text |

## Professors
| Key | Field | Definition | Type |
| :--- | :--- | :--- | :--- |
| PK | ProfessorID | Number to distinguish the Professor | Integer |
|-| Name | Professor name | Text |


