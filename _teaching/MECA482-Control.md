---
title: "MECA 482 — Control System Design" # Course title shown on p.1. :contentReference[oaicite:0]{index=0}
collection: teaching
type: "Undergraduate course"               # Level inferred from course numbering and prerequisites.
venue: "California State University, Chico" # Institution on p.1. :contentReference[oaicite:1]{index=1}
institution: "California State University, Chico" # p.1 header. :contentReference[oaicite:2]{index=2}
course_code: "MECA 482"                    # p.1. :contentReference[oaicite:3]{index=3}
course_number: 482
term: "Fall 2019"                          # p.1. :contentReference[oaicite:4]{index=4}
level: "undergraduate"                     # Inferred.
status: "archived"                         # Course ran in 2019; set as archived for current list.
date: 2019-09-01                           # Fall 2019 start; use site’s preferred date format.
permalink: /teaching/2019-meca482-control  # Adjust if you have an existing URL slug.
tags: [control, SISO, modeling, state-space, root-locus, frequency-response, digital-control, reinforcement-learning] # Topics listed on pp.1–3. :contentReference[oaicite:5]{index=5}
featured: false
role: "Instructor"
years: "2019-2022"
pdfs:
  - label: "Syllabus"
    url: "/files/MECA_482_syllabus.pdf"

excerpt: "An introduction to classical control (e.g., SISO) and modern control (e.g., state-space). Modeling, stability, root locus, frequency response, digital control, labs, and a group project." # Topics pp.1–3. :contentReference[oaicite:6]{index=6}
short_description: "Classical SISO control with state-space introduction. Modeling, stability, root locus, frequency response, digital control, and learning-based control (optional)." # pp.1–3. :contentReference[oaicite:7]{index=7}

instructor:
  name: "H. Sinan Bank"                    # p.1. :contentReference[oaicite:8]{index=8}
  email: "hsbank@mail.csuchico.edu"        # p.1. :contentReference[oaicite:9]{index=9}
  phone: "530-898-4619"                    # p.1. :contentReference[oaicite:10]{index=10}
  office: "OCNL 428"                       # p.1. :contentReference[oaicite:11]{index=11}
  office_hours: "MW 2:00–4:00 pm; meetings via calendly.com/hsbank" # p.1. :contentReference[oaicite:12]{index=12}

sections:
  - section: "01 (3323)"                   # p.1. :contentReference[oaicite:13]{index=13}
    schedule: "MWF 12:00–12:50"
    location: "LANG 104"
  - section: "02 (5182)"                   # p.1. :contentReference[oaicite:14]{index=14}
    schedule: "MWF 1:00–1:50"
    location: "LANG 104"

learning_outcomes:
  - "Elicit and interpret the dynamic performance of a system." # Course Objective 1, p.1. :contentReference[oaicite:15]{index=15}
  - "Design controllers that meet stability, tracking, disturbance-robustness, and frequency-response requirements." # Objective 2, p.1. :contentReference[oaicite:16]{index=16}
  - "Understand and implement basic system identification with a given input." # Objective 3, p.1. :contentReference[oaicite:17]{index=17}
  - "Apply classical SISO methods and introductory state-space techniques." # Coverage bullets, p.1. :contentReference[oaicite:18]{index=18}

prerequisites:
  required:
    - "EECE 211"                           # p.1. :contentReference[oaicite:19]{index=19}
    - "MATH 260"                           # p.1. :contentReference[oaicite:20]{index=20}
  recommended:
    - "MECA 380"                           # p.1. :contentReference[oaicite:21]{index=21}
    - "MECH 320"                           # p.1. :contentReference[oaicite:22]{index=22}
    - "CSCI 111 or MECH 208"               # p.1. :contentReference[oaicite:23]{index=23}

texts:
  required:
    - "Nise, Control Systems Design, 7th ed., Wiley (2015)."    # p.1. :contentReference[oaicite:24]{index=24}
  suggested:
    - "Åström & Murray, Feedback Systems."                      # p.2. :contentReference[oaicite:25]{index=25}
    - "Golnaraghi & Kuo, Automatic Control Systems, 10th ed."   # p.2. :contentReference[oaicite:26]{index=26}
    - "Ogata, System Dynamics and Control, 4th ed."             # p.2. :contentReference[oaicite:27]{index=27}
    - "Close & Frederick, Modeling and Analysis of Dynamic Systems, 3rd ed." # p.2. :contentReference[oaicite:28]{index=28}
    - "Phillips, Nagle, & Chakrabortty, Feedback Control of Dynamic Systems, 4th ed." # p.2. :contentReference[oaicite:29]{index=29}
    - "Çetinkunt, Mechatronics with Experiments."               # p.2. :contentReference[oaicite:30]{index=30}

