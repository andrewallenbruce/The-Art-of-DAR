# The DAR Formula
## The Numbers Needed to Calculate Days in AR

You need only ***three*** numbers to calculate the average **Days in AR**. They are the *Number of Days in the Period*, the *total Gross Charges* for that period, and the *Ending AR Balance*. You will also need the *Average Daily Charge*, but you can derive this number from two of the three essential numbers:

### Number of Days in the Period

This is literally the number of days within the period for which you are measuring *Days in AR*. DAR is typically measured in monthly and quarterly increments, so this number will usually hover around 30, 60, 90, etc.

### Total Gross Charges

Gross charges, which are usually the *full* fee schedule[^3] charges, are typically all charges generated by the practice, regardless of actual reimbursement. This figure is the total dollar amount charged during the *Number of Days in the Period* you are measuring. Whether billed to insurance on a claim or to a self-pay patient, all charges for the period are included here.

[^3]: A list of fees physicians establish as the fair price for the services they provide. Keep in mind that it is not the same as a payment schedule.

### Average Daily Charge

This number is the *total Gross Charges* amount divided by the *Number of Days in the Period*.

### Ending AR Balance

This is the AR balance at the close of business on the final day of the *Period* that you are measuring.

## Step-by-Step Example of the DAR Formula

<br>

Let's go through an example of the DAR calculation step-by-step. The following table contains the **three** data points you need to calculate Days in AR: <br>

$$\\[3pt]$$

| **Number of Days in Period** | **Gross Charges** | **Ending AR Balance** |
|:----------------------------:|:-----------------:|:---------------------:|
|              30              |   \$131,440.30    |     \$203,460.50      |

: The three data points needed to calculate DAR.

$$\\[3pt]$$

### Calculate the Average Daily Charge

First, we need to calculate the **Average Daily Charge**. The formula is as follows:

$$\\[3pt]$$

$$
\dfrac {\textrm{Gross Charges}}{\textrm{Number of Days in Period}} = {\textrm{Average Daily Charge}}
$$

$$\\[3pt]$$

So, if we take the **Gross Charges** from the table above and divide it by the **Number of Days in the Period**, our **Average Daily Charge** will be **\$4,381.34**:

<br>

<br>


```r

## GCt divided by NDiP equals ADC

131440.30/30
```

[1] 4381.343

<br>

$$
\dfrac{131,440.28}{30}= 4,381.34
$$

<br>

### Calculate the Days in AR

Now that we have the three variables required by the DAR formula, we can calculate the **Days in AR**. Remember, our formula is:

$$\\[3pt]$$

$$
\dfrac {\textrm{Ending AR Balance}}{\textrm{Average Daily Charge}}= {\textrm{Days in AR}}
$$

$$\\[3pt]$$

We'll substitute the **Ending AR Balance** and **Average Daily Charge** into the above formula and divide. This will give us an average **Days in AR** of **46.44** days:


```r

# EARB divided by ADC equals DAR

203460.50/4381.34
#> [1] 46.43796
```

$$
\dfrac{203,460.50}{4,381.34}= 46.44
$$

$$\\[3pt]$$

Now our report table looks like this:

| **Days in Period** | **Gross Charges** | **Ending AR** | **Avg Daily Charge** | **Days in AR** |
|:------------------:|:-----------------:|:-------------:|:--------------------:|:--------------:|
|         30         |   \$131,440.30    | \$203,460.50  |      \$4,381.34      |     46.44      |

$$\\[3pt]$$