# PERT-CPM-Insurance-Company
Nothing much just a random-ASS_ignment 

![image](https://github.com/user-attachments/assets/b342553f-7fab-467e-8b46-d432f5614624)

Insurance Company Relocation: PERT/CPM Analysis Solution
Case Background
An insurance company has decided to shift its existing site to a new location. Some existing equipment will be discarded, while the remaining equipment will be kept. Tenders are accepted from potential contractors except for equipment removal.

![image](https://github.com/user-attachments/assets/61e12aac-164e-4fe7-9e05-010fb80956ec)

Solutions
1. Network Diagram
![image](https://github.com/user-attachments/assets/b342553f-7fab-467e-8b46-d432f5614624)

2. Minimum Time for Renovation from Design Stage
To calculate the minimum time for renovation from the design stage, we need to identify the critical path and sum the durations of activities along this path.
Forward Pass (Early Start and Early Finish)

A: ES = 0, EF = 0 + 14 = 14
B: ES = 14, EF = 14 + 4 = 18
C: ES = 18, EF = 18 + 2 = 20
D: ES = 20, EF = 20 + 1 = 21
E: ES = 14, EF = 14 + 2 = 16
F: ES = 14, EF = 14 + 3 = 17
G: ES = 16, EF = 16 + 2 = 18
H: ES = 16, EF = 16 + 4 = 20
K: ES = max(21, 17, 18) = 21, EF = 21 + 4 = 25
J: ES = 25, EF = 25 + 12 = 37
L: ES = 37, EF = 37 + 2 = 39
I: ES = max(20, 39) = 39, EF = 39 + 3 = 42
M: ES = max(20, 39) = 39, EF = 39 + 2 = 41

Backward Pass (Late Finish and Late Start)

I: LF = 42, LS = 42 - 3 = 39
M: LF = 42, LS = 42 - 2 = 40
L: LF = min(39, 40) = 39, LS = 39 - 2 = 37
J: LF = 37, LS = 37 - 12 = 25
K: LF = 25, LS = 25 - 4 = 21
D: LF = 21, LS = 21 - 1 = 20
C: LF = 20, LS = 20 - 2 = 18
B: LF = 18, LS = 18 - 4 = 14
A: LF = 14, LS = 14 - 14 = 0
F: LF = 21, LS = 21 - 3 = 18
G: LF = 21, LS = 21 - 2 = 19
E: LF = min(19, 35) = 19, LS = 19 - 2 = 17
H: LF = min(39, 40) = 39, LS = 39 - 4 = 35

Critical Path Identification
Activities with zero float (LS - ES = 0 or LF - EF = 0) are on the critical path:
Critical Path: A → B → C → D → K → J → L → I
Total duration of the critical path:
14 + 4 + 2 + 1 + 4 + 12 + 2 + 3 = 42 weeks
Therefore, the minimum time for renovation from the design stage is 42 weeks.
3. Independent Float for Non-Critical Activities
Independent float is the amount of time an activity can be delayed without affecting the earliest start of its successors or the latest finish of its predecessors.
Formula for Independent Float (IF)
IF = max(0, ES(j) - LF(i) - Duration)
Where:

ES(j) is the Early Start of the successor activity
LF(i) is the Late Finish of the predecessor activity

For activities with multiple successors, we take the minimum ES of all successors. For activities with multiple predecessors, we take the maximum LF of all predecessors.
Calculations for Non-Critical Activities

Activity E:

Predecessors: A (LF = 14)
Successors: G (ES = 16), H (ES = 16)
Duration: 2 weeks
IF = max(0, min(16, 16) - 14 - 2) = max(0, 0) = 3 weeks


Activity F:

Predecessors: A (LF = 14)
Successors: K (ES = 21)
Duration: 3 weeks
IF = max(0, 21 - 14 - 3) = max(0, 4) = 4 weeks


Activity G:

Predecessors: E (LF = 19)
Successors: K (ES = 21)
Duration: 2 weeks
IF = max(0, 21 - 19 - 2) = max(0, 0) = 3 weeks


Activity H:

Predecessors: E (LF = 19)
Successors: I (ES = 39), M (ES = 39)
Duration: 4 weeks
IF = max(0, min(39, 39) - 19 - 4) = max(0, 16) = 19 weeks


Activity M:

Predecessors: H (LF = 39), L (LF = 39)
Successors: None (project end, ES = 42)
Duration: 2 weeks
IF = max(0, 42 - max(39, 39) - 2) = max(0, 1) = 1 week



Therefore, the independent floats for non-critical activities are:

Activity E: 3 weeks
Activity F: 4 weeks
Activity G: 3 weeks
Activity H: 19 weeks
Activity M: 1 week

Summary

The network diagram is provided above, showing all activities and their dependencies.
The minimum time for renovation from design stage is 42 weeks.
The independent floats for non-critical activities are: E (3 weeks), F (4 weeks), G (3 weeks), H (19 weeks), and M (1 week).
