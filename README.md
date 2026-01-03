flowchart TD

A[Landing Page] --> B[Signup]
A --> C[Login]

C --> D{Role?}

D -->|Candidate| E[Candidate Dashboard]
D -->|Recruitment Admin| F[Admin Dashboard]
D -->|HR| G[HR Dashboard]

%% Candidate Flow
E --> E1[View / Update Profile]
E --> E2[View Job Feed]
E2 --> E3[Apply for Job]
E3 --> E4[Application Status: applied]
E4 --> E5[Track Application Status]

%% Admin Flow
F --> F1[Create / Publish Job]
F --> F2[View Jobs]
F2 --> F3[View Applicants]
F3 --> F4[Shortlist for Interview]
F4 --> F5[Application Status: shortlisted]

%% HR Flow
G --> G1[View Shortlisted Candidates]
G1 --> G2[Conduct Interview]
G2 --> G3{Decision}

G3 -->|Select| G4[Create Employee]
G4 --> G5[Employee Lifecycle]

G3 -->|Reject| G6[Application Status: rejected]

%% Future Extensions
G5 --> H1[Attendance]
G5 --> H2[Transfers]
G5 --> H3[Payroll]
G5 --> H4[Performance]
G5 --> H5[Grievance Redressal]
