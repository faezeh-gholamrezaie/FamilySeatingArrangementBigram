# Family Seating Arrangement Bigram
This repository contains a Python code implementation for generating optimal seating arrangements for 400 individuals based on specified constraints.
<div align="center">
    <img width="40%" src="https://github.com/faezeh-gholamrezaie/FamilySeatingArrangementBigram/blob/main/EfficientSeating.png">
</div>

## Overview
In this project, we start by generating 400 random names for individuals. These names include both first names and surnames. Next, we organize these individuals into 80 groups of 5, ensuring each group is contiguous.

To simulate seating arrangements, we create differences between individuals, ensuring that individuals within the same group have zero differences. We construct a difference matrix where individuals with differences are marked with a value of 1.

For the main task, we compute differences between the 80 groups. A group can have up to 4 differences with its neighboring groups. The probability of these differences is computed using torch.multinomial, considering initial random weights (W) and defining a loss function (LOSS). The primary goal is to arrange groups such that differences between them are minimized first, followed by minimizing differences between individuals within each group.

### Implementation Details
- Data Generation: Random generation of 400 names.
- Group Formation: Creation of 80 contiguous groups of 5 individuals each.
- Difference Calculation: Construction of a difference matrix to track differences between individuals.
- Optimization: Use of torch.multinomial to optimize the seating arrangement, prioritizing minimal inter-group and intra-group differences.
#### Output
The output of this model is a list of 400 names arranged in optimal contiguous seating groups, minimizing differences between both groups and individuals within groups.

