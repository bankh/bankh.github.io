---
title: "MECA 470 — Robotics Engineering"                  # Course title on p.1. :contentReference[oaicite:0]{index=0}
collection: teaching
type: "Undergraduate course"                               # 400-level course; fits undergrad catalog.
venue: "California State University, Chico"                # Header on p.1. :contentReference[oaicite:1]{index=1}
institution: "California State University, Chico"          # Header on p.1. :contentReference[oaicite:2]{index=2}
course_code: "MECA 470"                                    # p.1. :contentReference[oaicite:3]{index=3}
term: "Fall 2020"                                          # p.1 footer/header. :contentReference[oaicite:4]{index=4}
level: "undergraduate"                                     # Inferred from numbering.
status: "archived"                                         # Course ran in 2020.
date: 2020-08-24                                           # Week 1 is Aug 24–29. :contentReference[oaicite:5]{index=5}
permalink: /teaching/2020-meca470-robotics
tags: [robotics, ROS, kinematics, motion-planning, control, manipulation, wheeled-mobile-robots, vision, PoE, Jacobian, RRT, PRM, A*, MoveIt, DexNet, RoboDK, CoppeliaSim, Gazebo, AWS-RoboMaker] # Topics and tools on pp.1,4–7 and flyer. :contentReference[oaicite:6]{index=6} :contentReference[oaicite:7]{index=7}
featured: false
role: "Instructor"
years: "2020"
pdfs:
  - label: "Syllabus"
    url: "/files/MECA_470_syllabus.pdf"
  - label: "Course Flyer"
    url: "/files/MECA_470_flyer.pdf"

excerpt: "Robotics foundations: motion, kinematics, planning, control, manipulation, and mobile robots. ROS with RoboDK, CoppeliaSim, Gazebo. Team project and labs." # Scope and tools pp.1,4–7; flyer. :contentReference[oaicite:8]{index=8} :contentReference[oaicite:9]{index=9}
short_description: "Deep and rigorous course in robotics. SE(3) kinematics, PoE, Jacobians, planning with A*/PRM/RRT, contact mechanics, and software-driven labs using ROS and simulators." # Sections and outcomes pp.1,5–7. :contentReference[oaicite:10]{index=10}

instructor:
  name: "H. Sinan Bank"                                    # Flyer contact. :contentReference[oaicite:11]{index=11}
  email: "hsbank@mail.csuchico.edu"                        # Flyer contact. :contentReference[oaicite:12]{index=12}

sections:                                                  # Meeting pattern from flyer. :contentReference[oaicite:13]{index=13}
  - type: "Lecture"
    schedule: "TR 1:00–1:50 pm"
  - type: "Activity"
    schedule: "F 2:00–3:50 pm"
course_enrollment_number: "5725"                           # Flyer. :contentReference[oaicite:14]{index=14}

learning_outcomes:                                         # Detailed outcomes per module, pp.4–7. :contentReference[oaicite:15]{index=15}
  - "Explain software and hardware architecture concepts in robotics." # p.4. :contentReference[oaicite:16]{index=16}
  - "Compute degrees of freedom; apply Gruebler’s formula; identify joint constraints." # p.4. :contentReference[oaicite:17]{index=17}
  - "Express joint axes as screw axes in {s} or {b}; apply the PoE formula for forward kinematics in SE(3)." # p.5. :contentReference[oaicite:18]{index=18}
  - "Derive configuration‑dependent Jacobians; analyze singularities and manipulability." # p.5. :contentReference[oaicite:19]{index=19}
  - "Relate end‑effector wrenches and joint torques; use force and manipulability ellipsoids." # p.5. :contentReference[oaicite:20]{index=20}
  - "Model C‑space obstacles; represent free C‑space as graphs or trees; implement A*, PRM, and RRT." # p.6. :contentReference[oaicite:21]{index=21}
  - "Use grid maps and potential fields for motion planning and real‑time control among obstacles." # p.6. :contentReference[oaicite:22]{index=22}
  - "Analyze contact modes; test form and force closure; use friction cones and wrench spaces." # p.7. :contentReference[oaicite:23]{index=23}
  - "Perform contact kinematics and force analysis for rigid bodies with frictional contacts." # p.7. :contentReference[oaicite:24]{index=24}

prerequisites:                                             # Flyer prerequisites/co-req. :contentReference[oaicite:25]{index=25}
  required_or_coreq:
    - "CSCI 111 or MECH 208"
    - "MECH 320 (co‑requisite)"

texts:
  required:
    - "Lynch, Kevin M., and Frank C. Park. *Modern Robotics*, 2nd ed. Free pre‑print accepted." # p.1. :contentReference[oaicite:26]{index=26}
    - "O’Kane, Jason M. *A Gentle Introduction to ROS*. Free digital accepted."                  # p.1. :contentReference[oaicite:27]{index=27}

