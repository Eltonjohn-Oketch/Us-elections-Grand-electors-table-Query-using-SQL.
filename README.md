# Us-elections-Grand-electors-table-Query-using-SQL.
# Introduction

I attempt to anaalyze & answer research questions on the US elections using SQL queries.
# Project Overview(Description)

Here is what we are suggesting to do: we will rank states by decreasing number of grand electors per capita. The first states in the list will be the most valuable (you get a large number of grand electors by convincing a small number of people to vote for you). We will target all the states at the top of the list until the cumulative sum (also called running total) of grand electors won is larger than half the total number of Grand Electors in the country

# Recording the Experimental Design

1.) To join the 2 tables:
You notice States are not capitalized the same way in both tables (one is in uppercase letters, the other not), so you will first need to convert all to uppercase, for instance.
Now you can join the tables on the state key.
2.) Your boss wants you to change the name of the "District of Columbia" state to its short version "DC". Please do that.
3.)To compute the ratio between the number of grand electors and the population. Please create a new column with that ratio.
4.)To order the states by decreasing ratio of Grand Electors per capita. That will make our priority list.
5.)To compute the running total of Grand Electors in that sorted list.
Hint: you can get inspiration from here to compute a running total from here:  https://stackoverflow.com/questions/21382766/cumulative-summing-values-in-sqliteLinks to an external site.
6.)Independently, to compute the half of the total of Grand Electors overall (in the whole country):
This is the threshold we need to reach for winning the presidential election.
7.)To filter our sorted list of states in order to keep only the (top) ones enabling us to reach the computed threshold. (the other states can be ignored). That is our target list.
Hint: You can do that in 2 steps:
Select all the states for which the running total is below or equal to the threshold.
Add the first state for which the running total is larger than the threshold.
Can you draw some conclusions from the result? Is it in line with your expectations? How many states do you end up with in the target list? Is it a small or a large number? Do you think it would be a good recommendation to target those states?
