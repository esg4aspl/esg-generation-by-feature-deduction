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

## Deducing Features from Full Product to Have a Defined Product Configuration

In the second experiment set of this study, 8 different base product are defined for this SPL. These base products includes one feature each from {accessCard, barcode, fingerprint, QRCode} or {email, SMS} feature sets and teacherAccess, studentAccess, viewRecord, viewClass, viewSchedule. Different product configurations are defined by adding feature sets (of size 3 that are consisting of random features) to these base products. The features to-be deduced to obtain the defined configurations, and the time it took to deduce these features are given in the table below. 

| Features to-be Deduced                                                                                               | fullProduct\_accessCardEmail | fullProduct\_accessCardSMS | fullProduct\_barcodeEmail |  fullProduct\_barcodeSMS | fullProduct\_barcodeEmail | fullProduct\_barcodeSMS | fullProduct\_barcodeEmail | fullProduct\_barcodeSMS |
| -------------------------------------------------------------------------------------------------------------------- | ---------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------------- | ----------------------- | ------------------------- | ----------------------- |
| addNewClass, addNewSchedule, deleteClass, updateClassDetail, editSchedule, assignNewSchedule                         | 13.65                        | 13.13                      | 14.56                     | 12.65                    | 12.95                     | 13.69                   | 14.27                     | 13.53                   |
| addNewClass,addNewSchedule,monitorAttendanceStatus, updateClassDetail,editSchedule,assignNewSchedule                 | 13.65                        | 13.34                      | 14.15                     | 12.48                    | 13.2                      | 12.4                    | 13.7                      | 13.02                   |
| addNewClass,addNewSchedule,updateClassDetail,editSchedule,traceAttendanceActivity, assignNewSchedule                 | 13.42                        | 13.06                      | 12.42                     | 13.56                    | 13.68                     | 13.55                   | 13.68                     | 13.21                   |
| addNewClass, deleteClass, monitorAttendanceStatus, updateClassDetail,editSchedule, assignNewSchedule                 | 14.05                        | 11.91                      | 12.08                     | 12.97                    | 13.09                     | 12.61                   | 11.93                     | 13.05                   |
| addNewClass, deleteClass, monitorAttendanceStatus, updateClassDetail, traceAttendanceActivity, assignNewSchedule     | 14.57                        | 12.39                      | 13                        | 12.81                    | 12.13                     | 12.55                   | 13.13                     | 12.07                   |
| addNewClass, deleteClass, updateClassDetail, editSchedule, traceAttendanceActivity, assignNewSchedule                | 15.22                        | 13.52                      | 11.73                     | 12.96                    | 12.87                     | 13.04                   | 12.74                     | 12.55                   |
| addNewClass,deleteClass, updateRecord, updateClassDetail, traceAttendanceActivity, assignNewSchedule                 | 14.08                        | 13.64                      | 13.04                     | 12.54                    | 12.52                     | 12.68                   | 12.64                     | 12.49                   |
| addNewClass, monitorAttendanceStatus, updateClassDetail, editSchedule, traceAttendanceActivity, assignNewSchedule    | 20.25                        | 12.75                      | 13.15                     | 12.48                    | 12.48                     | 12.09                   | 13.32                     | 12.29                   |
| addNewClass, updateRecord, monitorAttendanceStatus, updateClassDetail, traceAttendanceActivity, assignNewSchedule    | 13.96                        | 13.11                      | 12.52                     | 13.29                    | 12.65                     | 12.33                   | 12.97                     | 13.03                   |
| addNewClass, updateRecord, updateClassDetail, editSchedule, traceAttendanceActivity, assignNewSchedule               | 14.41                        | 14.35                      | 13.6                      | 13.16                    | 12.44                     | 13.06                   | 12.26                     | 13.66                   |
| addNewSchedule, deleteClass, monitorAttendanceStatus, editSchedule, traceAttendanceActivity, assignNewSchedule       | 15.07                        | 13.3                       | 12.39                     | 12.11                    | 12.54                     | 12.59                   | 12.76                     | 12.28                   |
| addNewSchedule, deleteClass, monitorAttendanceStatus, updateClassDetail, editSchedule, assignNewSchedule             | 15.82                        | 13.27                      | 17.19                     | 12.64                    | 12.54                     | 12.95                   | 13.25                     | 12.78                   |
| addNewSchedule, deleteClass, updateClassDetail, editSchedule, traceAttendanceActivity, assignNewSchedule             | 14.08                        | 14.27                      | 16.8                      | 12.39                    | 12.72                     | 12.04                   | 14.07                     | 12.95                   |
| addNewSchedule, deleteClass, updateRecord, editSchedule, traceAttendanceActivity, assignNewSchedule                  | 16.97                        | 13.73                      | 15.12                     | 13.33                    | 13.27                     | 13.19                   | 17.31                     | 13.18                   |
| addNewSchedule, monitorAttendanceStatus, updateClassDetail, editSchedule, traceAttendanceActivity, assignNewSchedule | 15.88                        | 12.76                      | 15.27                     | 12.97                    | 13.78                     | 12.02                   | 12.14                     | 12.82                   |
| addNewSchedule,updateRecord,monitorAttendanceStatus,editSchedule,traceAttendanceActivity,assignNewSchedule           | 14.28                        | 12.68                      | 13.12                     | 12.92                    | 12.55                     | 12.07                   | 12.5                      | 12.75                   |
| addNewSchedule,updateRecord,updateClassDetail,editSchedule,traceAttendanceActivity,assignNewSchedule                 | 15.26                        | 12.53                      | 12.95                     | 13.21                    | 13.2                      | 12.84                   | 12.79                     | 13.59                   |
| deleteClass,monitorAttendanceStatus,updateClassDetail,editSchedule,traceAttendanceActivity,assignNewSchedule         | 15.02                        | 12.81                      | 12.9                      | 13.53                    | 13.37                     | 12.27                   | 12.36                     | 12.59                   |
| deleteClass,updateRecord,monitorAttendanceStatus,editSchedule,traceAttendanceActivity,assignNewSchedule              | 15.29                        | 11.85                      | 13.13                     | 12.09                    | 11.74                     | 12.29                   | 12.82                     | 13.28                   |
| deleteClass,updateRecord,monitorAttendanceStatus,updateClassDetail,traceAttendanceActivity,assignNewSchedule         | 14.53                        | 12.84                      | 12.76                     | 13.31                    | 12.45                     | 12.48                   | 12.27                     | 13.36                   |
| deleteClass,updateRecord,updateClassDetail,editSchedule,traceAttendanceActivity,assignNewSchedule                    | 14.88                        | 13.88                      | 13.34                     | 12.37                    | 13.56                     | 13.07                   | 12.99                     | 13.61                   |
| updateRecord,monitorAttendanceStatus,updateClassDetail,editSchedule,traceAttendanceActivity,assignNewSchedule        | 14.11                        | 13.01                      | 12.97                     | 12.62                    | 12.7                      | 12.27                   | 13.1                      | 12.48                   |
