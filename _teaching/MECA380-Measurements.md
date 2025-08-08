---
title: "MECA 380 — Measurements and Instrumentation" # Title on p.1. :contentReference[oaicite:0]{index=0}
collection: teaching
type: "Undergraduate course"                          # 300-level; undergrad.
venue: "California State University, Chico"           # Header on p.1. :contentReference[oaicite:1]{index=1}
institution: "California State University, Chico"     # p.1. :contentReference[oaicite:2]{index=2}
course_code: "MECA 380"                               # p.1. :contentReference[oaicite:3]{index=3}
course_number: 380
term: "Fall 2021"                                     # p.1. :contentReference[oaicite:4]{index=4}
level: "undergraduate"
status: "archived"
date: 2021-08-23
permalink: /teaching/2021-meca380-measurements
tags: [measurements, instrumentation, LabVIEW, DAQ, sensors, transducers, signal-conditioning, filtering, ADC, DAC, aliasing, spectral-analysis, uncertainty, calibration, noise, statistics] # Course description and core topics, pp.1–2. :contentReference[oaicite:5]{index=5}
featured: false
role: "Instructor"
years: "2021"

excerpt: "Measurement of steady-state and dynamic systems. Calibration, uncertainty, statistics, LabVIEW-based data acquisition, signal conditioning, frequency-domain analysis, and noise mitigation." # Description and goals, p.1; core topics, p.2. :contentReference[oaicite:6]{index=6}
short_description: "Hands-on labs with sensors and transducers, DAQ and LabVIEW, signal conditioning and filtering, sampling and aliasing, uncertainty, and technical reporting." # SLOs and core topics, pp.1–2. :contentReference[oaicite:7]{index=7}

modality: "in-person"                                  # Rooms listed for discussions and labs, p.1. :contentReference[oaicite:8]{index=8}

# Keep instructor info consistent with your other course pages.
instructor:
  name: "H. Sinan Bank"
  email: "hsbank@mail.csuchico.edu"
  phone: "530-898-4619"
  office: "OCNL 428"
  office_hours: "MW 2:00–4:00 pm; meetings via calendly.com/hsbank"

sections:                                               # Section times and rooms on p.1. :contentReference[oaicite:10]{index=10}
  - section: "01"
    type: "Discussion"
    schedule: "Mon, Fri 4:00–4:50 pm"
    location: "OCNL 254"
  - section: "02"
    type: "Laboratory"
    schedule: "Wed 5:00–7:50 pm"
    location: "PLMS 112"
  - section: "03"
    type: "Laboratory"
    schedule: "Thu 2:00–4:50 pm"
    location: "PLMS 112"

learning_outcomes:                                      # SLOs, pp.1–2. :contentReference[oaicite:11]{index=11}
  - "Measure resistance, temperature, acoustic, and strain signals with standard instruments and LabVIEW virtual instruments."
  - "Design and calibrate measurement systems with sensors, transducers, signal conditioning, DAQ, and output stages."
  - "Conduct experiments, mitigate noise and interference, apply statistics, analyze and interpret data."
  - "Apply signal conditioning: excitation, amplification/attenuation, buffering, filtering, linearization, and scaling."
  - "Evaluate signals in the frequency domain; choose sampling to avoid aliasing."
  - "Identify noise sources and apply mitigation strategies."
  - "Calculate instrument uncertainty; design to meet accuracy requirements."
  - "Prepare technical reports and instrument specification sheets."

core_topics:                                            # Core knowledge list, p.2. :contentReference[oaicite:12]{index=12}
  - "Measurement concepts and instruments"
  - "Sensor characteristics and calibration"
  - "Experiment design"
  - "Temperature measurement"
  - "LabVIEW fundamentals"
  - "Probability, statistics, regression, and correlation"
  - "First- and second-order system characterization"
  - "Electrical measurements and lab instrumentation"
  - "Signal conditioning and filtering"
  - "Scaling and linearization"
  - "Frequency domain and spectral analysis"
  - "Aliasing and sampling"
  - "ADC and DAC"
  - "Strain measurement"
  - "Electrical noise sources and mitigation"
  - "Instrument uncertainty"

prerequisites:                                          # p.1. :contentReference[oaicite:13]{index=13}
  required:
    - "EECE 211/211L"
  one_of:
    - "CSCI 111"
    - "MECH 208"
    - "AMAR 300"

