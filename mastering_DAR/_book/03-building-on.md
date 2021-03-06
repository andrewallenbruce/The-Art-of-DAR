# Building on the DAR Formula

Now that we have gone through the basic formula and have some sample results, we can expand upon and rearrange this formula to do many other things. If we include the calculation for the **Average Daily Charge** in our DAR formula, it looks like this:

$$\\[3pt]$$

$$
\dfrac {\textrm{Ending AR Balance}}{\textrm{Gross Charges} \div \textrm{Number of Days in Period}}={\textrm{Days in AR}}
$$

$$\\[3pt]$$

To simplify things a bit, I'm going to begin using mathematical variables and acronyms for these numbers. They are as follows:

$$\\[3pt]$$

| **Variable** | **Acronym** | **Description**                 |
|:------------:|:-----------:|:--------------------------------|
|     $n$      |   `NDiP`    | Number of Days in the Period    |
|     $x$      |    `GCt`    | Total Gross Charges for `NDiP`  |
|     $y$      |   `EARB`    | Ending AR Balance               |
|     $c$      |    `ADC`    | Average Daily Charge for `NDiP` |
|     $z$      |    `DAR`    | Days in AR                      |

: DAR Formula Components.

$$\\[3pt]$$

## Ending AR Balance Required for $x$ DAR

What if we wanted to know the exact **Ending AR Balance** we'd need to attain a certain number of **Days in AR**? Let's take our table of results from the previous example and set up the calculation for this. Our results were:

