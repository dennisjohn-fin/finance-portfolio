**Prompt 1**

Scan the 'P\&L' sheet for formulas that contain hardcoded constants (e.g. \*0.2 or +5000).

Create a table in new sheet 'constants\_audit' with:

\- cell address

\- original formula

\- detected constant

\- suggested named assumption

\- fixed formula using 'assumptions'! range

Also summarize:

\- total constants found

\- top 3 most reused constants.



**Prompt 2**



These are the fixes to be executed as per your review:

1\. tax should be 25% of pre-tax profit on all rows 

2\. opex errors on the detected columns should be adjusted as per the audited formula

3\. cash flow calculation is to follow the formula, cash\_flow = net\_income + depreciation - capex



Make these modifications and document these changes in "tblConstantsAudit" table and "constants\_audit" sheet.



After these steps are complete, 

Update the 'assumptions' sheet to reflect the complete list of assumptions. Replace the detected constants in the original 'P\&L' sheet using the suggested formulas and assumptions that trace back to the 'Assumptions'! list/table.



**Prompt 3**



The additional fix is as follows:

Calculate a pre-tax profit (EBITDA minus depreciation minus interest) after column H. Tax is currently in column I and net income in column J.



Right now tax is calculated as simply 25% of pre-tax profit every month. That's wrong, because when the company makes a loss, it shouldn't pay tax — it should carry that loss forward and use it to reduce tax in future profitable months. I need you to fix this.



Please do the following:

Add two new columns to the right of the table 'tblPL':



1\. 'tax\_loss\_crfwd' — Tax Loss Carry forward  which is the accumulated unused losses remaining at the end of each month.

2\. 'dta' — which is the Deferred Tax Asset (DTA) the value of those losses at the 25% tax rate.



Recalculate the Tax column and Net Income column using these rules:



If pre-tax profit is negative (a loss):



tax = 0

Add the full loss to the tax loss carryforward

Recognise a deferred tax asset of 25% of the loss (this is a credit that reduces the loss on the income statement)

Tax expense line = negative (a benefit)

Net income = pre-tax profit minus the tax benefit (so the loss is smaller after the tax credit)



If pre-tax profit is positive (a profit):



First, use any available tax loss carryforward to offset the profit

Taxable income = profit minus losses used

Cash tax paid = taxable income × 25%

Reduce the tax loss carryforward by the amount used

Deferred tax expense = the drop in the DTA balance for that month

Total tax expense = cash tax + deferred tax expense

Net income = pre-tax profit minus total tax expense



When all losses are used up:



Tax loss carryforward = 0

DTA = 0

Tax = pre-tax profit × 25%

Net income = pre-tax profit minus tax

refer the 25% tax rate from the assumption sheet. 



Show me the recalculated Tax, Net Income, Tax Loss Carryforward, and DTA for every row, and confirm that the final DTA balance equals the remaining unused losses × 25%(tax rate).



If anything is unclear in my layout, ask me before making changes.

log these changes in the 'constants\_audit' sheeet



