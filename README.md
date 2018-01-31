# Budget Project

## Requirements:
* Automatically keep track of all my purchases and expenses
* Automatically keep track of all my income
* Be able to send notifications (email, phone, pushbullet)
* Calculate a burn rate
* Know how much I should spend in certain categories (pie chart)
* Tell what category a transaction falls under
* Know how much I should be saving
* Tell me whether or not I'm on track for the month
* Output how much to put away
  * Maybe automatically put this amount away
* Output how much is left in the budget for certain categories

## Implementation:
1/29/2018:
This is where things get a little tricky. After all, I don't know too much about database design, which I would likely implement for storing transaction data, and I don't know how to get the transaction data in the database in the first place without requiring me to actually touch the DB. These being the magic things though, the top-down view looks like this:

### Unautomated portion
1. User defines budget percentages
### Income portion
1. Income comes in -> (receive notification) -> store income data in database -> collect average income
2. Calculate budget using user-defined percentages
Repeat whenever 1 happens
### Transaction portion
1. Transaction occurs -> store transaction data in database
2. Subtract transaction from calculated categorized budget amount -> (receive notification "you have x left in groceries")
### Scheduled portion
1. User defines schedule
2. At defined date, receive notification to put away savings
### Reporting
Know and be able to view at all times:
* How much each budget line accounts for
* How much each transaction in a budget category totals
* Total amount of money I have
* How much I expect to save at the end of the month (or scheduled time)
* My burn rate

The above is basically a wish list, as actually implementing this requires a lot of moving parts. I'm excited to take up this project, and I'm excited that there's so much to learn here.
Some things I need to check out: 
* yodlee, which should be able to provide transaction data
* SQL, so I can actually learn how to design databases

Bye for now!

Brandon Choi


1/31/2018:

This project is holding until I finish exams. Till then, I'm using Mint, which makes use of yodlee to get transaction data. Interesting features of Mint are:

Goals: Mint is able to track goals like student loans, and is able to link my Nelnet account to tell how far along I am with my loans. Can yodlee do this?

Things I'd like Mint to do:

Either: Scale my budget (including savings) to the amount of income I have
Or: be able to tell that I'm earning extra, then add that amount to the amount I should save
In eiher case, Mint doesn't do anything with the extra income I have that's not accounted for in my budget.

Daily burn rate/
Max burn rate
