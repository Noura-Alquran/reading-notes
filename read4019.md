# Read: Class 09 Summary:
## Enriching Your Python Classes With Dunder (Magic, Special) Methods:
* **Dunder methods**  or **the special methods** or **magic methods** are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example __init__ or __str__.
* They are used to create functionality that can't be represented as a normal method.
* **Object Initialization**: __init__: To construct objects from class.
* **Object Representation**: __str__, __repr__ :
  1. __repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.
  2. __str__: The “informal” or nicely printable string representation of an object. This is for the enduser.
* **Iteration**: __len__, __getitem__, __reversed__
  - __len__ for len()
  - __getitem__ for indexing
* **Operator Overloading for Comparing**: __eq__, __lt__
  - __lt__ for <
  - __le__ for <=
  - __eq__ for ==
  - __ne__ for !=
  - __gt__ for >
  - __ge__ for >=
* **Operator Overloading for Merging**:
  - This means defining operators for custom classes that allow operators such as + and * to be used on them.
  - Example: __add__ for +
* **Callable Python Objects**: 
  - to make an object callable like a regular function you can add the __call__ dunder method. 

## Basic Statistics in Python — Probability:
* Probability is a measure of the likelihood of an event to occur.
* The probability formula is defined as the possibility of an event to happen is equal to the ratio of the number of favourable outcomes and the total number of outcomes.
  *  **Probability of event to happen P(E) = Number of favourable outcomes/Total Number of outcomes**
* Statistics is the study of the collection, analysis, interpretation, presentation, and organization of data. 
* given enough data, statistics enables us to calculate probabilities using real-world observations. Probability provides the theory, while statistics provides the tools to test that theory using data.
* the normal distribution is a probability distribution that is symmetric about the mean, showing that data near the mean are more frequent in occurrence than data far from the mean. In graph form, normal distribution will appear as a bell curve.
* The normal distribution is significant to probability and statistics thanks to two factors: **the Central Limit Theorem** and **the Three Sigma Rule**.
* The Central Limit Theorem states that the sampling distribution of the sample means approaches a normal distribution as the sample size gets larger — no matter what the shape of the population distribution.
*  The Three Sigma rule dictates that given a normal distribution, 68% of your observations will fall between one standard deviation of the mean. 95% will fall within two, and 99.7% will fall within three. the Three Sigma Rule enables us to know how much data is contained under different intervals of a normal distribution.
* The Z-score is a simple calculation that answers the question, “Given a data point, how many standard deviations is it away from the mean?”
* The z-score is positive if the value lies above the mean, and negative if it lies below the mean.
* The formula for calculating a z-score is is **z = (x-μ)/σ**, where x is the raw score, μ is the population mean, and σ is the population standard deviation.
