# Bus_Route_ML
This repo is a demo of coding for a fake bus routes with states, routes, bus types, passengers, and dates that creates a data set with multiple adjustable variables.
I originally created this dataset to test potential new hires skills and current team with Power BI and Excel data cleaning and dashboard development.
There is an associated word document that tells the new hire the requirements and gives pricing sheet. This tests the ability to extrabolate the price info to add it to a dashboard or determine other errors.

==What this dataset does===
This generator can be reused to create different datasets for different purposes. Each run can be tuned to embed a specific finding — one version might show Route 7 consistently overcrowded and needing larger buses, another might show oversized buses being underused across Texas. Each version tests a different kind of pattern recognition, from single-route capacity issues to state-level inefficiencies.

This also makes it useful for group testing: generating slightly different datasets per trainee prevents them from sharing answers while still testing the same skills.

===Data set creation controls===
1. N_ROWS: Number of rows of data to create. (some errors make more for duplicates)
2. Seed number: random number generation (28)
3. CLEAN MODE: (True / False) all errors are turned off. Used for ML to ensure errors do not cause issues when testing.
4. Run Label: name of file if multiple need to ne created

===World===
This is the world creation section. Currently it covers vehicle type, routes, state, and riders. These are based on a random number generator, paired with weights to skew the data depending on a few factors. The names, route-to-state pairs, and weights can each be adjusted independently to add more vehicle types, routes, or states, rearrange existing ones, or change the weights — producing a different dataset from the same underlying structure.

Entities: States
Routes: States with routes associated
Vehicle: Types - Standard, HellCat, Mini, Volt
Vehicle Multiplier:
Vehicle Capacity: Limit on the number of riders per vehicle type

Vehicle weights by tier: assigned weight for each route.
Each vehicle type is assigned a weight per route tier (busy, moderate, quiet). Busy routes are weighted toward larger buses, quiet routes toward smaller ones. This creates a learnable relationship between route volume and vehicle type which lets the dataset intentionally include oversized-bus inefficiencies for a ML analysis or analyst to catch.
Route Multiplier:



===Errors===

===Planned projects===
create bus route data - Working
Data error exploration and cleaning - in progress
ML projects - in progress



Development notes: Dataset generation logic was built with Claude (Anthropic) as a coding assistant. Data creation logic, Error-injection design, dashboard requirements, and analysis approach are my own.
