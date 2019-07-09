## Relax Inc. makes productivity and project management software that's popular with both individuals and teams. Founded by several former Facebook employees, it's considered a great company to work at.


## Challenge:
#### Defining an "adopted user" as a user who has logged into the product on three separate days in at least one seven-day period, identify which factors predict future user adoption.

## Output:
#### Please draft a brief writeup of your findings (the more concise, the better - no more than one page), along with any summary tables, graphs, code, or queries that can help us understand your approach. Please note any factors you considered or investigation you did, even if they did not pan out. Feel free to identify any further research or data you think would be valuable.

## Data Provided:
#### A. takehome_users.csv
**name**: the user's name
**object_id**: the user's id
**email**: email address
**creation_source**: how their account was created. This takes on one of 5 values:
    - PERSONAL_PROJECTS: invited to join another user's personal workspace
    - GUEST_INVITE: invited to an organization as a guest (limited permissions)
    - ORG_INVITE: invited to an organization (as a full member)
    - SIGNUP: signed up via the website
    - SIGNUP_GOOGLE_AUTH: signed up using Google Authentication (using a Google email account for their login id)
**creation_time**: when they created their account
**last_session_creation_time**: unix timestamp of last login
**opted_in_to_mailing_list**: whether they have opted into receiving marketing emails
**enabled_for_marketing_drip**: whether they are on the regular marketing email drip
**org_id**: the organization (group of users) they belong to
**invited_by_user_id**: which user invited them to join (if applicable).

#### B. takehome_user_engagement.csv
**daily_user_login**: row for each day that a user logged into the product.

## Produced Files:
**predicting_user_adoption.ipynb**: Creates dataframe that defines a user as "adopted" or "not"
**user_adoption_explored.ipynb**: Identifies which factors predict future user adoption using Random Forest Classification

## Conclusion:
In order to predict user_adoption with Mean Absolute Error of 0.03, use user's last_session_creation_time (with 59% importance) and user's creation_time (with 34% importance).