software:
  - "MATLAB (with required toolboxes noted in Blackboard)."      # p.2. :contentReference[oaicite:31]{index=31}
  - "Python 3.6 (see requirements.txt in course repository)."    # p.2. :contentReference[oaicite:32]{index=32}
  - "V-REP for physics-based simulation."                        # p.2. :contentReference[oaicite:33]{index=33}

lab_hardware: "In-class labs using simple physical systems to connect theory with practice." # p.2. :contentReference[oaicite:34]{index=34}

assessments:                                    # Weights on p.2. :contentReference[oaicite:35]{index=35}
  quizzes:
    count: 4
    weight: "20%"
    note: "(3+1) in-class; cumulative coverage possible."       # p.2. :contentReference[oaicite:36]{index=36}
  homeworks:
    count: 8
    weight: "20%"                                              # p.2. :contentReference[oaicite:37]{index=37}
  labs:
    count: 5
    weight: "10%"                                              # p.2. :contentReference[oaicite:38]{index=38}
  group_project:
    weight: "20%"                                              # p.2. :contentReference[oaicite:39]{index=39}
  final_exam:
    weight: "30%"                                              # p.2. :contentReference[oaicite:40]{index=40}

group_project_details:                         # Criteria on p.4. :contentReference[oaicite:41]{index=41}
  presentation_time: "5 minutes"
  evaluation_criteria:
    - "Theoretical rigor (20%)"
    - "Complexity of control application (15%)"
    - "Documentation and presentation (25%)"
    - "Results and final implementation (40%)"
    - "Peer voting (optional 10–20%, with instructor veto for fairness)"

topics:                                         # Weekly outline on p.3. :contentReference[oaicite:42]{index=42}
  - "Wk1: Introduction"
  - "Wk2–3: Modeling in Frequency Domain (Lab L1)"
  - "Wk4: Modeling in Time Domain"
  - "Wk5: Time Response (Lab L2)"
  - "Wk6: Reduction of Multiple Sub-systems; Quiz 1"
  - "Wk7: Stability (Lab L3)"
  - "Wk8: Steady-State Error; Quiz 2; Final Project Proposal due"
  - "Wk9: Root Locus and Design (Lab L4)"
  - "Wk10: Frequency Response and Design; Quiz 3"
  - "Wk11: Design with State Space (Lab L5)"
  - "Wk12: Digital Control; Quiz 4"
  - "Wk13: N/A (no meetings listed)"
  - "Wk14: Learning-based Control (Optional)"
  - "Wk15–16: Final Project Presentations (5 min each)"
  - "Wk17: Final Exam"

policies_summary:
  platform: "Blackboard Learn for syllabus and materials; monitor portal and public course page." # p.1. :contentReference[oaicite:43]{index=43}
  late_homework: "Accepted with penalties; details announced with fair notice."                    # p.2. :contentReference[oaicite:44]{index=44}
  academic_integrity: "Follow CSU Chico Academic Integrity Policy; violations reported to Office of Student Conduct." # p.4. :contentReference[oaicite:45]{index=45}
  classroom_protocol: "Stay on task; avoid unrelated online activity during class."               # p.4. :contentReference[oaicite:46]{index=46}
  accessibility: "Coordinate accommodations with Accessibility Resource Center (ARC)."            # pp.4–5. :contentReference[oaicite:47]{index=47}
  student_support: "Student Learning Center provides tutoring and study support."                 # p.5. :contentReference[oaicite:48]{index=48}

syllabus_pdf: /files/meca_482_syllabus.pdf     # Replace with your site path to the uploaded PDF.

---

{% include teaching-pdfs.html %}

An applied course in classical control with a bridge to modern methods. Topics include modeling in time and frequency domains, stability analysis, steady‑state error, and controller design via root locus and frequency response, with introductions to state‑space and digital control. Laboratory exercises and a team project connect theory to practice.
