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

The feature dependency tree of this SPL is shown below. The features addNewClass, addNewSchedule, deleteClass and, updateRecord depend on the feature teacherAccess; the features viewRecord and  monitorAttendanceStatus depend on the feature studentAccess; and the feature traceAttendanceActivity depends on updateRecord. Additionally, while the feature updateClassDetail depends on the features addNewClass and teacherAccess; the feature editSchedule depends on the features addNewSchedule and teacherAccess. Finally, the feature assignNewSchedule depends on the features addNewSchedule, updateClassDetail and, editSchedule. 

![FeatureDependencyTree](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/StudentAttendanceSystemSPL/FeatureDependencyTree.png)

## Deducing Features from Full Product One-By-One
In the first experiment set of this study, the features are deduced from the full product one-by-one. The measured time(ms) results of this experiment are given below.

| Feature to-be Deduced   | fullProduct\_accessCardEmail | fullProduct\_accessCardSMS | fullProduct\_barcodeEmail |  fullProduct\_barcodeSMS | fullProduct\_barcodeEmail | fullProduct\_barcodeSMS | fullProduct\_barcodeEmail | fullProduct\_barcodeSMS |
| ----------------------- | ---------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------------- | ----------------------- | ------------------------- | ----------------------- |
| addNewClass             | 17.03                        | 15.69                      | 14.87                     | 14.17                    | 14.93                     | 15.28                   | 15.27                     | 16.39                   |
| addNewSchedule          | 16.94                        | 15.89                      | 16.08                     | 14.81                    | 14.59                     | 14.9                    | 14.7                      | 15.56                   |
| assignNewSchedule       | 11.74                        | 11.23                      | 11.89                     | 14.21                    | 11.18                     | 13.25                   | 11.93                     | 11.48                   |
| deleteClass             | 13                           | 11.52                      | 11.62                     | 10.9                     | 10.85                     | 12.52                   | 11.32                     | 12.08                   |
| editSchedule            | 23.94                        | 14.19                      | 14.41                     | 14.27                    | 14.67                     | 14.45                   | 16.67                     | 14.9                    |
| monitorAttendanceStatus | 13.72                        | 11.64                      | 11.93                     | 11.38                    | 11.08                     | 12.18                   | 11.31                     | 11.46                   |
| studentAccess           | 16.68                        | 14.63                      | 14.21                     | 15.02                    | 14.46                     | 15                      | 14.59                     | 14.98                   |
| teacherAccess           | 17.89                        | 16.81                      | 16.95                     | 16.48                    | 16.3                      | 17.07                   | 19.11                     | 15.72                   |
| traceAttendanceActivity | 13.2                         | 12.94                      | 11.49                     | 11.08                    | 11.77                     | 11.64                   | 11.65                     | 11.17                   |
| updateClassDetail       | 15.97                        | 14.69                      | 14.39                     | 16.43                    | 15.19                     | 14.64                   | 14.1                      | 14.33                   |
| updateRecord            | 19.93                        | 14.33                      | 14.1                      | 13.92                    | 13.73                     | 14.12                   | 14.35                     | 18.46                   |
| viewClass               | 12.67                        | 12.44                      | 12.16                     | 11.66                    | 11.18                     | 11.38                   | 11.65                     | 11.45                   |
| viewRecord              | 12.92                        | 10.96                      | 11.42                     | 11.08                    | 11.61                     | 11.69                   | 11.65                     | 11.69                   |
| viewSchedule            | 12.63                        | 11.14                      | 10.87                     | 11.14                    | 11.11                     | 11.28                   | 11.94                     | 12.49                   |
