# Work Units

This blog post explains, conceptually, the foundations of the Work Unit system that is used within my [AI Agent fleet](The-Fleet.md). It is also a technical spec sheet, so that you may choose to implement it yourself[^3].

## Table of Contents
1. [What Are Work Units?](#what-are-work-units)
2. [Alternatives to Work Units - Why Didn't They Work?](#alternatives-to-work-units)
- 2.1 [Spoon Theory](#spoon-theory)
- 2.2 [Battery Analogy](#battery-analogy)
3. [How to Use Them](#how-to-use-work-units)
- 3.1 [Identify your tasks](#identify-your-tasks)
- 3.2 [Assess your tasks](#assess-your-tasks)
- 3.3 [Calculate Work Unit disbursement and accrual](#calculate-work-unit-disbursement-and-accrual)
- 3.4 [Weekly/monthly recap](#weekly-or-monthly-recap)
4. [Summary and Closure](#summary-and-closure)

# What Are Work Units?
The easiest way to describe a Work Unit is as follows:
> A Work Unit represents thirty minutes of ideal work[^0]. It serves as a reference unit for quantifying the cognitive and structural load required to execute an event or task.

Two tasks of equal length may consume radically different numbers of Work Units depending on:
- Cognitive intensity
- Social demands
- Environmental stimulation
- Masking requirements
- Decision density
- Context switching
- Recovery requirements

Work Units therefore measure structural impact, not clock time. 

# Alternatives to Work Units
**(AKA: Why didn't the alternatives work? How do we fix that to make a system built for the greater good?)**

Work units are inspired by two main, competing analogies used within the disability community: Christine Miserandino's concept of the 'spoon theory,'[^1] and the 'battery analogy'[^2] which, as far as my knowledge, was not coined by one member of the disability community but was independently created across disparate chronic illness forums as smartphone and battery-oriented technology became more prevalent. This section discusses why both of these theories are useful, but not useful enough for the context in which Work Units are employed. Spoons and battery percentages are **not deterministic enough**, **don't have the proper structure to be used by machines and humans**, and otherwise are unfit for purpose because of **the need to explain the analogy in a concise manner.** A Work Unit is also not *just* for disabled people. Anyone, at any time, is welcome to use the Work Unit spec. 

## Spoon Theory
With all due respect to Miserandino, the spoon theory is great as a beginning introduction to the world of capacity management and fatigue. However, for more expansive models, the spoon theory just does not work. How many spoons does one start with? 10? 20? 1,000? I can't imagine tracking that consistently. The analogy also doesn't have as long of a reach as Work Units do. The original analogy only talks of borrowing a spoon from the 'next day.' What happens if you are continually borrowing spoons? Is there a way to regain spoons that one has lost? Conjectures like this are, well, improvised and thought out for specific in-the-moment benefit, and in the long term don't have accountability or tracking. 

It's a powerful explanatory tool still used by many disabled and chronically ill people, so I don't want to disparage it.

## Battery Analogy
This analogy used to be the one that I used to describe my capacity needs before I devised Work Units. It makes inherent sense, is easy to explain to anyone who's familiar with a smart battery-powered device, and accounts for recharge activities. It has the same issue as spoon theory, though, in that it lacks long-term foresight. The 'context window,' so to speak, is only a few days, if not a week at most. This works for people whose lives are cyclical and/or otherwise needing to plan in the short-term because of the inevitability of flare-ups or other illness-related symptoms and issues.

# How to Use Work Units
Work Unit allocations follow a fairly simple process:
1. [Identify your tasks](#identify-your-tasks)
2. [Assess your tasks](#assess-your-tasks)
3. [Calculate Work Unit disbursement and accrual](#calculate-work-unit-disbursement-and-accrual)
    - [Daily sustainability](#what-is-the-sustainable-range-of-work-units-one-should-spend-or-complete-in-one-day)
    - [Mathematical formulae](#mathematical-formulae)
4. [Weekly/monthly recap](#weekly-or-monthly-recap)
    - [Example week](#example-week)

## Identify your tasks
This is the hardest part of the entire Work Unit process. What are the **recurring**, **visible tasks** in your life? 
This could include:
- Work shifts
- Academic obligations (lectures, known weekly quizzes, etc.)
- Volunteer or personal recurring obligations (church, errands)
- Travel

The Work Unit system also allows for recovery tracking and long-range planning. Ensure that you include tasks that refill you, such as:
- Time to work on your hobbies or special interests
- Seeing friends
- Scheduled time off

Work Units aren't meant to maximize productivity at one's personal expense. Instead, Work Units are meant to help you allocate your time and energy to the things that mean the most, while still being able to balance mandatory tasks and obligations.

## Assess your tasks
As stated earlier, a Work Unit represents thirty minutes of ideal work. This definition is now the baseline for which all Work Units will be allocated for your tasks. A task’s Work Unit allocation reflects how many thirty-minute blocks of ideal work it consumes in **structural impact** — *not* in clock time. 

Examples of different tasks and their Work Unit allocations:
- A 75-minute lecture takes up 13 work units because of the higher cognitive load required to absorb information and take notes.
- Social obligations can consume up to 24 work units depending on length, sensory capacity, and political maneuvering.
- A thirty-minute drive in heavy traffic may consume more than one work unit due to travel fatigue.
- A high-visibility 45-minute presentation may cost more than a 90-minute lecture. 

Concretely, the most important part of allocating work units is knowing, conceptually, that time doesn't equal work units. Two activities of identical duration may have radically different structural costs. 

 For example, there are activities that can even *give* you work units, restoring your capacity to do deep work later:
- Working on a passion project or researching a special interest
- Low-demand social activity with trusted friends
- (Pretending to) read a book while holding a mug of tea.

After your first allocations, assessment becomes a structural exercise. 
Questions to ask yourself when allocating work units:
- How far is this task from ideal conditions?
- How much context-switching, evaluation pressure, and other cognitive load is present?
- Is there a sensory load that you need to account for?
- Is the task meant to support your recovery?

## Calculate Work Unit disbursement and accrual
Now that all of your tasks are allocated, calculating how many Work Units a day, or even a week, takes is simple. 

### What is the sustainable range of Work Units one should 'spend' or 'complete' in one day? 
There is no universal daily Work Unit limit. Completing Work Units and determining your range is covered in the [weekly or monthly recap](#weekly-or-monthly-recap). For the purposes of clarity, a sustainable daily range is the amount of Work Units you can complete:
- Without next-day strain or cognitive fog
- Without 'borrowing heavily' from the following day

Your 'baseline' will determine the range. Further, the baseline is never static. It reflects your current health, sleep quality, environmental stability, and cumulative load. Work Unit completion should be dynamically allocated.

It is important to note that in my personal implementation of the Work Unit system, the baseline is based on a weekly rolling average of activities I've completed. This allows the model to reflect real-world performance rather than theoretical capacity. Over time, the baseline will shift to reflect the user’s stable operating range.

### Mathematical formulae
To start, the *base* Work Unit allocation is:
`Daily Load = Σ (Task WU allocations)`[^3].

Load may carry across days, as follows:
`Net Loadₙ = Daily Loadₙ + Carryoverₙ₋₁ − Recoveryₙ`, where `Daily Loadₙ` = total work units for the day, `Carryoverₙ₋₁` = unresolved strain from the previous day, and `Recoveryₙ` is meaningful decompression or sleep quality adjustment. The ideal case is that `Daily Loadₙ - Recoveryₙ = 0`. In practice, this means recovery is sufficient to prevent baseline drift upward. Short-term elevation is expected; chronic elevation is not.

The baseline, as discussed earlier in this post, is calculated as a weekly rolling average of Work Units completed during *normal operating conditions*. Normal operating conditions are defined as weeks without illness, crisis events, travel disruptions, operational events beyond regular duty, or abnormal schedule volatility. This rolling-average baseline functions as a moving reference point. If the baseline trends upward over time without adequate recovery or structural supports in place, risk increases.

## Weekly or monthly recap
Work Unit allocation is not static. After using the system for a period of time, you should continually reassess how many Work Units a task actually consumes. Structural demand changes. 

For example, writing lecture notes in the first half of an academic semester may require more cognitive effort as you acclimate to the material and format. The same task in the second half of the semester may require fewer Work Units due to familiarity, pattern recognition, and improved efficiency. Conversely, the same task may increase in cost over time, such as an informal social obligation that turns into a formalized, structured club or extracurricular activity. 

Rigidity is the enemy of assessing true capacity. Reassessment ensures that the model reflects reality rather than assumption. Further, the exact same week will change in work units over time, which I will demonstrate in the following example:

### Example Week 1: Before Calibration
**Monday:**
- 2 lectures (13 Work Units each, 26 Work Units total)
- Social lunch with friends (7 Work Units)
- Drive home, in heavy traffic, for 30 minutes (3 Work Units)
This day ends up being 36 Work Units from standing calendar obligations. This total does not yet include discretionary tasks such as completing assignments, studying, errands, or unexpected interruptions.

**Tuesday:**
- 4 lectures (13 Work Units each, 52 Work Units total)
- Study group lunch and dinner with friends on-campus (14 Work Units)
- Meeting or job interview (10 Work Units)
- Evening club or extracurricular activity after dinner (10 Work Units)
This is 86 Work Units, so structurally we know this day needs more support than Monday. Even if each individual event is manageable in isolation, the cumulative load increases carryover risk.

**Wednesday:**
- 1 lecture (13 Work Units)
- Solo lunch picked up to-go (1 Work Unit)
- Independent assignment work (8 Work Units)
- Research special interest (0 Work Units, -4 Recovery Units)
**Important to note:** The formula to calculate Net Load applies here. 
In this case, Net Load = 22 Work Units (Structural Load) - 4 Recovery Units = 18 Work Units total for the day.

**Thursday:**
Same as Tuesday, so again, the total is 86 Work Units.
At this point, cumulative strain risk is high. Two 86 Work Unit days within the same week significantly exceed a typical baseline without structural support.

**Friday:**
- No lectures on Friday, nice! (0 Work Units)
- Club executive meeting (13 Work Units)
Total: 13 Work Units. This day is also a day to recover from the previous day. It reduces intensity but does not fully offset Tuesday/Thursday stacking.

**Saturday:**
- Weekly errands (10 Work Units)
- Afternoon work shift (10 Work Units)
Total: 20 Work Units

**Sunday:**
- Light planning for the week (6 Work Units)
- Low-demand social interaction (4 Work Units)
Total: 10 Work Units.

**Summary for the week:** 
The total work units for this week are 256 Work Units. The rolling baseline from this week would be **256/7 = ~37 Work Units**. 

For reference, eight hours of uninterrupted ideal work would equate to approximately 16 Work Units. In practice, most real-world workdays exceed this due to meetings, transitions, and social demands.

### Example Week 2: After Calibration
**Monday**
**Before Calibration:** 36 Work Units
**After Calibration:**
- 2 lectures (11 Work Units each, 22 Work Units total)
(Improved note system, reduced friction)
- Social lunch (6 Work Units)
(Bounded duration, lower masking)
- Drive home (2 Work Units)
(Optimized departure timing)

Total: 30 Work Units
Making structural changes and taking advantage of natural efficiency improvements decreases the Work Unit cost of this day by 6 Work Units, or roughly ~17%. 

**Tuesday**
**Before Calibration:** 86 Work Units
**After Calibration:**
- 4 lectures (11 Work Units each, 44 Work Units total)
(Improved familiarity; reduced note friction)
- Study group lunch + dinner (12 Work Units)
(Intentional pacing; bounded duration)
- Meeting or job interview (9 Work Units)
(Reduced anticipatory load)
- Evening club or extracurricular activity (8 Work Units)
(Delegation; reduced masking intensity)

Total: 73 Work Units
Structural refinement reduces the cost of this day by 13 Work Units, or approximately 15%. The day still remains high-density. Calibration does not eliminate heavy days, but these changes significantly improve recovery.

**Wednesday:**
**Before Calibration:** 18 Work Units (net load)
**Structural Load:** 22 Work Units
**Recovery Credit:** 4
**After Calibration:**
- 1 lecture (11 Work Units)
(Improved familiarity)
- Solo lunch (1 Work Unit)
- Independent assignment work (7 Work Units)
(More efficient workflow)
- Research special interest (0 Work Units structural, −6 Recovery Units)

**Structural Load:** 19 Work Units
**Recovery Credit:** 6
**Net Load:** 13 Work Units

Efficiency reduces structural cost slightly. Intentional recovery increases stabilization capacity.

**Thursday:**
Same schedule as Tuesday, so still 73 Work Units. 

**Friday:**
**Before Calibration:** 13 Work Units
**After Calibration:**
- No lectures on Friday! (0 Work Units)
- Club executive meeting (11 Work Units)
(Familiarity with the tasks and optimizing meeting agenda)

Very small changes to make tasks more efficient will compound later in the week.

**Saturday:**
**Before Calibration:** 20 Work Units
**After Calibration:**
- Weekly errands (8 WU)
(Optimized sequencing)
- Afternoon work shift (9 WU)
(Improved pacing)

Total: 17 Work Units

**Sunday:**
- Light planning for the week (4 Work Units)
- Low-demand social interaction (3 Work Units)
Total: 7 Work Units.

**Weekly Summary:**
Small changes add up. By making these improvements and reflecting them in Work Unit calculation, **29 Work Units** were shaved off of the week, making a **~37 Work Unit** baseline average turn into a **~32 Work Unit** baseline average. This is a ~11% reduction, but small numbers can deliver large results for quality-of-life.

# Summary and Closure
Work Units are not a metaphor. They are not a motivational tool. They are not a moral ledger for productivity. Instead, Work Units are a structural accounting system. 

Time is not cost. Two hours in a quiet room working on a passion project does not equal two hours in a crowded lecture hall or roundtable meeting. A low-demand hobby may restore more than it consumes. A task’s structural impact depends on context, stacking, autonomy, sensory load, and recovery. Without a shared unit, those differences collapse into vague language — “busy,” “tired,” “overwhelmed.” Work Units prevent that collapse and provide structured language to explain demand.

# Footnotes
[^0]: “Ideal work” means work performed under low sensory, social, and external cognitive load. For me, this means a quiet environment with minimal interruptions and high autonomy. For you, “ideal” may look different — but it must be consistent.
[^1]: The ‘spoon theory’ is as follows: take a set amount of units of energy (in the original analogy, spoons off of every cafe table within the vicinity of the author and her friend’s conversation), and lay them out in a row. These ‘spoons’ now represent the amount of energy that a disabled person has for the day. Each task will take up a set amount of ‘spoons’; once you are out of spoons for the day, you can choose to borrow from the next day to do more tasks, but know that the next day will have less energy to perform a task. (Henriksen, 2025, written for a Disability Studies in-class essay) [Link to the (archived) original essay by Miserandino for further reading.](https://web.archive.org/web/20191117210039/https://butyoudontlooksick.com/articles/written-by-christine/the-spoon-theory/)
[^2]: The battery analogy has been used by many chronic illness and disability communities, so there is not one 'true' explanation. The analogy I had previously found to be useful personally: Each person starts with a fully charged battery. The capacity of the battery, much like your smartphone, is degraded for those of us with a disability. It therefore follows that the battery will deplete faster when completing daily activities. Once your battery reaches 0%, you have to complete recovery activities to charge your battery. [Link here](https://themighty.com/topic/chronic-illness/cell-phone-theory-spoon-theory-energy-chronic-illness/) and [here](https://batemanhornecenter.org/wp-content/uploads/2024/10/Video-Transcript-Life-with-a-Low-Battery-Living-with-MECFS.pdf) for two allocations of the battery analogy that make sense to me.
[^3]: My personal implementation of the Work Unit has other bonuses and stacking modifiers calculated daily. That implementation is not going to be brought into this post, since it would detract from the generalized explanation. Full spec sheet of my specific implementation is available upon request.

#documentation #documentation/work-units
