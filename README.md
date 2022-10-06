# kickstarter-analysis

## To gain insights into crowdfunding campaigns using a multi-dimensional raw data set

## Ultimately the goal is to provide Louise with some key insights for her own kickstarter campaign


### We performed 2 analyses:

###  1)  Successful theater campaigns as a function of launch date and category: ![image](https://user-images.githubusercontent.com/114181709/194191370-5599b8a7-745d-46b6-afd1-2db26a35ff4d.png)
We were able to gain this insight by using a Pivot Table to filter our initial raw data by "Parent Category" = "theater", "Months" and "outcomes" = "successful", "failed" or "canceled".
This enabled us to see that campaigns launched during the span of March to September have been more successful, with the most success found in campaigns launched in  May. 

###  2) Successful campaigns as a function of funding goals: ![image](https://user-images.githubusercontent.com/114181709/194192239-9f7b4921-1598-4c89-8278-a500b8d4488c.png)
In this case we used a "countifs" formula to filter our data by "Subcategory" = "plays", Numerical ranges of funding goals and "outcomes". This created some challenges because we weren't able to define a numerical range within column A of our "Outcomes Based on Goals" worksheet. Consequently, we had to use less efficient logic. To illustrate, to count the number of successful campaigns with a funding goal between $1,000 and $4,999, we had to count the number of successful campaigns with a funding goal < $5,000, and then subtract from that result the number of successful campaigns with a goal < $1,000. We repeated this formula for our entire data table. Here's the formula that was used to find all failed campaigns with a funding goal between $45,000 and $49,000: =COUNTIFS('Raw Data'!P2:P4115, "plays", 'Raw Data'!F2:F4115, "failed", 'Raw Data'!D2:D4115,A12) - C11 - C10 -C9- C8 - C7 - C6 - C5 - C4 - C3 - C2, where Cn is the result from the previous range.


### To conclude, we are able to recommend that Louise ought to seek less than $1,000 and to launch the campaign during May. However, this is obviously not a guarantee of a successful campaign. It would help to have a feedback from the "funders" about each campaign and their decision to donate. This can provide more precise data around which Louise can actually structure her project.
[Kickstarter Challenge.xlsx](https://github.com/bpietrancosta/kickstarter-analysis/files/9720189/Kickstarter.Challenge.xlsx)
