# Five Things I Learned After One Year as a Data Analyst

Today marks one year of working as a Data Analyst, as well as my one-year anniversary of working full-time post undergrad. Now that I’ve crossed this milestone, I thought it would be a good idea to reflect on the things I’ve learned along this interesting journey.

## Quality Data is the Foundation for Successful Analytics 

The old adage of “garbage in, garbage out” is a profound cornerstone of the data landscape that holds true from basic tasks such as descriptive analytics to more complex ones such as Machine Learning. Without quality data, your metrics become meaningless, and your team can enter a downward spiral of distrust across all stakeholders you serve. Quality data does not just mean that it is accurate, but that it is also easy to digest and consume. This starts at the schema design of your Data Warehouse and rolls all the way up to how you present the data to your stakeholders. To ensure that your data is of high quality, all members of the data ecosystem should own QA; from the Data Engineers who ingest the data and design the warehouse, to the analysts who present the data.

## Do not Discount the Power and Flexibility of SQL

When I first started, I was obsessed with Python and often tried to use it for basic analysis. This bottlenecked things and slowed down my workflow since I would have to import the data from our data warehouse and then spend a ton of time searching through Seaborn documentation to try to get my visualizations to look just right. After coming to terms with SQL and adopting it as my tool of choice for practically any task that is within its limits, my workflow is far more efficient. I’ve also found that the syntax is far more interpretable and intuitive than the seemingly endless method chaining you would have to do to accomplish the same task in a Python data library such as Pandas or NumPy.

## Descriptive Analytics Tends to Have a Higher ROI Than More Complex Methods Such as Machine Learning 

This is because practically everyone needs descriptive analytics to make accurate decisions, but not everyone needs to predict or automate something. Additionally, descriptive analytics has a much shorter development time than Machine Learning. This allows the team to pump out metrics and reports to enable decision makers across the organization, instead of getting bogged down trying to predict or automate something used by only a small fraction of the entire organization.

## Documentation is a Front-Loaded Necessity 

I remember writing my first piece of technical documentation. It was not memorable based on its content, but instead on how much I hated doing it. We even had a team meeting centered around documentation that I had to sit through each week. But as we built a library full of documentation to be used both internally and externally, I began to understand its value. Emails I would spend 15 minutes writing would begin to disappear as the knowledge contained within the documentation began to spread across the organization. Quarterly reports that used to leave me asking “Wait, how do I do this again?” became a simple step-by-step process of working through the documentation. Sure, documentation may take a long-time up front, sometimes even longer than the task itself, but the time it saves down the road makes it a worthy investment for the long haul.

## Clean Code Will Save You from a Work-Life Full of Misery 

My mentality going into building my first datasets was typically to just get the data to be accurate and usable. But then I would look back on these queries months later and have no clue what I was trying to accomplish. It became even more of a nightmare when I would pass the reporting on to others and they would have to read through what I wrote, making any updates quite the arduous process. Now my queries are much more readable, mostly based on a series of questions I ask myself during development such as:

-   “What are the requirements and what data sources do I need?”

-   “Is there a way I can reduce my data sources?”

-   “Will anyone with knowledge of SQL be able to easily read this?”

There are also some standard practices I try to follow for all my queries including:

-   Having a formal code review of my own work as well as others

-   Using CTE’s over subqueries whenever possible

-   Choosing readability over reduced verbosity (especially with aliases)

    -   Ex. Calling a table “arr_table as arr” instead of “arr_table as a”

-   Having a standardized way of handling whitespace

    -   Ex. Tabbing all fields within each select, where, and order by clause, etc.
