---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

(python_by_example)=

# Economic Evaluation of NTFPS

## Overview

In order estimate the impact of the programme beyond identification of patients at risk of falls, it is necessary to estimate the effectiveness in terms of adverse events avoided, fractures given their personal, health and social care impact and accuracy of recording.  To establish the effectiveness of NTCFPS, we utilised routinely collected data regarding non-elective hospital admissions due to fractures in the exposed population; comparing trends whilst the service was in operation to those after the service had closed. Our research question was to determine whether the discontinuation of the NTCFPS was associated with a rise in the number of fracture rates in those aged over 60 years. 

## Data 

Outcomes of interest were non-elective admissions due to fractures of all types and hip fracture non-elective admissions for those aged over 60. Data was obtained from Northumbria Healthcare Trust (Caldicott Approval C3351) including the number of fracture events for patients registered at each GP practice, and the number of bed days for each event from April 2010 until December 2017. The number of over 60’s registered to each GP practice was obtained from NHS Digital with a yearly average taken. 
Although the service was introduced in 2009, there was a rolling adoption of GP practices (Table X). The four GP practices that had adopted the intervention in 2013 were excluded due to having less than one year of the NTFPS being activated. Although Techniques have been developed to allow the diff-in-diff approach to account for rolling adoption of an intervention (REF  ), for the purposes of this demonstration in this worked example we analysed the 14 practices who had adopted the NTFPS already by 2013 and ignored the consequences of rolling adoption. This resulted in 1 year where the NTFPS was operational in the exposed group and 4 years following service closure. 

TABLE HERE

The costing perspective used was that of the U.K. National Health Service (NHS) with all prices being in pounds sterling (£) using 2017-18 prices.  The cost of the programme was £194,000 per year which accounted for staff wages, overheads, equipment/maintenance, room rental, and two acute trust medic sessions. Bed days were costed at £438.71 per bed day (REF). Costs and events were discounted by 3.5% each year after 2013 (REF)

##construcitng dataset for analysis
The mixed model approach requires data to be constructed in a long format such that both cost and fracture event are listed in the same outcome variable “Dep Var”. To distinguish between the cost and fracture event outcomes for each year we include an “Outcome” variable which takes a value of 0 for fracture event and a value of 1 for cost. It should also be noted that to improve efficiency and speed of the analytical software, the events can be rescaled. In this example, cost variables were scaled down by 1000 to be in line with fracture events. Costs are then rescaled at a later stage in the analysis.  
For each GP practice, there are 10 entries: 5 periods (2013 to 2017) with a cost and an fracture event outcome for each. Time is centred on the intervention ending in 2014, with 2013- the pre-intervention year- values at -1, 2014 being valued at 0 and subsequent years following closure gaining the values 1,2,3 accordingly. There is an indicator variable “before and after” that takes a value of 0 for those years before intervention stopped and a 1 for those years after. There is also an exposure variable which takes a value of 0 for those in the control -no intervention- group and a 1 for those in the intervention group. We combine the “before and after” and “exposure” variables to create a “diff in diff” variable, which takes a value of 1 for post-intervention in the exposure group and a value of 0 for all else.  This variable would allow a grouped diff in diff analysis combining all of the pre and post events together. In order to identify diff-in-diff effects for each year post-exposure we can create “diff in diff” variables for each year, specifically “Diff 2014” “Diff 2015” “Diff 2016” “Diff 2017”, which each takes a value of 1 for the corresponding year post-exposure in the exposure cohort and a value of 0 for all else. 

TABLE HERE

## Statistical model 

Mixed model, no random effect outcome estimated from nonlinear combinations. Although Bootstrapping is a common method to capture uncertainty around parameters, the limited number of GP practices in this example limited the effectiveness of bootstrapping. As such we instead captured uncertainty using random draw from a normal distribution with the means defined by the coefficients from the regression and the variance defined by the and covariates. We note that in the worked example 2 using a simulated dataset we present an analysis which demonstrates the bootstrapping method. 

Outcomes were expressed in terms of event per over 60’s person at GP practice to account for differences in population between practices. Results are presented both on a per person basis and converted to a population level value. 

Regression Model here

explain regression model here

## How model works

Step by step of process -incl visual of output
 -regression output
 -convert using nlcom + why inlcuding rescale for costs and discounting

```{code-cell} ipython3
This is example code.
```

 ## Results
Total fractures:
- Effect in each year on cost and falls
- ICER + WTP for each year including graphs
- Overall across the 4 years combined

Hip fractures:
- Effect in each year on cost and falls
- ICER + WTP for each year including graphs
- Overall across the 4 years combined

## Interpreting results

Include discussion of results here


