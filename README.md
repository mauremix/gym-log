# Gym Log

## About
A training log application that records workout sessions, helping users to monitor performance and evaluate progress over time—with the simplicity of a phone note and the power of data-driven insights.

## Domain Structure 
```
 Block (usually 4 months period)
    └── Mesocycle (usually a month. 3–4 per block)
           └── Microcycle
                └── Session
                        └── Component (upper, lower, core, rehab)
                                └── Exercise
                                        └── Sets (weight, reps, RIR -reps in reserve-, comment, metadata)
```

## Log Protocol
> <exercise_name>: <weight><unit> x <reps(RIR)> / <reps(RIR)> / …  // <optional_comment>

example: 
> bicep curl: 22kg x 12(2)/10(0)/8(0) // good one 

meaning:
* Weight: 22 kg 
* Sets: 3
    * Set 1: 12 reps, 2 RIR
    * Set 2: 10 reps, 0 RIR
    * Set 3: 8 reps, 0 RIR
* Comment: "good one"


In addition, each log contains the following metadata of when the exercise was performed:
* Block
* Cycle
* Week
* Session Day
* day and hour
