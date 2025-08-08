---
title: "SMFG 386 — Manufacturing Automation Systems"       # Course title on p.1. :contentReference[oaicite:0]{index=0}
collection: teaching
type: "Undergraduate course"                                # Inferred from 300-level numbering; adjust if needed.
venue: "California State University, Chico"                 # Header on p.1. :contentReference[oaicite:1]{index=1}
institution: "California State University, Chico"           # Header on p.1. :contentReference[oaicite:2]{index=2}
course_code: "SMFG 386"                                     # p.1. :contentReference[oaicite:3]{index=3}
course_number: 386
term: "Spring 2020"                                         # p.1. :contentReference[oaicite:4]{index=4}
level: "undergraduate"                                      # Inferred.
status: "archived"                                          # Course ran in 2020; set archived for current list.
date: 2020-01-01                                            # For sorting
permalink: /teaching/2020-smfg386-automation
tags: [automation, CAD, CAM, NC, PLC, microcontrollers, sensors, actuators, ADC, DAC, robotics, AGV, FMS, CIM, computer-vision, scheduling] # Course description and units of study, pp.1–2. :contentReference[oaicite:5]{index=5}
featured: false
role: "Instructor"
years: "2020"
pdfs:
  - label: "Syllabus"
    url: "/files/SMFG_386_syllabus.pdf"

excerpt: "Automation and manufacturing systems: CAD/CAM, NC, PLCs, robotics, AGVs, FMS, CIM, and vision; labs and a team project." # Course description, p.1. :contentReference[oaicite:6]{index=6}
short_description: "Design and control of automated production systems. Sensors and actuators, PLCs and microcontrollers, robotics, NC/CAM, FMS/CIM, and perception." # pp.1–2. :contentReference[oaicite:7]{index=7}

modality: "online"                                          # Class locations marked Online for both sections, p.1. :contentReference[oaicite:8]{index=8}

instructor:
  name: "H. Sinan Bank"                                     # p.1. :contentReference[oaicite:9]{index=9}
  email: "hsbank@mail.csuchico.edu"                         # p.1. :contentReference[oaicite:10]{index=10}
  phone: "530-898-4619"                                     # p.1. :contentReference[oaicite:11]{index=11}
  office: "Zoom"                                            # p.1. :contentReference[oaicite:12]{index=12}
  office_hours: "MW 12:00–2:00 pm"                          # p.1. :contentReference[oaicite:13]{index=13}

sections:                                                   # Class times and locations, p.1. :contentReference[oaicite:14]{index=14}
  - section: "01 (3236)"
    schedule: "MWF 10:00–10:50 am"
    location: "Online"
  - section: "02 (3237)"
    schedule: "Thu 5:00–7:50 pm"
    location: "Online"

learning_outcomes:                                          # Student Learning Outcomes, p.1. :contentReference[oaicite:15]{index=15}
  - "Explain reasons to employ automation and cite typical applications."
  - "Describe sensor and actuator functions in automated systems."
  - "Select suitable sensors and actuators for given tasks."
  - "Describe fundamentals of NC technology."
  - "Use a PLC and an embedded microcontroller for specified control functions."
  - "Describe the anatomy and attributes of robotic systems."
  - "Identify components and interfaces in flexible manufacturing systems."
  - "Troubleshoot systems and take appropriate corrective actions."
  - "Design an automated system to meet operational specifications."
  - "Research and summarize a technology or application in automation or robotics."

prerequisites:
  - "PHYS 202"                                              # p.1. :contentReference[oaicite:16]{index=16}
  - "SMFG 360"                                              # p.1. :contentReference[oaicite:17]{index=17}

texts:
  required:
    - "Groover, Mikell P. *Automation, Production Systems, and Computer-Integrated Manufacturing*, 5th ed., Pearson, 2019. (eBook acceptable.)" # p.2. :contentReference[oaicite:18]{index=18}
  suggested:                                                # p.2. :contentReference[oaicite:19]{index=19}
    - "Hanssen, Dag H. *Programmable Logic Controllers: A Practical Approach to IEC 61131-3 Using CoDeSys*, 2015."
    - "Scherz, Paul, and Simon Monk. *Practical Electronics for Inventors*, 2013."
    - "Çetinkunt, Sabri. *Mechatronics with Experiments*, 2015."

software:                                                   # Required software list, p.2. :contentReference[oaicite:20]{index=20}
  - "Windows 10 PC"
  - "Python 3.6 with Visual Studio Code"
  - "MATLAB (with required toolboxes such as System Composer noted in Blackboard)"
  - "CoppeliaSim for physics-based simulation"
  - "CoDeSys 3.5 (IEC 61131-3 PLC programming)"
  - "SimulIDE for microcontroller simulation"
  - "Rhino with Grasshopper (trial okay)"
  - "Omron Learning portal registration"
