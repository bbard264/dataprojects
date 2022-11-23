# A/B Testing
A/B Testing refers to a randomized experimentation process wherein two or more versions of a variable are shown to different segments of website visitors at the same time to determine which version leaves the maximum impact and drive business metrics.

## Let Explore!
Now the objective of out A/B Testing is finding out which one colour of pens that people prefer it more than others. we easily just spread questionnaire to people around us. here are those pens look like!\
![2pens](https://user-images.githubusercontent.com/95345008/147789681-7c95b941-7b4b-4c06-888c-94aaf31ac45f.jpg)\
The orange pen and the turqoise pen
## Collect & Prepare Data
After Pen Questionnaire is spread out to 50 peoples, we got these!
1. Gender : 32 Males, 18 Females
2. Age : 21-42
3. Purpose : 32 peoples purpose for Study and 18 for Work
4. Satisfaction Score of orange pen : 1 - 5 (5 = Very satisfied)
5. Satisfaction Score of turqoise pen : 1 - 5 (5 = Very satisfied)\
\
then, we prepare data to here.\
\
![image](https://user-images.githubusercontent.com/95345008/147789740-f7415309-2d15-42c4-a34b-06684df9eb51.png)
## Paired T-Test
we use paired T-Test to find difference of satisfaction score between 2 colous of pen. here the result.\
![image](https://user-images.githubusercontent.com/95345008/147789765-26784441-8e4f-430a-902c-40ef9091c27c.png)\
From T-Test, there are different between 2 colours of pens and turquoise score is more than oragne score at significant 0.01\
We also add some effect that we think it effects to the result
### Gender Effect
![image](https://user-images.githubusercontent.com/95345008/147789794-098a7694-9233-4837-bfa0-0876e8a38ecc.png)
\
And we found that 'Gender' is no effect.
### Purpose of Purchasing Effect
![image](https://user-images.githubusercontent.com/95345008/147789803-600916ef-6755-4ecc-9599-4cb5108f5f62.png)
\
And we found that 'Purpose of Purchasing' is no effect.
## Conclusion
From T-Test, we found that people like turquoise pen more than orange and purpose of purchasing and gender is no effect.
