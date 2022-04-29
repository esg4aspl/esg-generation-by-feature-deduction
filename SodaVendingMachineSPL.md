# Generating Different Product Configurations by Deducting Features from the Full Product(s) of Soda Vending Machine SPL

Soda Vending Machine SPL has 6 features. The feature model, the core ESG model and, f-ESG models of this SPL are given [here](https://github.com/esg4aspl/SPL-FESG-Examples/blob/master/SodaVendingMachineSPL.md). 
There are 39 different product configurations belonging to this SPL. 
The number of nodes and the number of edges belonging to the c-ESG and the f-ESGs are given in the table below. 

| Feature   | Number of Nodes | Number of Edges |
| --------- | --------------- | --------------- |
| core      | 4               | 1               |
| serveSoda | 4               | 4               |
| serveTea  | 4               | 4               |
| payEUR    | 4               | 4               |
| payUSD    | 4               | 4               |
| free      | 4               | 4               |
| cancel    | 7               | 7               |

[Click for the PDF version of the table](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/SodaVendingMachineSPL/FeatureData.pdf)

There is one full product of this SPL. The number of nodes and the number of edges belonging to the full product are given in the table below. 

| Full Product | Number of Nodes | Number of Edges |
| ------------ | --------------- | --------------- |
| fullProduct  | 11              | 15              |

[Click for the PDF version of the table](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/SodaVendingMachineSPL/FullProductData.pdf)

The feature dependency tree of this SPL is shown below. The feature cancel depends on the features payEUR and payUSD and, all the other features depend on the core in this SPL. 

![FeatureDependencyTree](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/SodaVendingMachineSPL/FeatureDependencyTree.png)

## Deducing Features from Full Product One-By-One
In the first experiment set of this study, the features are deduced from the full products one-by-one. The measured time(ms) results of this experiment are given below.

| Feature to-be Deduced | fullProduct |
| --------------------- | ----------- |
| payEUR                | 8.37        |
| payUSD                | 8.5         |
| cancel                | 6.12        |
| serveSoda             | 5.92        |
| serveTea              | 5.7         |
| free                  | 6.07        |

[Click for the PDF version of the table](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/SodaVendingMachineSPL/OneFeatureDeduction.pdf)

## Deducing Features from Full Product to Have a Defined Product Configuration

In the second experiment set of this study for  Soda Vending Machine SPL, a base product that consists of the features payEUR and serveSoda in addition to the core is defined. 
Different product configurations are defined by adding feature sets (of size 3 that are consisting of random features) to this base product. The features that are added to the base product, the features to-be deduced to obtain the defined configurations, and the time it took to deduce these features are given in the table below. 

| Features Added To The Base Product | Feature to-be Deduced | fullProduct |
| ---------------------------------- | --------------------- | ----------- |
| serveTea,cancel,free               | payUSD                | 8.5         |
| payUSD,serveTea,free               | cancel                | 6.12        |
| payUSD,cancel, free                | serveTea              | 5.7         |
| payUSD,serveTea,cancel             | free                  | 6.07        |

[Click for the PDF version of the tables](https://github.com/esg4aspl/esg-generation-by-feature-deduction/blob/main/SodaVendingMachineSPL/FeatureSetDeduction.pdf)
