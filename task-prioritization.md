# Task Prioritization

## Actors

There are several actors:

* Direct Customer - A client directly using the product.
  * Hospital admins
  * Practice manager
  * Technical admin
  * Doctors
* Nurses
* Indirect Customer
  * Patients (indirect)
* Sales - The team who interact with clients. They may request tasks based on conversations with potential clients indirectly. Tasks from
sales is different than coming from the client directly. We don't want to automatically implement all client requests.
* Quality Assurance - The team that provides quality control for the product. This team is responsible for ensuring that the engineered
product reflects the required specifications.
* Support - The team that provides support for the client. This team is different than the quality assurance.
* Business - Higher up business executives or management. Want to influence or shift the product's direction.
* Marketing - Marketing may have conducted research and think they will be able to provide the direction that will benefit the product and
its future. This is likely a new feature, or changing the audience or perspective of existing features.
* Development Engineer - Responsible for implementing features and fixing issues.
* Finance - Financial concerns may influence tasks. Something may be too expensive or inefficient in its current state.
* Security Engineer - Responsible for securing the application and platform
* Operations Engineer - Responsible for maintaining, monitoring systems, responding to incident and infrastructure troubleshooting

## Tasks

There are several types of tasks:

* A problem with existing functionality - A calculator function incorrectly adds two numbers.
* A feature request or improvement upon an existing function - A restaurant bill calculator. A feature is requested to evenly split the bill
among the people.
* A completely new function - Convert the bill into different currencies
* A configuration branching - Keep existing functionality but provide a mechanism to change the configuration - Allow for different
currencies as the default
* A security or compliance related vulnerability on existing functionality - A person can change the amount after its been calculated.
* A performance issue on existing functionality - It takes a very long time to calculate
* Maintenance on existing functionality - Changing the way the numbers are added to allow for a variable ratio on the split bill.

The "actor" and "task" together define a contextual task. A feature that a development engineer or an operations engineer may have may be
useful to them but may not be the best for the longevity of the product. The product owner is responsible for evaluating all of the needs at the time
and deciding what needs are the greatest. A well defined SDLC would provide a well structured mechanism to aid the product owner to sort the
importance of tasks.

The type of task in combination with the actor determines the overall weight that the task should carry when being prioritized.

### Calculating priority

Let's go through a simple example with a subset of actors and tasks to illustrate how to actually prioritize tasks with this approach.

Let's have four actors:
* Client
* Sales
* Business
* Development

Let's have four tasks:
* Bug
* Security or compliance
* Feature
* Maintenance or build related

Now let's prioritize our actors. Here we will order our actors and tasks numerically where the lower numeral indicates a higher priority and a higher
numeral indicates a lower priority.


We want to utilize the short-term impact and long-term impact of the given task. We also want to consider the chance that the task will occur or
not. We need to be able to allow an organization to weight the importance of short-term and long-term impact.

1. **AI** - Actor importance (0 not very important, 10 very important)
2. **STPI** - Short term positive impact (-10 very negative impact, 0 no impact, 10 a very significant positive impact)
3. **LTPI** - Long term positive effect (-10 very negative impact, 0 no positive impact, 10 a very significant positive impact)
4. **CHANCE** - Likelihood of occurrence (0 not going to happen at all, 5 could be either way, 10 is certain)

There are two weights that you must set. How much importance you place on the short term (STW) and how much you place on the long term
(LTW).

The formula is simple:

```
P = (STPI * STW) + (LTPI * LTW) + AI
```

Take the long and short term impacts with their weights. Then we want to account for the likelihood of them occurring.

### Collisions

This general process should help to mitigate most of the possible priority related matters. There will be always be times when a decision is
required as two or more events of importance coincide. This approach should aid as a rubric and to help with objectivity.
