Problem Set 1
Statistics and Econometrics
Due: 12pm, 4 November 2019
General Guideline
$ % What we are looking for in the assignments is a demonstration that you can understand the econometrics
and statistics questions and can use R to solve them. That means effective programming to get correct results
is needed, but at the same time, clear explanations of economics/business concepts in well presented reports
are equally important when assessing your work. In particular, you will be marked for successful (correct)
programming (not the style of coding), good understanding of related concepts, and clear interpretations
and explanations of results.
Only two forms of reports will be accepted, either pdf or html. We strongly suggest you to submit the pdf
or html converted from R markdown/notebook after you program in R. Please submit both the source code
and pdf/html file.
Question 1
The data set ceosal2.RData contains information on chief executive officers for U.S. corporations. Two
variables of interest are the annual compensation (salary) and the prior number of years as company CEO
(ceoten).
1. Find the average salary and the average tenure in the sample.
2. How many CEOs are in their first year as CEO (that is, ceoten = 0)? What is the longest tenure as a
CEO?
3. What is the average salary for CEOs with tenure longer than or equal to the average tenure? What is
the average salary for CEOs with tenure shorter than the average tenure?
4. Create a graph to examine the relationship between salary and ceoten for all CEOs. Comment.
5. Estimate the simple regression model
log(salary) = 0 + 1ceoten + u,
and report your results. What is the (approximate) predicted percentage increase in salary given one
more year as a CEO?
Question 2
The data set bwght.RData contains data on births to women in the United States. Two variables of interest
are the infant birth weight in ounces (bwght), and the average number of cigarettes the mother smoked per
day during pregnancy (cigs).
1. Estimate the simple regression model
bwght = 0 + 1cigs + u,
and report your results.
2. What is the predicted birth weight when cigs = 0? What about when cigs = 20 (one pack per day)?
Comment on the difference.
3. Does this simple regression necessarily capture a causal relationship between the child’s birth weight
and the mother’s smoking habits? Explain.
4. To predict a birth weight of 125 ounces, what would cigs have to be? Comment.
5. The proportion of women in the sample who do not smoke while pregnant is about 85%. Does this
reconcile your finding from part 4?

Problem Set 2
Statistics and Econometrics
Due: 12pm, 11 November 2019
General Guideline
What we are looking for in the assignments is a demonstration that you can understand the econometrics and
statistics questions and can use R to solve them. That means effective programming to get correct results is
needed, but at the same time, clear explanations of economics/business concepts in well presented reports
are equally important when assessing your work. In particular, you will be marked for successful (correct)
programming (not the style of coding), good understanding of related concepts, and clear interpretations and
explanations of results.
Only two forms of reports will be accepted, either pdf or html. We strongly suggest you to submit the pdf or
html converted from R markdown/notebook after you program in R. Please submit both the source code and
pdf/html file.
Question 1
Using the data set ceosal1.RData to answer the following questions. Consider an equation to explain salaries
of CEOs in terms of annual firm sales, return on equity (roe, in percentage form), and return on the firm’s
stock (ros, in percentage form):
log(salary) = 0 + 1 log(sales) + 2roe + 3ros + u
1. In terms of the model parameters, state the null hypothesis that, after controlling for sales and roe,
ros has no effect on CEO salary. State the alternative that better stock market performance increases
a CEO’s salary.
2. Estimate the model and report your results. By what percentage is salary predicted to increase if
ros increases by 50 basis points (i.e., ros increases by 50)? Does ros have a practically large effect on
salary?
3. Test the null hypothesis that ros has no effect on salary against the alternative that ros has a positive
effect. Carry out the test at the 10% significance level (please show clearly the test statistic and the
critical value used in your testing).
4. Would you include ros in a final model explaining CEO compensation in terms of firm performance?
Explain.
Question 2
Use the data set lawsch85.RData to answer the following questions. Consider an equation to explain the
median starting salary for new law school graduates
log(salary) = 0 + 1LSAT + 2GPA + 3 log(libvol) + 4 log(cost) + 5rank + u,
where LSAT is the median LSAT score for the graduating class, GPA is the median college GPA for the
class, libvol is the number of volumes in the law school library, cost is the annual cost of attending law school,
and rank is a law school ranking (with rank = 1 being the best).
1. Estimate the model. State and test the null hypothesis that the rank of law schools has no causal effect
on median starting salary (please show clearly the test statistic and the critical value used in your
testing).
2. Are features of students - namely, LSAT and GPA - individually or jointly significant for explaining
salary?
3. Test whether the size of the class (clsize) or the size of the faculty (faculty) needs to be added to this
equation: carry out a single test for joint significance of the two variables.

