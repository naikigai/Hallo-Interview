# Elevator Design LLD problem

Requirements Feedback :

### What went well

- Your hardware setup is solid and well-aligned with what you learned from clarifying questions — 3 elevators, 10 floors, hall call panels with UP/DOWN direction, and destination panels inside the elevator are all captured correctly. 
- You've kept your error handling section from the last attempt, calling out that invalid floor numbers should be rejected — that's an important system-level concern and it's good to see it held in place. 
- Your out-of-scope section is clean and accurate, correctly excluding weight capacity and emergency/fault handling. 

### What needs improvement

- Your workflow section is a good start but it's still missing the system's dispatching responsibility — you describe a user clicking a hall button and an elevator arriving, but your requirements don't state that the system must choose and dispatch an appropriate elevator to service that call. This is the core behavioral job of the control system, and interviewers will probe on it. 
- The tick-based simulation is still absent from your requirements — the system advances in discrete time steps via a step() function, and this is a fundamental design constraint that will shape how you model state transitions. Since you didn't ask about it, consider raising it with the interviewer before you start designing: 'Is this a real-time system or does it advance in simulation steps?' 

### Minor suggestions

- You might also consider noting that invalid direction inputs on a hall call panel (anything other than UP or DOWN) should be rejected — it's a natural companion to the floor validation you already have. 
