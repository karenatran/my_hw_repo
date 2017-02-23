### ***Project 2 Feedback***

***Nico Van de Bovenkamp***
***

**Overall** Very thorough exploratory analysis and exploratory analysis plan you have laid out! You continue to make very good use of appending methods for efficient coding and reproducibility of results! And great work on filling those missing values.

**Some notes**

* **Q.1** Good use of method appending, however the way we usually define 'observation' or 'instance' is the number of rows or the number of whole 'things' that we have observed. Think, in this case, an observation is each student that applied to school and each student is defined by: GRE, GPA, Prestige of undergraduate institution, and admittance.
* **Q.9** You are definitely right that each distribution does exhibit some slight skew, and what is required of a normal distribution, however all of them are approximately normally distributed. Think about how you could potentially correct for this skew, or what tests you could apply to confirm or reject the assumption that a distribution is approximately normally distributed.
* **Q.13** This plan is very precise! The one comment I would make is that we don't really 'build a model by using graphs' as much as we explore the underlying data visually in order to subsequently build our model. For example, in lesson 6 we made some graphs of the data to explore relationships and distributions of the data, and then we started to build out a preliminary model (making the bikesharemodel data frame, and taking the further step of dummify-ing all of the categorical variables). Let me know if this is clear.

**Bonus** Nice work on this bonus! Some thoughts really quick:
* Although your code for doing the log transform was correct (nice job with that!), we wouldn't want to perform a transform on a discrete variable (like prestige) because transforms usually require 'continuous' variables. Try doing the transform on GRE and GPA!
* Good job on filling those missing values! I encourage you to look into some other ways you could do this too so you have multiple methods when it comes to a new dataset!