$$\\[1pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | **DAR** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-------------:|
|       30       | \$131,440.30  |  \$203,460.50  |  \$4,381.34   |     46.44     |

$$\\[3pt]$$

Next, we have our DAR formula, which we'll convert to variables to make it easier to visualize what's going on mathematically:

$$
\begin{aligned}
{\textrm{If:}} \ \ \
\dfrac {\textrm{EARB}}{\textrm{GCt} \div \textrm{NDiP}}&={\textrm{DAR}} \\
\\
\\
{\textrm{Where:}}\ \ \
{\textrm{EARB}}&=y\\ \ \
{\textrm{GCt}}&=x\\ \ \
{\textrm{NDiP}}&=n\\ \ \
{\textrm{DAR}}&=z\\ \ \
\\
\\
{\textrm{Then:}} \ \ \
\dfrac {y}{x \div n}&={z} \\
\end{aligned}
$$ $$\\[3pt]$$ Next, we need to find the formula for `EARB`, which we can do by taking the formula for `DAR` and solving for $y$, which gives us:

$$\\[3pt]$$

$$
\dfrac {zx}{n}={y}
$$

$$\\[3pt]$$

Let's look at our table again, but this time let's say that we would like to have achieved a `DAR` of **39.44.** What **Ending AR Balance** would we have needed to achieve this result?

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | ***Desired DAR*** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-----------------------:|
|       30       | \$131,440.30  |      *?*       |  \$4,381.34   |       ***39.44***       |

: Calculate EARB Required for $x$ DAR.

$$\\[3pt]$$

If we plug our known variables into our formula for EARB, we get an `EARB` of **\$172,800.18**. This is the Ending AR Balance needed to achieve **39.44** Days in AR, given the other variables.


```r

# DAR multiplied by GCt, then divided by NDiP, equals EARB

(39.44*131440.30)/30
#> [1] 172800.2
```

$$
\dfrac {39.44 \times 131,440.30}{30}={172,800.18}
$$

$$\\[3pt]$$

## Total Gross Charges Required for $x$ DAR

We can perform the same steps if we wanted to know the **total Gross Charges** we'd need to attain a certain number of **Days in AR**. Let's again take our original table of results and set up the calculation:

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | **DAR** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-------------:|
|       30       | \$131,440.30  |  \$203,460.50  |  \$4,381.34   |     46.44     |

$$\\[3pt]$$

We have our DAR formula converted to variables:

$$
\begin{aligned}
{\textrm{If:}} \ \ \
\dfrac {\textrm{EARB}}{\textrm{GCt} \div \textrm{NDiP}}&={\textrm{DAR}} \\
\\
\\
{\textrm{Where:}}\ \ \
{\textrm{EARB}}&=y\\ \ \
{\textrm{GCt}}&=x\\ \ \
{\textrm{NDiP}}&=n\\ \ \
{\textrm{DAR}}&=z\\ \ \
\\
\\
{\textrm{Then:}} \ \ \
\dfrac {y}{x \div n}&={z} \\
\end{aligned}
$$ $$\\[3pt]$$

To find the formula for `GCt`, we take the formula for `DAR` and solve for $x$, giving us:

$$\\[3pt]$$

$$
\dfrac {yn}{z}={x}
$$

$$\\[3pt]$$

Looking back at our table, we would again like to have achieved a `DAR` of **39.44.** What **total Gross Charges** would we have needed to achieve this result?

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | ***Desired DAR*** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-----------------------:|
|       30       |      *?*      |  \$203,460.50  |  \$4,381.34   |       ***39.44***       |

: Calculate GCt Required for $x$ DAR.

$$\\[3pt]$$

If we plug our known variables into our formula for **total Gross Charges**, we get a `GCt` of **\$154,762.04**. As the **Average Daily Charge** is determined in part by `GCt`, this calculation will also change it, to **\$5,158.74**.


```r

# EARB multiplied by NDiP, then divided by DAR equals GCt

(203460.50*30)/39.44
#> [1] 154762

# GCt divided by NDiP equals ADC

154762.04/30
#> [1] 5158.735
```

$$
\begin{aligned}
\dfrac {203,460.50 \times 30}{39.44}&={154,762.04}\\
\\
\\
\dfrac {154,762.04}{30}&={5,158.74}
\end{aligned}
$$ $$\\[3pt]$$

## Number of Days Required for $x$ DAR

We can perform the same steps if we wanted to know the **Number of Days** we'd need to attain a certain number of **Days in AR**. Let's again take our original table of results and set up the calculation:

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | **DAR** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-------------:|
|       30       | \$131,440.30  |  \$203,460.50  |  \$4,381.34   |     46.44     |

$$\\[3pt]$$

We have our DAR formula converted to variables:

$$
\begin{aligned}
{\textrm{If:}} \ \ \
\frac {\textrm{EARB}}{\textrm{GCt} \div \textrm{NDiP}}&={\textrm{DAR}} \\
\\
\\
{\textrm{Where:}}\ \ \
{\textrm{EARB}}&=y\\ \ \
{\textrm{GCt}}&=x\\ \ \
{\textrm{NDiP}}&=n\\ \ \
{\textrm{DAR}}&=z\\ \ \
\\
\\
{\textrm{Then:}} \ \ \
\frac {y}{x \div n}&={z} \\
\end{aligned}
$$ $$\\[3pt]$$

To find the formula for `NDiP`, we take the formula for `DAR` and solve for $n$, giving us:

$$\\[3pt]$$

$$
\frac {zx}{y}={n}
$$ $$\\[3pt]$$

Looking back at our table, we would again like to have achieved a `DAR` of **39.44.** What **Number of Days in the Period** would we have needed to achieve this result?

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | ***Desired DAR*** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-----------------------:|
|      *?*       | \$131,440.30  |  \$203,460.50  |  \$4,381.34   |        **39.44**        |

: Calculate NDiP Required for $x$ DAR.

$$\\[3pt]$$

If we plug our known variables into our formula for total Gross Charges, we get an `NDiP` of **25.48**. As the **Average Daily Charge** is determined in part by `NDiP`, this calculation will also change it, to **\$5,158.57**.


```r

# DAR multiplied by GCt, then divided by EARB, equals NDiP

(39.44*131440.30)/203460.50
#> [1] 25.47917

# GCt divided by NDiP equals ADC

131440.30/25.48
#> [1] 5158.568
```

$$
\begin{aligned}
\dfrac {39.44 \times 131,440.30}{203,460.50}&={25.48}\\
\\
\\
\dfrac {131,440.30}{25.48}&={5,158.57}
\end{aligned}
$$

$$\\[3pt]$$

## Average Daily Charge Required for $x$ DAR

This formula is going to be a bit different from the previous three. Remember, our formula for the **Average Daily Charge** is:

$$\\[3pt]$$

$$
\dfrac {\textrm{Gross Charges}}{\textrm{Number of Days in Period}} = {\textrm{Average Daily Charge}}
$$ $$\\[3pt]$$

Let's take our DAR formula and make the appropriate adjustments:

$$
\begin{aligned}
{\textrm{If:}} \ \ \
\dfrac {\textrm{EARB}}{\textrm{ADC}}&={\textrm{DAR}} \\
\\
\\
{\textrm{Where:}}\ \ \
{\textrm{EARB}}&=y\\ \ \
{\textrm{ADC}}&=c\\ \ \
{\textrm{DAR}}&=z\\ \ \
\\
\\
{\textrm{Then:}} \ \ \
\dfrac {y}{c}&={z} \\
\end{aligned}
$$ $$\\[3pt]$$

To find the formula for `ADC`, we take the formula for `DAR` and solve for $c$, giving us: $$\\[3pt]$$

$$
\dfrac {y}{z}={c}
$$

$$\\[3pt]$$

Looking back at our table, we would again like to have achieved a `DAR` of **39.44.**

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | **DAR** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-------------:|
|       30       | \$131,440.30  |  \$203,460.50  |  \$4,381.34   |     46.44     |

$$\\[3pt]$$

What **Average Daily Charge** would we have needed to achieve this result?

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | ***Desired DAR*** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-----------------------:|
|       30       | \$131,440.30  |  \$203,460.50  |      *?*      |        **39.44**        |

: Calculate ADC Required for $x$ DAR.

$$\\[3pt]$$

If we plug our known variables into our formula for **Average Daily Charge**, we get an `ADC` of **\$5,158.74**. As a change in `ADC` will effect `GCt`, we'll use the `ADC`-centric formula for `GCt` to calculate it, giving us **\$154,762.05**.


```r

# EARB divided by DAR equals ADC

203460.50/39.44
#> [1] 5158.735

# NDiP multiplied by ADC equals GCt

30*5158.735
#> [1] 154762
```

$$
\begin{aligned}
\dfrac {203,460.50}{39.44}&={5,158.74}\\
\\
\\
{30 \times 5,158.74}&={154,762.05}
\end{aligned}
$$

$$\\[3pt]$$

## Average Daily Charge-Related Formulas

For completeness' sake I'm going to include the formulas for `EARB`, `NDiP`, and `GCt` that include the `ADC` variable ($c$):

$$
\begin{aligned}
{\textrm{Where:}}\ \ \
{\textrm{EARB}}&=y\\ \ \
{\textrm{NDiP}}&=n\\ \ \
{\textrm{GCt}}&=x\\ \ \
{\textrm{ADC}}&=c\\ \ \
{\textrm{DAR}}&=z\\ \ \
\\
\\
{\textrm{Then:}} \ \ \
{z \times c}&={y} \\
{x \div c}&={n} \\
{n \times c}&={x} \\
\end{aligned}
$$ $$\\[3pt]$$

We'll test these out to make sure everything's in order:

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | **DAR** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-------------:|
|       30       | \$131,440.30  |  \$203,460.50  |  \$4,381.34   |     46.44     |

$$\\[3pt]$$


```r

# 1. DAR multiplied by ADC = EARB
46.43793010499292*4381.343
#> [1] 203460.5

# 2. GCt divided by ADC equals NDiP
131440.30/4381.343
#> [1] 30

# 3. NDiP multiplied by ADC equals GCt
30*4381.343
#> [1] 131440.3
```

And, as you can see, everything adds up. One note is that you do want to be mindful to include the entire number and every one of its decimals in the calculations for accuracy, then round up afterwards. Hopefully by now, you're beginning to see some patterns emerging that begin to illustrate the relationship between all of the variables that make up the DAR calculation.

## Relationship Between the DAR Variables

If you noticed, we now have two different formulas for the **Average Daily Charge**:

$$\\[3pt]$$

$$
\begin{aligned}
\dfrac {\textrm{GCt}}{\textrm{NDiP}} &= {\textrm{ADC}}
\\
\\
\\
\dfrac {\textrm{EARB}}{\textrm{DAR}} &= {\textrm{ADC}}
\end{aligned}
$$

$$\\[3pt]$$

If these are both true, then we can assume that both of the following equations are true:

$$\\[3pt]$$

$$
\begin{aligned}
\dfrac {\textrm{GCt}}{\textrm{NDiP}} &= \dfrac {\textrm{EARB}}{\textrm{DAR}}
\\
\\
\\
\dfrac {\textrm{DAR}}{\textrm{NDiP}} &= \dfrac {\textrm{EARB}}{\textrm{GCt}}
\end{aligned}
$$

$$\\[3pt]$$

Or, in mathematical terms:

$$\\[3pt]$$

$$
\begin{aligned}
\dfrac {x}{n}&=\frac {y}{z}
\\
\\
\\
\frac {z}{n}&=\frac {y}{x}
\end{aligned}
$$

$$\\[3pt]$$

Let's test this equivalency out with our original report values:

$$\\[3pt]$$

| **NDiP** ($n$) | **GCt** ($x$) | **EARB** ($y$) | **ADC** ($c$) | **DAR** ($z$) |
|:--------------:|:-------------:|:--------------:|:-------------:|:-------------:|
|       30       | \$131,440.30  |  \$203,460.50  |  \$4,381.34   |     46.44     |

$$\\[3pt]$$


```r

# 1. GCt divided by NDiP equals ADC
131440.30/30
#> [1] 4381.343

# 2. EARB divided by DAR equals ADC
203460.50/46.43793010499292
#> [1] 4381.343

# 3. EARB divided by GCt equals the DAR Ratio
203460.50/131440.30
#> [1] 1.547931

# 4. DAR divided by NDiP equals the DAR Ratio
46.43793010499292/30
#> [1] 1.547931
```

$$\\[3pt]$$

$$
\begin{aligned}
\dfrac {131,440.30}{30}&=\dfrac {203,460.50}{46.43793}
\\
\\
\\
\dfrac {46.43793}{30}&=\dfrac {203,460.50}{131,440.30}
\end{aligned}
$$

$$\\[3pt]$$

Again, you'll want to include all of the decimals in the calculation for absolute accuracy, but:

1.  the **total Gross Charges** divided by the **Number of Days in the Period** is equal to the **Ending AR Balance** divided by the average **Days in AR**. Not only that,

2.  the average **Days in AR** divided by the **Number of Days in the Period** is equal to the **Ending AR Balance** divided by the **total Gross Charges**.

This is an important relationship called the **DAR Ratio** that we'll explore in depth in the next chapter.

$$\\[3pt]$$

## Formula Quick Reference

The following table contains a summary of each of the formulas we have discussed in this chapter.

$$\\[3pt]$$

| **Name**       | **Formula**               | **Variable Form**         |
|----------------|---------------------------|---------------------------|
| DAR^1^         | `EARB` / (`GCt` / `NDiP`) | $y \div (x \div n) = z$   |
| DAR^2^         | `EARB` / `ADC`            | $y \div c = z$            |
| GCt^1^         | (`EARB` x `NDiP`) / `DAR` | $(y \times n) \div z = x$ |
| GCt^2^         | `NDiP` x `ADC`            | $n \times c = x$          |
| EARB^1^        | (`DAR` x `GCt`) / `NDiP`  | $(z \times x) \div n = y$ |
| EARB^2^        | `DAR` x `ADC`             | $z \times c=y$            |
| NDiP^1^        | (`DAR` x `GCt`) / `EARB`  | $(z \times x) \div y = n$ |
| NDiP^2^        | `GCt` / `ADC`             | $x \div c={n}$            |
| ADC^1^         | `GCt` / `NDiP`            | $x \div n = c$            |
| ADC^2^         | `EARB` / `DAR`            | $y \div z = c$            |
| DAR *Ratio*^1^ | `EARB` / `GCt`            | $y \div x$                |
| DAR *Ratio*^2^ | `DAR` / `NDiP`            | $z \div n$                |