software_and_tools:                                        # Syllabus and flyer tools. :contentReference[oaicite:28]{index=28} :contentReference[oaicite:29]{index=29}
  items:
    - "ROS (Robot Operating System)"
    - "Gazebo"
    - "CoppeliaSim"
    - "RoboDK"
    - "AWS RoboMaker"
    - "Python and C/C++"
  notes:
    - "Use native Linux when possible; Linux VMs or AWS RoboMaker are options." # Flyer guidance. :contentReference[oaicite:30]{index=30}
    - "Course does not require hardware; no credit for doing hardware builds."   # p.1. :contentReference[oaicite:31]{index=31}

assessments:                                               # Pulled from 'Weightings, Grading, and Rubric' and overview. :contentReference[oaicite:32]{index=32}
  exams:
    modules: 4                                             # “4 Exam Modules: 3 Exams + 1 Final.” p.1. :contentReference[oaicite:33]{index=33}
    regular_exams_weight: "15%"                            # “15% Exams x 3.” p.2 graphic. :contentReference[oaicite:34]{index=34}
    final_exam_weight: "20%"                               # “20% Exam x 4.” p.2 graphic. :contentReference[oaicite:35]{index=35}
  homework:
    count: 6
    weight: "15%"                                          # p.2 graphic. :contentReference[oaicite:36]{index=36}
  exercises:
    count: 8
    weight: "20%"                                          # p.2 graphic. :contentReference[oaicite:37]{index=37}
  labs:
    count: 10
    weight_note: "Shown in grading graphic; see syllabus figure." # p.2 graphic shows Labs x10. :contentReference[oaicite:38]{index=38}
  project:
    count: 1
    milestones: ["W1 topic selection", "W2 team setup", "approval", "deliver milestones"] # p.2 project lane. :contentReference[oaicite:39]{index=39}
  participation:
    weight: "10%"                                          # p.2 graphic. :contentReference[oaicite:40]{index=40}
  extra_credit:
    range: "5–10% possible"                                # “Excluding 5–10% extra credits.” p.2. :contentReference[oaicite:41]{index=41}

topics:                                                     # Section list and flyer topics. :contentReference[oaicite:42]{index=42} :contentReference[oaicite:43]{index=43}
  - "Section 1: Foundations of robot motion—C‑spaces, freedoms/constraints, linear algebra lab."
  - "Section 2: Robot kinematics—PoE, Jacobians, singularities, manipulability."
  - "Section 3: Motion planning and control—graphs/trees, A*, PRM, RRT, grid maps, potential fields."
  - "Section 4: Manipulation and wheeled robots—contact modes, form/force closure, friction cones."
  - "ROS stack essentials—navigation (SLAM), MoveIt manipulation, perception (e.g., DexNet)."
  - "Python programming and interfacing with digital twins in RoboDK and CoppeliaSim."

schedule_highlights:                                       # From the module table on p.4. :contentReference[oaicite:44]{index=44}
  - "Week 1 (Aug 24–29): Linear algebra review; software install; reading preview; due 08/30/20."
  - "Week 2: ROS setup; Lab—RoboDK robot types and frames."
  - "Week 3: Videos and Chapter 3; assignment due Sep 20."
  - "Week 4: CoppeliaSim; Lab—apply linear algebra with Python on RoboDK/CoppeliaSim."

policies_summary:
  blackboard: "Software details, assignments, and materials are organized in Blackboard." # p.1. :contentReference[oaicite:45]{index=45}
  late_work: "Late assignments accepted with penalty; one‑week delay may reduce to zero." # p.4. :contentReference[oaicite:46]{index=46}
  academic_integrity: "Follow CSU Chico Academic Integrity policy; violations reported."  # p.8. :contentReference[oaicite:47]{index=47}
  add_drop: "Follow University add/drop rules and deadlines."                             # p.8. :contentReference[oaicite:48]{index=48}
  accessibility: "Coordinate accommodations with the Accessibility Resource Center (ARC)." # p.8. :contentReference[oaicite:49]{index=49}
  student_support: "Student Learning Center resources available."                         # p.8. :contentReference[oaicite:50]{index=50}

syllabus_pdf: /files/meca470-robotics-fall2020.pdf         # Source: Fall 2020 PDF. :contentReference[oaicite:51]{index=51}
course_flyer_pdf: /files/meca470-technical-elective-flyer.pdf # Source: flyer. :contentReference[oaicite:52]{index=52}

# header:
#   image: /images/teaching/meca470/hero.jpg                 # Optional hero image.
# cover_alt: "Industrial robot arm with simulated path and sensors"
---

{% include teaching-pdfs.html %}

A rigorous robotics course. You study motion, kinematics, planning, and manipulation. You implement algorithms with ROS and simulators and work in teams. Assessments include three exams, a final, homework, exercises, labs, and a project with milestones. The outline and tooling follow the Fall 2020 syllabus and the course flyer.


