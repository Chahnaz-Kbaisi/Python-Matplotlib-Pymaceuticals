# Matplotlib - The Power of Plots
![Lab](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/Laboratory.jpg)


The [analysis](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/tree/main/Pymaceuticals) described here was performed for Pymaceuticals Inc., a San Diego-based pharmaceutical company specializing in anti-cancer treatments, to clarify the efficacy of several skin cancer drugs on the size of tumors in mice. 

The purpose of this analysis was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. A technical report, which included tables and figures showing relative responses, was generated and delievered to the executive team with a top-level summary of the results.

[Pymaceuticals jupyter notebook](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Pymaceuticals/pymaceuticals.ipynb) analysis included the following steps: 

* Checked the data for any mouse ID with duplicate time points and removed any data associated with that mouse ID.

* Cleaned data for the remaining steps.

* Generated a summary statistics table consisting of the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

* Generated a [bar plot](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/pandas_bar_plot.png) using both Pandas's `DataFrame.plot()` and [Matplotlib's](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/pyplot_bar_plot.png) `pyplot` that shows the number of total mice for each treatment regimen throughout the course of the study.

![Bar Plot](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/pandas_bar_plot.png)

* Generated a [pie plot](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/pie_plot_pandas.png) using both Pandas's `DataFrame.plot()` and [Matplotlib's](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/pie_plot_pyplot.png) `pyplot` that shows the distribution of female or male mice in the study.


* Calculated the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. 

* Calculated the quartiles and IQR and quantitatively determined if there are any potential outliers across all four treatment regimens.

* Using Matplotlib, generated a [box and whisker plot](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/final_tumor_reg_box.png) of the final tumor volume for all four treatment regimens and highlighted any potential outliers in the plot by changing their color and style.

* Selected a mouse that was treated with Capomulin and generated a [line plot](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/capomulin_l509_line.png) of tumor volume vs. time point for that mouse.

* Generated a [scatter plot](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/tumor_weight_scatter.png) of mouse weight versus average tumor volume for the Capomulin treatment regimen.

* Calculated the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. Plotted the [linear regression](https://github.com/Chahnaz-Kbaisi/Python-Matplotlib-Pymaceuticals/blob/main/Images/linear_regression.png) model on top of the previous scatter plot.


## Observations and Insights
***
1. Capomulin and Ramicane both had a greater effect on final tumor volume than Infubinol and Ceftamin, and the data for them was less dispersed, which means there was more variability. Only Infubinol had an outlier with drastic tumor reduction, however this does not indicate drug efficacy. Both Capomulin and Ceftamin are negatively skewed while Infubinal and Ramicane are symmetrical in their data distribution.  

2. For Capomulin it seems drug efficacy is dependent on building up to a certain dosage, such that at day 20 the tumor volume decreased drastically over the next 4 to 5 days. Then, a second phase of tumor reduction occurs thereafter. From this individual mouse it looks like the effects of Capomulin are quite rapid once it reaches the necessary dose in the body. 

3. Tumor volume is positively correlated with mouse weight. So, as the mouse grows, so does the tumor. The slope of the regression (0.95, close to 1) shows that tumor volume is proportional to to body weight. Finally, above 18g of body weight, the volume of the tumors appears to increase more drastically (i.e., at 17g there were a few smaller tumors and some larger ones).

