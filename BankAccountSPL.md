# Generating Different Product Configurations by Deducting Features from the Full Product(s) of Bank Account SPL

Bank Account SPL has 9 features. The feature model given below is modified from, the core ESG model and, f-ESG models of this SPL are given [here](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/BankAccountSPL.md). There are 81 different product configurations belonging to this SPL.

![Feature Model](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/BankAccountSPL/Feature%20Model.PNG)

The number of nodes and the number of edges belonging to the c-ESG and the f-ESGs are given in the table below. 

| Feature            | Number of Nodes | Number of Edges |
| ------------------ | --------------- | --------------- |
| core               | 3               | 2               |
| deposit            | 8               | 9               |
| withdraw           | 8               | 9               |
| cancelDeposit      | 5               | 4               |
| cancelWithdraw     | 5               | 4               |
| interest           | 7               | 7               |
| interestEstimation | 6               | 5               |
| dailyLimit         | 8               | 11              |
| overdraft          | 8               | 10              |
| credit             | 7               | 7               |

[Click for the PDF version of the table](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/BankAccountSPL/FeatureData.pdf)

There are 2 different full products of this SPL due to the features that are connected with XOR. The number of nodes and the number of edges belonging to the 2 full products are given in the table below. 

| Full Product           | Number of Nodes | Number of Edges |
| ---------------------- | --------------- | --------------- |
| fullProduct\_overdraft | 20              | 37              |
| fullProduct\_credit    | 21              | 38              |

[Click for the PDF version of the table](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/BankAccountSPL/FullProductData.pdf)

The feature dependency tree of this SPL is shown below. The feature cancelDeposit depends on the feature deposit, the feature cancelWithdraw depends on the feature withdraw and, the feature interestEstimation depends on the feature interest. 
Moreover, the feature dailyLimit depends on the features wihtdraw and cancelWithdraw; and, the feature overdraft depends on the features cancelWithdraw and dailyLimit. 

![FeatureDependencyTree](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/BankAccountSPL/FeatureDependencyTree.png)

## Deducing Features from Full Product One-By-One
In the first experiment set of this study, the features are deduced from the full products one-by-one. The measured time(ms) results of this experiment are given below.

| Feature to-be Deduced | fullProduct\_overdraft | fullProduct\_credit |
| --------------------- | ---------------------- | ------------------- |
| cancelDeposit         | 9.24                   | 7.82                |
| cancelWithdraw        | 10.43                  | 10.73               |
| deposit               | 9.9                    | 10.41               |
| withdraw              | 10.66                  | 10.21               |
| interest              | 10.15                  | 10.81               |
| interestEstimation    | 7.2                    | 8.03                |
| dailyLimit            | 9.71                   | 7.68                |
| overdraft             | 7.34                   | \-                  |
| credit                | \-                     | 7.62                |

[Click for the PDF version of the table](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/BankAccountSPL/OneFeatureDeduction.pdf)

## Deducing Features from Full Product to Have a Defined Product Configuration

In the second experiment set of this study for Bank Account SPL, a base product that consists of the features deposit and withdraw in addition to the core is defined. Different product configurations are defined by adding feature sets (of size 3 that are consisting of random features) to this base product. The features to-be deduced to obtain the defined configurations, and the time it took to deduce these features are given in the tables below for fullProduct_overdraft and fullProduct_credit respectively. 

| Features to-be Deduced                            | fullProduct\_overdraft |
| ------------------------------------------------- | ---------------------- |
| cancelDeposit, cancelWithdraw, interestEstimation | 10.00                  |
| cancelDeposit, cancelWithdraw, overdraft          | 9.49                   |
| cancelDeposit, dailyLimit, overdraft              | 7.31                   |
| cancelDeposit, interest, interestEstimation       | 8.21                   |
| cancelDeposit, interestEstimation, overdraft      | 8.08                   |
| cancelDeposit, cancelWithdraw, dailyLimit         | 7.88                   |
| cancelDeposit, interestEstimation, dailyLimit     | 8.19                   |
| cancelWithdraw, dailyLimit, overdraft             | 7.84                   |
| cancelWithdraw, interest, interestEstimation      | 11.85                  |
| cancelWithdraw, interestEstimation, overdraft     | 10.67                  |
| cancelWithdraw, interestEstimation, dailyLimit    | 8.04                   |
| interest, interestEstimation, overdraft           | 8.10                   |
| interestEstimation, dailyLimit,overdraft          | 7.55                   |
| interest, interestEstimation, dailyLimit          | 8.05                   |

| Features to-be Deduced                            | fullProduct,\_credit |
| ------------------------------------------------- | -------------------- |
| cancelDeposit, cancelWithdraw, credit             | 7.83                 |
| cancelDeposit, cancelWithdraw, dailyLimit         | 7.37                 |
| cancelDeposit, cancelWithdraw, interestEstimation | 9.81                 |
| cancelDeposit, credit, dailyLimit                 | 7.94                 |
| cancelDeposit, credit, interestEstimation         | 7.53                 |
| cancelDeposit, interest, interestEstimation       | 9.79                 |
| cancelDeposit,interestEstimation, dailyLimit      | 7.82                 |
| cancelWithdraw, credit, dailyLimit                | 6.76                 |
| cancelWithdraw, credit, interestEstimation        | 8.09                 |
| cancelWithdraw, interest, interestEstimation      | 7.50                 |
| cancelWithdraw, interestEstimation, dailyLimit    | 6.37                 |
| credit, interest, interestEstimation              | 6.01                 |
| credit, interestEstimation, dailyLimit            | 5.81                 |
| interest, interestEstimation, dailyLimit          | 5.77                 |

[Click for the PDF version of the tables](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/BankAccountSPL/FeatureSetDeduction.pdf)