texts:
  required:
    - "Figliola, R. S., and D. E. Beasley. *Theory and Design for Mechanical Measurements*, 7th ed., Wiley, 2019. 5th and 6th acceptable." # p.4. :contentReference[oaicite:14]{index=14}
  optional:
    - "Beckwith, T. G., R. D. Marangoni, and J. H. Lienhard. *Mechanical Measurements*, 6th ed., Pearson, 2019." # p.4. :contentReference[oaicite:15]{index=15}
    - "Travis, J., and J. Kring. *LabVIEW for Everyone*, 3rd ed., Prentice Hall, 2006." # p.4. :contentReference[oaicite:16]{index=16}
    - "Scherz, P., and S. Monk. *Practical Electronics for Inventors*, 4th ed., McGraw‑Hill, 2016." # p.4. :contentReference[oaicite:17]{index=17}

software_and_equipment:
  required:
    - "PC laptop capable of running NI ELVISmx 2019; license provided for the course." # p.4. :contentReference[oaicite:18]{index=18}
    - "LabVIEW (NI ELVISmx 2019)"                 # p.4. :contentReference[oaicite:19]{index=19}
  recommended:
    - "MATLAB and/or Excel"                       # p.4. :contentReference[oaicite:20]{index=20}
  materials:
    - "Bound lab notebook, turned in at end of course." # p.3. :contentReference[oaicite:21]{index=21}

assessments:                                            # Grading policy and scales, p.3. :contentReference[oaicite:22]{index=22}
  without_final_project:
    participation_quizzes: "20%"
    lab_reports_and_assignments: "40%"
    exams_curved: "40%"
    grade_cap: "B+ maximum if no Final Project"
    scale: "B+ ≥ 87% > B ≥ 83% > B‑ ≥ 80% > C+ ≥ 77% > C ≥ 73% > C‑ ≥ 70% > D ≥ 60% > F"
  with_final_project:
    participation_quizzes: "15%"
    lab_reports_and_assignments: "30%"
    exams_curved: "30%"
    final_project: "25%"
    scale: "A ≥ 93% > A‑ ≥ 90% > B+ ≥ 87% > B ≥ 83% > B‑ ≥ 80% > C+ ≥ 77% > C ≥ 73% > C‑ ≥ 70% > D ≥ 60% > F"
  late_policy: "−20% of full credit per day late; submit a cover letter via Blackboard for consideration at term end." # p.3. :contentReference[oaicite:23]{index=23}
  quizzes_note: "Pop quizzes may be given based on assigned readings." # p.3. :contentReference[oaicite:24]{index=24}

policies_summary:
  blackboard_onenote: "Syllabus, assignments, schedule on Blackboard; class notes via OneNote Class Notebook." # p.2. :contentReference[oaicite:25]{index=25}
  attendance: "Active participation expected during all sessions." # p.2. :contentReference[oaicite:26]{index=26}
  academic_integrity: "Follow CSU Chico Academic Integrity policy; violations reported." # p.5. :contentReference[oaicite:27]{index=27}
  accessibility: "Coordinate accommodations with the Accessibility Resource Center (ARC)." # p.5. :contentReference[oaicite:28]{index=28}
  student_support: "IT Support Services and the Student Learning Center available." # pp.5–6. :contentReference[oaicite:29]{index=29}
  covid_safety_fall2021: "Vaccination deadline and indoor face coverings required at that time." # p.4. :contentReference[oaicite:30]{index=30}

topics:                                                 # Condensed from core topics, p.2. :contentReference[oaicite:31]{index=31}
  - "Measurement systems and calibration"
  - "Sensors and transducers"
  - "Signal conditioning and filtering"
  - "Sampling, aliasing, and ADC/DAC"
  - "Frequency‑domain analysis and spectral methods"
  - "Temperature and strain measurement"
  - "Noise and mitigation strategies"
  - "Uncertainty analysis"
  - "LabVIEW and virtual instrumentation"
  - "Technical reporting"

milestones:
  - "Optional Final Project used to integrate course outcomes." # p.3. :contentReference[oaicite:32]{index=32}

pdfs:
  - label: "Syllabus"
    url: ""
syllabus_pdf: 
---

{% include teaching-pdfs.html %}

A hands‑on course on measurement and instrumentation. You build and calibrate systems, analyze data in time and frequency, and manage uncertainty and noise. Labs use LabVIEW and DAQ hardware. Grading offers two paths, with or without a Final Project.


