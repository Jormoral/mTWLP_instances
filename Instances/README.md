# Instance Documentation
# multiple time window learning problem (mTWLP)

## Overview
This document provides an overview and detailed description of the mTWLP instances stored in `.txt`. An instance includes
users and depot time windows and a time matrix. The instances are created using the
[Traffic signs dataset of Montréal](https://open.canada.ca/data/en/dataset/59511eff-8924-4436-973d-f26c261d680e). The distances between nodes were calculated
using the haversine formula. Then, a uniform service time of 3 minutes, and the average vehicle speed of 8.8 m/s have been used to calculate the time matrices.

For more information about the instances' creation, refer to the original manuscript [Mortes et al. (2025)](https://www.sciencedirect.com/science/article/pii/S2352146524005192).

## File Structure
The TXT file has the same structure as the solomon instances for the traveling salesman problem with time windows (TSPTW), separating values using a space. The structure is the following:

* Number of nodes (including the depot).
* Time matrix. The first row is the time from the depot to the other nodes. The first column is the time from the other nodes to the depot. This time represents the travel time between nodes i and j, plus the service time at node i.
* Time windows for each node. The first node is the depot. The time window format is the following: earliest_1 latest_1 earliest_2 latest_2 ... earliest_i latest_i, where i is the number of time windows of this customer.

## Instance example

```txt
4
0 20 21 15
20 0 5 11
21 5 0 12
15 11 12 0
0 480
0 210 390 480
0 30 180 480
330 480