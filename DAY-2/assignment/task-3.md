# Metrics Calculation

![Question](../screenshots/Question.png)

*Given*
- *Total deployment: 40*
- *Deployment causing incidents: 6*
- *Working Days: 20*
- *Lead Time for Change (average): 3 hours*
- *Incident detection + resolution times:*
    1. 10:00 AM → 11:30 AM
    2. 2:00 PM → 2:45 PM
    3. 9:00 AM → 11:00 AM
    4. 4:00 PM → 8:00 PM
    5. 1:00 PM → 1:30 PM
    6. 11:00 AM → 3:00 PM

*now,*

## 1. Deployment Frequency (per day)

*Deployment Frequency= Total Deployments/Total working days*

    Deployment Frequency = 40/20          
    2 deployment per day
    Answer: 2 deployment per day

## 2. Lead Time for Changes

    Given average time from commit → production:
    Lead Time = 3 hours

## 3. Change Failure Rate (CFR)

*Change in failure rate is percentage of deployments that cause failure in production.*
    CFR = (6/40)*100%  
        = 15%

    therefore,
    Change Failure Rate = 15%

## 4. Mean Time to Recovery (MTTR)

*Mean time to recovery is the avg. time needed to fix the system after failure.*

    Calculate duration of each incident:

    | Incident | Detected | Resolved | Duration (hours) |
    |----------|----------|----------|------------------|
    | 1        | 10:00 AM | 11:30 AM | 1.5              |
    | 2        | 2:00 PM  | 2:45 PM  | 0.75             |
    | 3        | 9:00 AM  | 11:00 AM | 2                |
    | 4        | 4:00 PM  | 8:00 PM  | 4                |
    | 5        | 1:00 PM  | 1:30 PM  | 0.5              |
    | 6        | 11:00 AM | 3:00 PM  | 4                |

    Sum of durations = 1.5 + 0.75 + 2 + 4 + 0.5 + 4 = 12.75 hrs

    MTTR = 
    12.75/6 = 2.125 hrs

    therefore,
    MTTR = 2.125 hours

## 5. Team Classification Based on DORA Metrics

| Metric                   | Value          | Elite                | High                 | Medium                | Low                  |
|--------------------------|----------------|----------------------|----------------------|-----------------------|----------------------|
| Deployment Frequency     | 2 per day      | Multiple per day     | Daily                | Between weekly/monthly| yearly or more       |
| Lead Time for Changes    | 3 hours        | <1 hour              | 1 day                | 1 week                | >1 month             |
| Change Failure Rate (%)  | 15%            | 0-15%                | 16-30%               | 31-45%                | >45%                 |
| MTTR                     | 2.125 hours    | <1 hour              | <1 day               | <1 week               | >1 week              |

### Interpretation

- **Deployment Frequency=**  2 per day → Between High and Elite  
- **Lead Time for Changes=** 3 hours → Closer to High  
- **Change Failure Rate=**   15% → At the border of Elite and High  
- **MTTR=**                  2.125 hours → Closer to High  

### Overall Classification

The team is a **High performer**, close to Elite, based on the above DORA metrics.

---



