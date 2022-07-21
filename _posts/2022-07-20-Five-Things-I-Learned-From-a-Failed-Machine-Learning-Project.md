# Five Things I Learned from a Failed Machine Learning Project

Over the past year, I've been working with one of my former professors on a machine learning project that predicts if a publicly traded company will emerge from bankruptcy or not. We leveraged the [Florida-UCLA-Lopucki Bankruptcy Research Database](https://lopucki.law.ufl.edu/index.php) for our training data and set out to beat the benchmark set by the logistic regression model explained in this [paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2492209). Although the project ultimately failed, I learned a lot and decided to share those lessons here with the hope that'll prevent others from making the mistakes I did.

## Always Have Enough Subject Matter Expertise to Fully Understand the Data

When I embarked on this project, I knew very little about how bankruptcy cases work. This led me to become very confused by the meaning of many features in this 200-column dataset. I was often confused about which features would cause data leakage or not and which features would naturally be more important than others: issues that anyone with domain expertise in bankruptcy cases would be able to solve. Don't be like me and realize It is extremely difficult to leverage data to its potential when you lack domain expertise.

## Understand if it's Worth Beating the Benchmark or Not

Looking back, the model in Lopucki's paper was a fine solution to predicting bankruptcy, achieving a 0.87 ROC AUC score on our testing set. With a model as simple and accurate as this, attempting to beat it with fancy machine learning methods is a fool's errand. But I was blinded by my desire to become published straight out of undergrad and threw the kitchen sink at the problem trying to beat the benchmark. In reality, if a simple model fits the use case, don't chase accuracy with more complex methods down a rabbit hole.

## Start with a Minimal Viable Option Before Deep Diving into a Project

When I first started working on this project, I dove in headfirst spending hours trying to come up with new features to engineer, new hyperparameter search spaces, and anything else to beat the benchmark. Looking back, I should've just pushed the data through LightGBM, or any other auto ML solution, to see if Machine Learning was the right approach to the problem. Beginning with a minimal viable option will allow you to cut your losses early before investing too heavily.

## Make Data Cleaning Reproducible and Scalable 

After I understood the data to the best of my ability, I went right into data cleaning. Writing hundreds of lines of spaghetti code that I had to re-write all over again once I tried to apply it to the newly published dataset. To avoid this disaster, package your data cleaning procedures into functions and methods to ensure reproducibility and to avoid doing the same work twice.

## Be Passionate About the Subject

To be honest, bankruptcy cases are not a subject that I'm particularly interested in. Sure, I'm interested in finance and economics, and you could say that bankruptcy cases are related to that. But my desire to take on this project was mostly fueled by my ambition to become published straight out of undergrad. Once things got hard, my ambition began to wane, and the project became more of a chore than something I looked forward to. When embarking on a data science project, make sure you're passionate about the subject – don't do projects just to do projects.
