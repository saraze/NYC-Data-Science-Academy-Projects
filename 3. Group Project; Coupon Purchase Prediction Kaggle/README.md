#The original description of the project can be found [here](https://www.kaggle.com/c/coupon-purchase-prediction).

"Recruit Ponpare is Japan's leading joint coupon site, offering huge discounts on everything from hot yoga, to gourmet sushi, to a summer concert bonanza. Ponpare's coupons open doors for customers they've only dreamed of stepping through. They can learn difficult to acquire skills, go on unheard of adventures, and dine like (and with) the stars.

Investing in a new experience is not cheap. We fear wasting our time and money on a product or service that we may not enjoy or fully understand. Ponpare takes the high price out of this equation, making it easier for you to take the leap towards your first sky-dive or diamond engagement ring.

Using past purchase and browsing behavior, this competition asks you to predict which coupons a customer will buy in a given period of time. The resulting models will be used to improve Ponpare's recommendation system, so they can make sure their customers don't miss out on their next favorite thing."

##Overview of R scripts contained herein:

### 1. pre-processing

+ *split-data.R* --- splits the original training data into
training-validation sets

+ *make-features.R* --- pre-processes the features of the users 
and the test coupons

### 2. tuning parameters (feature weights)

+ *run-tests.R* --- implements our recommendation model on
a validation set using various weight combinations for
the coupon features; records resulting scores (MAPs)

+ *cos-sim.R* --- a function that accepts a weight combination
for the coupon features and returns coupon recommendations for
all users

+ *map.R* --- a function that computes the mean average precision
(MAP) of the recommendations for all users in a validation set

+ *summ-tests.R* --- combines the test scores (MAPs) from all
validation sets

### 3. producing a submission

+ *make-submission.R* --- produces coupon recommendations for
all users in the test set
