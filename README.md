## Zero-Knowledge Proof
___
Our approach to solve test problem is straightforward.

Used tools:
* Python
* numpy
* pandas
* scipy
___
### Identify a set of events and parameters with the highest or lowest correlation with the potential account cancellation.
We used Cramer's V method to calculate the correlation between different ```event_name```s and ```Subscription Premium Cancel``` event for each user who once cancelled subscription.

The results are:
* Events with highest correlation with Subscription Premium Cancel are (```'Add Payment Method Failed'```, ```'Order'```, ```'Wallet Opened'```)
* Events with lowest correlation with Subscription Premium Cancel are (```'Sign Up Success'```, ```'Transaction Refund'```, ```'Add Vehicle Failed'```)
___
### Prioritize the events, event properties or user properties, which have highest or lowest correlation with the account cancellation.
We used Cramer's V method again this time to calculate the correlation between ```event_platform``` and ```Subscription Premium Cancel``` event.

The platform with the highest correlation is ```android``` with the correlation of ```0.30398```.
The platform with the lowest correlation is ```ios``` with the correlation of ```0.24567```.