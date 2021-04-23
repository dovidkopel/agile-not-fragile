# Agile Resources

It should be "agile" not "fragile". Some agile perspectives believe that to be truly "agile" every member of the team must know every component etc. Not only is this ridiculous but it tries to make every member of the team a jack of all trades. This may work in some scenarios and over time the team may be able to reach an equilibrium and a healthy state. You don't achieve healthiness but just hiring more people or throwing money on it.

* **T**echnologies - The different technologies used in a project
* **C**ode - A project may be composed of several modules or components. Even a single module could be very large and a single engineer may not be proficient in all of it
* Domain **K**nowledge -  Knowledge of the workings of the industry, the business, the actors

`T + C + K = A/N` (Asset coverage over number of team members)

The TCK (Tack) has a formula that can easily identify a healthy or unhealthy team. There are a few different metrics that we may glean from this information.

Track the size, complexity, impact of each aspect the system.
Let's start off with counting one point for each aspect of each section.
We have two sides of that equation, the right side represents the human asset coverage.
To what extent is each aspect of the system covered by a team member (employee).

This formula doesn't account for the importance and/or weight of each category and each individual component.
The other side of the formula that requires additional detail is the degree to which each team member's fluency in each individual componenet.

Let's break down each category into how we may interface with greater details.

For each of the three `TCK` individual items, a team member should provide these three data points:
* Duration - Years of experience
* Comfortablity - How comfortable you are (1 least, 10 most)
* Fluency - How fluent you are (1 none, 10 guru)

Now for each category there are these details

## Technology
* Usage - How much unique usage is each technology utilized
* Changes- How often are changes made to how the technology is used
* Impact - How great of an impact does this technology affect the system
* Uniqueness - How much is the product specific functionality used that a comparable alternative may not have

## Knowledge
* Breadth
* Complexity
* Dependencies
* Cross Dependencies

## Code
* Lines of code
* Comments
* Complexity
* Test Coverage
* Dependencies
* Cross Dependencies
* Criticality

# Deep Dive
Let's create a sample project:

1. A financial system that has a back-end component, the company dashboard, a trader app for Android and iOs.
2. We can say that is 4 unique components of source code. 
The number of technologies involved are: Java, PostgreSQL, AMQP, Android, iOS, JavaScript; totaling 6 technologies.
The extent of the domain knowledge could be very vast, let's just say there are 10 distinct separate knowledge domains.
So we can summarize C=4, T=6, K=10 with a grand total of A=20.
Now let's create a fictional team:
* Tom
* Jim
* Bob
* Ron

Let's say that each member of this team knows exactly 5 aspects of the 20 total aspects each with a 100% proficiency. That would mean that if one of the team members was unavailable they would be lacking a fourth of their total A value.

This is of course the single point of failure concept. TACK attempts to provide insight into into deficiencies with members of the team or with aspects of the project. This information may be used when planning a sprint, considering hiring additional resources, continuing education, etc.

### Perfect ratio

In a perfect world our fictional team would have a value of A=80 where each member of the team possesses the full 20 possible points. Not only is this unrealistic but very often diminishing returns. If that happens naturally that is one thing, however attempting to achieve this is an unreasonable goal and will likely end with unhappy overworked employees and in the end unhappy customers.

### Your ratio
Each team may choose what their own values of "healthy" and "unhealthy". A reasonable healthy value is for every point of a project there is 250% coverage on a team. This ensures that a single person is not solely owning, and even a second person still has a partial backup. A possible unhealthy value may be anything below 150%.

Let's take for example the back-end component. With our fictional team it is possible to have: Tom=50, Jim=20, Bob=100, Ron=30, this yields a total of 200%. While this is in fact more than the 150% threshold we had set earlier there is some additional details that can enhance our understanding. If we calculate the standard deviation of the set  {20, 30, 50, 100} you get 35.59 and a coefficient of variation of 0.7118. The fairly high standard deviation tells us that the 200% isn't well distributed. This will mean that while we may have high coverage, there still may be a single point of failure. In fact, let's adjust our numbers slightly to this: {50, 40, 50, 60}. That still yields a total of 200%, but it's standard deviation is 8.165 and coefficient of variation at 0.1633. It is better to have a more evenly distributed total with a variation as close to 0 as possible.

#### Not one size fits all
The figured used thus far have been for illustration purposes only and not something that will be the same in every organization. Just like an organization must specify how many "9's" in uptime they want, so too here. Depending on the architecture of the organization and the products it is offering there will be different healthy and unhealthy values.
#### Set triggers
An organization should not make these values static like one time set and forget about it. These metrics should evolve and hopefully improve alongside your organization. You should strive for greater coverage in your teams with greater proficiency. Set event based triggers that will ensure you re-evaluate your current position and approach. Such triggers can be number of employees, number of clients, or target revenue.
