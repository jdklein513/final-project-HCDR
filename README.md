# Home Credit Default Risk

## Synopsis

Certain consumers throughout the United States struggle to receive loan support from banks due to lacking credit history. Banks are uncertain if the demographic can repay loans they are seeking. Home Credit is a service whose goal is to provide loan opportunities for this underserved population. Failing to build and implement an accurate model to predict repayment assumes major consequences. There is missed financial interest opportunity if a consumer will pay the loan and they are denied. Consequently, if a loan is granted to a consumer likely to default, Home Credit may not recoup the principal. Home Credit supplements internal credit and loan history data with third party credit and loan history data to more accurately determine a consumer's likelihood to repay a loan. Several machine learning algorithms such as logistic regression and tree-based regression fit on the combined data features are compared to assess prediction accuracy on unseen loan applications. The current Kaggle leading model generates an out-of-sample area under the ROC curve of .805.

## Repo Structure

+ **adhoc**: stores any ad hoc code used to perform the exploratory data analysis on available HCDR data sources. This is generally code for one time tasks like exploration or data prep.

+ **code**: stores notebook code for business understanding, data understanding, data preparation, modeling, evaluation, and kaggle contest submission.

+ **data**: stores the HCDR data extracted from the kaggle competition. The descriptions below are provided via the kaggle competition.

    + application_{train|test}.csv: This is the main table, broken into two files for Train (with TARGET) and Test (without TARGET). Static data for all applications. One row represents one loan in our data sample.

    + bureau.csv: All client's previous credits provided by other financial institutions that were reported to Credit Bureau (for clients who have a loan in our sample). For every loan in our sample, there are as many rows as number of credits the client had in Credit Bureau before the application date.

    + bureau_balance.csv: Monthly balances of previous credits in Credit Bureau. This table has one row for each month of history of every previous credit reported to Credit Bureau - i.e the table has (#loans in sample * # of relative previous credits * # of months where we have some history observable for the previous credits) rows.

    + POS_CASH_balance.csv: Monthly balance snapshots of previous POS (point of sales) and cash loans that the applicant had with Home Credit. This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample - i.e. the table has (#loans in sample * # of relative previous credits * # of months in which we have some history observable for the previous credits) rows.

    + credit_card_balance.csv: Monthly balance snapshots of previous credit cards that the applicant has with Home Credit. This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample - i.e. the table has (#loans in sample * # of relative previous credit cards * # of months where we have some history observable for the previous credit card) rows.

    + previous_application.csv: All previous applications for Home Credit loans of clients who have loans in our sample. There is one row for each previous application related to loans in our data sample.

    + installments_payments.csv: Repayment history for the previously disbursed credits in Home Credit related to the loans in our sample. There is a) one row for every payment that was made plus b) one row each for missed payment. One row is equivalent to one payment of one installment OR one installment corresponding to one payment of one previous Home Credit credit related to loans in our sample.
    
    + HomeCredit_columns_description.csv: This file contains descriptions for the columns in the various data files.

+ **output**: sore the reports, presentations, models, and plot output from the code section of the repo.

    + models: current and archived model objects
    + reports: html notebook output with analysis and model results
    + presentations: final powerpoint presentations for delivering results
    + plots: plots generated throughout EDA and modeling
    + images: images embedded in code

## How to run code

This repo is currently under development and this section will be updated at a later date.

## Contributors

* Joel Klein (joeklein@iu.edu)
* Rakesh Jothishankar (rjothis@iu.edu)
* Suriyadeepan Narayanasamy (sunara@iu.edu)
* Ashley Thornton (ashthorn@iu.edu)
