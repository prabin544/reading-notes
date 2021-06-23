## How to use Random Module?
The Random module contains some very useful functions.

#### Randint
If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.
```
import random
print random.randint(0, 5)
This will output either 1, 2, 3, 4 or 5.
```
#### Random
If you want a larger number, you can multiply it.

For example, a random number between 0 and 100:
```
import random
random.random() * 100
```
#### Choice
Generate a random value from the sequence sequence.

random.choice( ['red', 'black', 'green'] ).
The choice function can often be used for choosing a random element from a list.
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

#### Shuffle
The shuffle function, shuffles the elements in list in place, so they are in a random order.

```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
Output:
# print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
# of course your results will vary
```

#### Randrange
Generate a randomly selected element from range(start, stop, step)
```
random.randrange(start, stop[, step])
import random
for i in range(3):
    print random.randrange(0, 101, 5)
```
[source](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)

## What is Risk Analysis
Risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.  

#### what could be the possible risks that you could encounter? 

- Use of new hardware
- Use of new technology
- Use of new automation tool
- The sequence of code
- Availability of test resources for the application

Now, you must know there are certain risks that are unavoidable. I am enumerating them below:

- The time that you allocated for testing
- A defect leakage due to the complexity or size of the application
- Urgency from the clients to deliver the project
- Incomplete requirements

In such cases, you have to tackle the situation with care. Following points can be taken care of:

- Conduct Risk Assessment review meeting
- Use maximum resources to work on high-risk areas
- Create a Risk Assessment database for future use
- Identify and notice the risk magnitude indicators: high, medium, low.

Now, what are these risk magnitude indicators? 

- High: means the effect of the risk would be very high and non-tolerable. The company might face loss.
- Medium: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.
- Low: it is tolerable. There lies little or no external exposure or no financial loss.

Moving on! Our next topic queued is as follows:

##### Risk Identification
There are different sets of risks included in the risk identification process. Those are as follows:

- Business Risks: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.
- Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.
- Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required
- Software Risks: You should be well versed with the risks associated with the software development process.

After identifying the risks associated with your software, the next step is to assess the risks; i.e, Risk Assessment.

##### Risk Assessment
In the risk analysis process, these steps prove to be the most important one. It is said that this step is way too complex and should be tackled with the utmost care. After risk identification, assessment has to be dealt programmatically. There are a few perspectives on risk assessment.
[source](https://www.edureka.co/blog/risk-analysis-in-software-testing/)
