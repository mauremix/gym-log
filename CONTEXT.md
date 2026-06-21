# Gym Log

"Gym Log" records training sessions so progress can be reviewed over time. Its language follows periodized strength-training concepts where training is organized from larger planning periods down to individual sessions.

## Language

**Block**:
The largest planned training period in the log, typically spanning several months. A Block starts on a Monday, ends on a Sunday, and contains a variable number of whole, contiguous Mesocycles; gaps are allowed between Blocks, but Blocks do not overlap. Blocks use numbered labels only.

**Mesocycle**:
A medium-length training period within a Block, usually around one month. A Mesocycle starts on a Monday, ends on a Sunday, and contains a variable number of whole, contiguous Microcycles, usually four. Mesocycles use numbered labels within their Block only.
_Avoid_: Cycle

**Microcycle**:
A fixed Monday-through-Sunday training week within a Mesocycle, containing zero or more Sessions. Microcycles use numbered labels within their Mesocycle only, and their dates are not edited individually.
_Avoid_: Week

**Session**:
A performed training day within exactly one Microcycle, labeled by its day of week and identified by its calendar date. There is at most one Session per calendar date, it belongs to the Microcycle active on that date, and it may collect Logs added at different times during that date. A Session cannot exist on a date without an active Block, Mesocycle, and Microcycle.
_Avoid_: Session Day

**Component**:
A section within a Session that groups Exercises by training focus. The canonical Components are Upper, Lower, Core, and Rehab, and each Component may appear at most once in a Session.

**Exercise**:
A reusable movement that can be performed across many Sessions, such as Bicep Curl. Each Exercise belongs to exactly one Component.

**Log**:
A performed instance of one Exercise at one required weight within a Component during a Session, including its Sets and notes. Within the same Session, an Exercise and Weight identify one Log; additional Sets at the same Weight belong to that Log. The same Exercise may have multiple Logs in one Session when it is performed with different weights; unweighted exercises are logged with a weight of zero.

**Weight**:
The load used for a Log, recorded in kilograms. A Weight of zero represents an unweighted Exercise.

**Set**:
One effort within a Log, recording repetitions and optional reps in reserve. The Log carries the weight used for all of its Sets.

**Log Protocol**:
The note-like shorthand used to enter structured Logs, including Exercise, Weight, Sets, optional reps in reserve, and optional notes.
