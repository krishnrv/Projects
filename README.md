# Spanish translation on website: A/B testing
Academic Projects
# Problem 

A worldwide e-commerce site has localized versions of the site in Spanish. Managers noticed that Spain-based users have a much higher conversion rate than any other Spanish-speaking country. After talking to the international team in charge of Spain And Latin America(LatAm) about it, the Spain and LatAm country manager suggested that one reason could be translation. All Spanish- speaking countries originally had the same translation of the site which was written by a translator from Spain. 


# Proposed Solution

They agreed to try a test where each country would have its one translation written by a local (Argentinian users would see a translation written by an Argentinian, Mexican users by a Mexican, and so on), replicating what happened with Spanish users. As for users from Spain, they would have no change since their translation is already localized to Spanish.

## A. Hypothesis

Including a localized Spanish translation for each country's dialect will increase conversions for Spanish-speaking countries other than Spain.

## B. Metric

We will be using conversion as the metric to test our hypothesis. Conversion is defined as the number of customers who sign up for the company's website, given they have been exposed to the translation.

##  C. Experiment

Our goal from this experiment is to understand the effect of having local translation from each country on user conversion, which is done by randomly dividing visitors into equal groups for each country, and having one group (control group) exposed to the original Spanish translation, and the other (treatment group) exposed to a more localized Spanish translation. We want to measure conversion for each group after having been exposed to respective translations, and see whether having a localized translation results in a significant difference between conversions coming from users viewing the control version versus the treatment version.

It is estimated that about 80,000 shoppers from Spanish-speaking countries visit the website daily, and the company would want enough time to negotiate contracts before the holiday season if the result turns out favorable towards local translations. Therefore, the experiment will run for 5 days to allow for a sizeable sample, which is from the 30th of November to December 4th, giving enough time for the company to act on findings before the holidays.

First, the conversion ratio will be explored for both groups in order to have an idea of the effects of localizing translations. Then, a two-tailed statistical t-test will determine whether statistically significant difference exists, and whether it is worth introducing to the website. The two-tailed test will be used because we do not know which translation is likely to perform better, and therefore can use testing in two directions.

user_id : the id of the user. Unique by user. Can be joined to user id in the other table.
For each user, we just check whether conversion happens the first time they land on the
site since the test started.

date : when they came to the site for the first time since the test started

source : marketing channel: Ads, SEO, Direct . Direct means everything except for ads
and SEO. Such as directly typing site URL on the browser, downloading the app w/o
coming from SEO or Ads, referral friend, etc.

device : device used by the user. It can be mobile or web

browser_language : in browser or app settings, the language chosen by the user. It can
be EN, ES, Other (Other means any language except for English and Spanish)

ads_channel : if marketing channel is ads, this is the site where the ad was displayed. It
can be: Google, Facebook, Bing, Yahoo ,Other. If the user didn't come via an ad, this
field is NA

browser : user browser. It can be: IE, Chrome, Android_App, FireFox, Iphone_App,
Safari, Opera

conversion : whether the user converted (1) or not (0). This is our label. A test is
considered successful if it increases the proportion of users who convert.

test : users are randomly split into test (1) and control (0). Test users see the new
translation and control the old one. For Spain-based users, this is obviously always 0
since there is no change there.

user_id : the id of the user. It can be joined to user id in the other table
sex : user sex: Male or Female
age : user age (self-reported)
country : user country based on ip address
