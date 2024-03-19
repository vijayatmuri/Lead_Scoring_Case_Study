# Lead_Scoring_Case_Study
Lead Scoring Case Study
# Problem Statement
An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their website and browse for courses. 

The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Moreover, the company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%. 
 
Now, although X Education gets a lot of leads, its lead conversion rate is very poor. For example, if, say, they acquire 100 leads in a day, only about 30 of them are converted. To make this process more efficient, the company wishes to identify the most potential leads, also known as ‘Hot Leads’. If they successfully identify this set of leads, the lead conversion rate should go up as the sales team will now be focusing more on communicating with the potential leads rather than making calls to everyone

# Problem Mapping and Solution Approach
The company requires you to build a model wherein you need to assign a lead score to each of the leads such that the customers with a higher lead score have a higher conversion chance and the customers with a lower lead score have a lower conversion chance. The CEO has given a ballpark of the target lead conversion rate to be around 80%.

The problem can be mapped to find the hot leads i.e. the leads that are most likely to convert into paying customer.
This is a classification problem, where in we need to build a model to assign lead score to each of the leads such that the customer with higher lead score has higher conversion chance and customer with lower lead score has lower conversion chance
The company wants to utilize their resources optimally such that the lead conversion rate to be around 80% (we need to have suitable cutoff of the lead score and identify the potential leads such that lead conversion rate (recall_score) would be greater than 80%)