software_notes:
  - "Virtual machines are problematic on macOS; use a Windows 10 PC." # p.2. :contentReference[oaicite:21]{index=21}
  - "Instructor does not assist with software installation; delays incur penalties." # p.2. :contentReference[oaicite:22]{index=22}

lab_hardware: "In‑class labs use simple physical systems to tie theory to practice." # p.3. :contentReference[oaicite:23]{index=23}

assessments:                                               # Weights on p.3. :contentReference[oaicite:24]{index=24}
  labs:
    weight: "15%"
  exams:
    weight: "15%"
  homeworks:
    weight: "15%"
  group_project:
    weight: "15%"
  final_exam:
    weight: "30%"
  participation:
    weight: "10%"
  notes:
    - "Exams are online, typically Fri evening to Sun midnight; 48+ hours to submit; late uploads not accepted." # p.3. :contentReference[oaicite:25]{index=25}
    - "Participation reflects intellectual contribution; attendance alone does not determine participation credit." # p.3. :contentReference[oaicite:26]{index=26}
    - "Late homework accepted with penalties; components may change with fair notice." # p.3. :contentReference[oaicite:27]{index=27}

group_project_details:                                     # Project criteria and logistics, p.5. :contentReference[oaicite:28]{index=28}
  team_size: 3
  deliverables:
    - "5‑minute presentation"
    - "Concise documentation following provided templates"
    - "Google spreadsheet entries for project description, team, and milestones"
  evaluation_criteria:
    - "Theoretical rigor (20%)"
    - "Complexity of application (15%)"
    - "Documentation and presentation (25%)"
    - "Results and final implementation (40%)"
    - "Peer voting (optional 10–20%, with instructor veto for fairness)"
  grading_floor_for_incomplete_projects: "60% of total (starting point for incomplete work)" # p.5. :contentReference[oaicite:29]{index=29}

topics:                                                     # Units of study, p.2; schedule table summarized from p.4. :contentReference[oaicite:30]{index=30}
  - "Section 1 — Production systems design and architecture: model‑based design; principles of automation; manufacturing operations."
  - "Section 2 — Automation and control systems: intro to automation; industrial control; hardware (sensors, actuators, ADC/DAC)."
  - "Section 3 — Automation and process control: discrete control and PLCs; microcontrollers."
  - "Section 4 — Robotics and automated systems: robotics; NC technology."
  - "Section 5 — Planning and perception (time permitting): computer vision; single‑station and multi‑station cells; planning and scheduling."

milestones:                                                # From the Topics/Tentative Schedule table on p.4. :contentReference[oaicite:31]{index=31}
  - "Team and project proposal: Week 3."
  - "Exam 1: after Week 4."
  - "Final project proposal: Week 10."
  - "Exam 2: after Week 13."
  - "Final project delivery: Week 16."
  - "Final exam: Week 17."

policies_summary:
  blackboard: "Syllabus and materials on Blackboard Learn; access via Chico State Portal." # p.1. :contentReference[oaicite:32]{index=32}
  exams_window: "Online exams; Fri evening to Sun midnight; 48+ hours to submit; no late uploads." # p.3. :contentReference[oaicite:33]{index=33}
  email_and_drive: "Use student email for Google Drive submissions; ensure other Gmail accounts are logged out." # p.3. :contentReference[oaicite:34]{index=34}
  academic_integrity: "Follow CSU Chico Academic Integrity policy; violations reported to Student Conduct." # p.5. :contentReference[oaicite:35]{index=35}
  classroom_protocol: "Stay on task; avoid unrelated online activity during class." # p.5. :contentReference[oaicite:36]{index=36}
  accessibility: "Coordinate accommodations with Accessibility Resource Center (ARC)." # p.6. :contentReference[oaicite:37]{index=37}
  student_support: "Student Learning Center services available." # p.6. :contentReference[oaicite:38]{index=38}

syllabus_pdf: /files/smfg386-syllabus-spring2020.pdf       # Source file is the Spring 2020 PDF. :contentReference[oaicite:39]{index=39}

# header:
#   image: /images/teaching/smfg386/hero.jpg                 # Optional hero image.
# cover_alt: "Automated manufacturing cell with robot, conveyor, and PLC I/O"
---

{% include teaching-pdfs.html %}

An applied course in manufacturing automation. You study production systems and architecture, control hardware, PLCs and microcontrollers, robotics, NC/CAM, cells and FMS/CIM, and computer vision. Labs and a team project tie theory to practice. The outline, grading, software, and policies follow the Spring 2020 syllabus.


