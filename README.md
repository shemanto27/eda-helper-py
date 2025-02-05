# EDA Helper Function - Boost your Exploretory Data Analysis Process!


## Credit

- I first came to this idea of using helper function from a course by [@MisbahullahSheriff](https://github.com/MisbahullahSheriff) and it was brilliant. This EDA helper function originally was created by [@MisbahullahSheriff](https://github.com/MisbahullahSheriff). Now I have edited the file and organized it for easy to use.Extra functions has been added by me.


## Installation

Use in Google Colab: put the fill in the notebook's directory

```bash
import google.colab.drive as drive
drive.mount('/content/drive', force_remount=True)

import sys
import os
sys.path.append('<your_directory>')
import eda_helper_functions as ehf
```
    
## Step-by-Step EDA

-  Import Libraries

-  Read `training` dataset, we perform EDA only on `training` dataset

- High-level Analysis
    - Data Summary:
        - .info() method
        - .describe() method on `numeric` and `categorical` features separately

    - Missing Data:
        - find missing value with number and percentages

            ```bash
                ehf.missing_info(df)
            ```
        - bar plot for better visualization of missing data
        
             ```bash
                ehf.plot_missing_info(df)
            ```
    
    - Outliers:
        - Isolation forest

    - Pair plots:
        ```bash
            ehf.pair_plots(df)
        ```

    - Correlation Analysis(heatmaps):
        - Numeric(Pearson's/Spearman's)
        - Categorical(Cramer's V)

        ```bash
            ehf.correlation_heatmap(df)
        ```

        ```bash
            ehf.cramersV_heatmap(df)
        ```



- Detailed Analysis of each Columns

    ```bash
        df.columns # find all columns   
    ```
    - Summary

        ```bash
            ehf.cat_summary(df, "<cat_feature>")
        ```

    - Univariate plots

        ```bash
            ehf.cat_univar_plots(df, "<cat_feature>")
        ```
    - Bivariate plots

        ```bash
            ehf.num_cat_bivar_plots(
            data=train,
            num_var="<num_feature>",
            cat_var="<cat_feature>"
            )
        ```
    - Hypothesis Testing(normality, strength of association)

        ```bash
            ehf.num_cat_bivar_plots(
            data=train,
            num_var="<num_feature>",
            cat_var="<cat_feature>"
            )
        ```    