Problem Set 3
Statistics and Econometrics
Due: 12pm, 18 November 2019
General Guideline
What we are looking for in the assignments is a demonstration that you can understand the econometrics and
statistics questions and can use R to solve them. That means effective programming to get correct results is
needed, but at the same time, clear explanations of economics/business concepts in well presented reports
are equally important when assessing your work. In particular, you will be marked for successful (correct)
programming (not the style of coding), good understanding of related concepts, and clear interpretations and
explanations of results.
Only two forms of reports will be accepted, either pdf or html. We strongly suggest you to submit the pdf or
html converted from R markdown/notebook after you program in R. Please submit both the source code and
pdf/html file.
Question 1
Suppose you collect data from a survey on wages, education, experience, and gender. In addition, you ask for
information about marijuana usage. The original question is: “On how many separate occasions last month
did you smoke marijuana?"
1. Write an equation that would allow you to estimate the effects of marijuana usage on wage, while
controlling for other factors. You should be able to make statements such as, “Smoking marijuana five
more times per month is estimated to change wage by x%."
2. Write a model that would allow you to test whether drug usage has different effects on wages for men
and women. How would you test that there are no differences in the effects of drug usage for men and
women?
3. Suppose you think it is better to measure marijuana usage by putting people into one of four categories:
nonuser, light user (1 to 5 times per month), moderate user (6 to 10 times per month), and heavy
user (more than 10 times per month). Now, write a model that allows you to estimate the effects of
marijuana usage on wage.
4. Using the model in part 3, explain in detail how to test the null hypothesis that marijuana usage has
no effect on wage.
5. What are some potential problems with drawing causal inference using the survey data that you
collected?
Question 2
Use the data in bwght2.RData for this exercise.
1. Estimate the quation
log(bwght) = 0 + 1npvis + 2npvis2 + u
by OLS, and report the results. Is the quadratic term significant?
2. Show that, based on the equation from part 1, the number of prenatal visits that maximizes log(bwght)
is estimated to be about 22. How many women had at least 22 prenatal visits in the sample?
3. Does it make sense that birth weight is actually predicted to decline after 22 prenatal visits? Explain.

4. Add mother’s age to the equation, using a quadratic functional form. Holding npvis fixed, at what
mother’s age is the birth weight of the child maximized? What fraction of women in the sample are
older than the “optimal” age?
5. Would you say that mother’s age and number of prenatal visits explain a lot of the variation in
log(bwght)?

