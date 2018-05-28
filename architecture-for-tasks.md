# Architecture for tasks
The design for a task must be appropriate for the solution as well as the numerous other constraints that may be present. When in the position to
architect a feature the time and level of effort involved will usually be the most significant factor. As discussed regarding clarifying a task's
requirements, an engineer should never approach a task blindly at face value. By the time a task is being designed the hope is that all of the
clarifications have been made and the requirement is in fact clear. Even within a clearly defined task there may be several implementation paths
as well as slight variations.

Let's go through a simple use case and its potential architecture now.
> As as an administrator I would like to be able to filter the list of patients by the last name
From experience for some reason people have a tendency to often interchange sort and filter. You can sort alphabetically by patients last name in
either ascending or descending order. That is different than filtering the results to only include matching criteria. This sort of ambiguity should be
clarified when vetting the requirements prior to the design phase. After vetting the requirements the use case was re-written as follows:

> As an administrator I would like to be able to sort the list of patients by their last name alphabetically

Is there still ambiguity? Slightly. We could make it slightly clearer.

> As an administrator I would like to be able to sort the list of patients by their last name alphabetically while specifying the
> direction ascending (A-Z) or descending (Z-A).

There is truly only implementation details left. There are a few ways visually this is typically accomplished as well as with the data manipulation.
The simplest approach is that the data retrieved is always the same and the sorting only occurs on the client side. This requires only a change to
the front-end which is a pro, however it lacks to deal with things like pagination. If the data was being paginated sorting on a single page would
"work" but is very likely not the desired functionality. Let's say the table is not paginated. The most common way of sorting in a table is allowing
the user to click on the header of the corresponding column. Next to the text of the header an up or down arrow would often be present to indicate
the current direction. None of these conventions are written in stone (that I know of). If the use case is to only implement sort on the single column
a potential usability issue could arise. If there are several other columns present the user can likely get confused why they cannot sort those
columns. Due to this it may be advisable to specify the sort in a control field above the table. This isn't a big deal, but it is anticipating possible
issues or complications when choosing an implementation. It is also possible to further clarify if there are only a few other columns whether they
should be sort-able as well.

This small silly example is trivial in the bigger picture of software engineering by far. It does however illustrate the possible range of options and
possible complexities.

With the sorting tabular data example used above the initial development may have not anticipated the extent of how many total records there
would actually be. Load time on the user as well as undue stress on the web server and database is the outcome of that oversight. It indeed may
have not been an oversight, business needs constantly change. An engineer cannot truly account for every possible outcome. They can however
design and engineer defensively. Anticipating potential changes even when the customer repeatably insists that it isn't necessary is part of the
job. The true test is looking at the real domain of the entity. If you are display a list of a person's favorite member of the band The Beatles, it is a
matter of fact that this list may never exceed four (or at least the four most well known). If you are dealing with a list of baseball cards you own
there is of course a physical limit. Depending on who you are that number could vary significantly. A collector could have thousands of baseball
cards. If were listing all of the current active baseball players that would be different. While we may not know right now the exact number of
players, we know that it is finite. We also know that there cannot be millions or thousands. Can a doctor have millions or thousands of patients?
Active patients, unlikely thousands. Including inactive patients over a span of fifty years, that's possible. A hospital may certainly have many
thousands of patients. If you are true to the domain you will never regret it.

## Design is more than implementation

The design for tasks should be compose of more than just the possible implementations. Testability is not a made up word. Initial simple unit
testing is a given. Unit testing should not be mentioned as an aspect of the development. The implementation of that task should not even be
considered without quality unit tests. A unit test is the litmus test that will ensure when other pieces of code may change that your isolated tests
will be able to pinpoint functionality.

The design must also take security implications as part of the design, not just a mere afterthought. Threat modeling and pen testing and the like
are great and should be performed, but the engineering team should act is if they are the only ones responsible for the security of the application!!

## Choosing a design
These items are all important and are not ordered in priority. They must be alll considered when choosing different design approaches, and
technologies.
* Ease of implementation
* Execution efficiency
* Code clarity
* Code modularity
* Testability
* Security implications
