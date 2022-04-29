# Generating Different Product Configurations by Deducting Features from the Full Product(s) of Student Attendance System SPL

Student Attendance System SPL has 20 features. The feature model, the core ESG model and, f-ESG models of this SPL are given [here](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/StudentAttendanceSystemSPL.md). There are 2664 different product configurations belonging to this SPL. The number of nodes and the number of edges belonging to the c-ESG and the f-ESGs are given in the table below. 

| Feature                 | Number of Nodes | Number of Edges |
| ----------------------- | ----------- | ----------- |
| core                    | 7           | 5           |
| studentAccess           | 6           | 6           |
| teacherAccess           | 7           | 7           |
| accessCard              | 5           | 5           |
| barcode                 | 6           | 8           |
| fingerprint             | 5           | 5           |
| QRCode                  | 5           | 5           |
| email                   | 5           | 4           |
| SMS                     | 5           | 4           |
| viewRecord              | 6           | 5           |
| updateRecord            | 8           | 8           |
| monitorAttendanceStatus | 5           | 4           |
| traceAttendanceActivity | 5           | 4           |
| viewClass               | 6           | 5           |
| addNewClass             | 8           | 12          |
| updateClassDetail       | 7           | 11          |
| deleteClass             | 7           | 7           |
| viewSchedule            | 6           | 5           |
| addNewSchedule          | 8           | 12          |
| editSchedule            | 7           | 11          |
| assignNewSchedule       | 6           | 6           |

There are 8 different full products of this SPL due to the features that are connected with XOR. The number of nodes and the number of edges belonging to the 8 full products are given in the table below. 

| Full Product                   | Number of Nodes | Number of Edges |
| ------------------------------ | ----------- | ----------- |
| fullProduct\_accessCardEmail   | 45          | 84          |
| fullProduct\_accessCardSMS     | 45          | 84          |
| fullProduct\_barcodeEmail      | 46          | 87          |
| fullProduct\_barcodeSMS        | 46          | 87          |
| fullProduct\_ fingerprintEmail | 45          | 84          |
| fullProduct\_fingerprintSMS    | 45          | 84          |
| fullProduct\_QRCodeEmail       | 45          | 84          |
| fullProduct\_QRCodeSMS         | 45          | 84          |

The feature dependency tree is shown below. 
![FeatureDependencyTree](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/StudentAttendanceSystemSPL/FeatureDependencyTree.png)