Problem Set 4
Statistics and Econometrics
Due: 12pm, 25 November 2019
General Guideline
What we are looking for in the assignments is a demonstration that you can understand the econometrics and
statistics questions and can use R to solve them. That means effective programming to get correct results is
needed, but at the same time, clear explanations of economics/business concepts in well presented reports
are equally important when assessing your work. In particular, you will be marked for successful (correct)
programming (not the style of coding), good understanding of related concepts, and clear interpretations and
explanations of results.
Only two forms of reports will be accepted, either pdf or html. We strongly suggest you to submit the pdf or
html converted from R markdown/notebook after you program in R. Please submit both the source code and
pdf/html file.
Question 1
Use the data set nbasal.RData to answer this question. A regression model is needed to study the factors
that influence salaries of NBA players. We use log(wage) as the dependent variable. Potential factors
that will affect a player’s wage include experience (exper, coll), games’ participation (games, avgmin),
position (forward, center, guard), performance (points, rebounds, assists), prestige (draft, allstar), and
demographic factors (black, children, marr). For this question, it is fine if you only consider these variables
in the level form.
1. Identify if there is any multicollinearity problem.
2. Find the model(s) with the lowest AIC by using forward and backward-stepwise selections.
3. Plot residuals against fitted values of model(s) from part 2. Is the residual plot satisfactory? Comment.
4. Repeat part 2 without avgmin. Comment on the differences.
Question 2
Use the data set meap93.RData to answer this question. Let math10 denote the percentage of students at a
Michigan high school receiving a passing score on a standardized math test. We are interested in estimating
the effect of per student spending (expend) on math performance. A simple model is
math10 = 0 + 1 log(expend) + 2 log(enroll) + 3lnchprg + u,
where the school size is measured by student enrollment (enroll), and lnchprg is the percentage of students
eligible for the federally funded school lunch program.
1. Estimate the model with and without the variable lnchprg (The model without lnchprg is referred to as
model 1 and the model with lnchprg is referred to as model 2). Explain why the effect of expenditures
on math10 is lower in model 2 than in model 1.
2. Does it appear that pass rates are lower at larger schools, other factors being equal? Explain.
3. Interpret the coefficient on lnchprg in model 2.
4. What do you make of the substantial increase in R2 from model 1 to model 2?

Problem Set 5
Statistics and Econometrics
Due: 12pm, 2 December 2019
General Guideline
What we are looking for in the assignments is a demonstration that you can understand the econometrics and
statistics questions and can use R to solve them. That means effective programming to get correct results is
needed, but at the same time, clear explanations of economics/business concepts in well presented reports
are equally important when assessing your work. In particular, you will be marked for successful (correct)
programming (not the style of coding), good understanding of related concepts, and clear interpretations and
explanations of results.
Only two forms of reports will be accepted, either pdf or html. We strongly suggest you to submit the pdf or
html converted from R markdown/notebook after you program in R. Please submit both the source code and
pdf/html file.
Question 1
Use the data in pntsprd.RData for this exercise.
1. The variable favwin is a binary variable indicating whether the team favored by the Las Vegas point
spread wins (If you are not familiar with spread betting, here is an explanation: https://en.wikipedia.
org/wiki/Spread_betting). A linear probability model to estimate the probability that the favored
team wins is
P(favwin = 1|spread) = 0 + 1spread.
Explain why, if the spread incorporates all relevant information, we expect 0 = .5.
2. Estimate the model from part 1 by OLS. Test H0 : 0 = .5 against a two-sided alternative. Use both
the usual and heteroskedasticity-robust standard errors.
3. Now, estimate a probit model for P(favwin = 1|spread). Interpret and test the null hypothesis that
the intercept is zero. [Hint: Remember that (0) = .5.]
4. Use the probit model to estimate the probability that the favored team wins when spread = 10.
Compare this with the LPM estimate from part 2.
5. Add the variables favhome, fav25, and und25 to the probit model and test joint significance of these
variables using the likelihood ratio test. (How many df are in the chi-square distribution?) Interpret
this result, focusing on the question of whether the spread incorporates all observable information prior
to a game.
Question 2
For this exercise, we use jtrain.RData to determine the effect of the job training grant on hours of job training
per employee. The basic model for the three years is
hrsempit = 0 + 1d88t + 2d89t + 1grantit
+2granti,t−1 + 3 log(employit) + ai + uit
1. Estimate the equation using fixed effects estimation (i.e., model = “within”). How many firms are used
in the estimation? How many total observations would be used if each firm had data on all variables
(in particular, hrsemp) for all three time periods?
2. Interpret the coefficient on grantit and comment on its significance.
3. Is it surprising that granti,t−1 is insignificant? Explain.
4. Do larger firms train their employees more or less, on average? How big are the differences in training?
