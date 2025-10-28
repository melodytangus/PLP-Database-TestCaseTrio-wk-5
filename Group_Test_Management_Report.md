🧪 Final Group Test Report Template — Word Puzzle Game Plus

Level: Intermediate QA | Week 5: Test Management

Course: Software Testing & Quality Assurance
Module: Test Management (Week 5)
Project Type: Group Assessment
Submission Date: 2025-10-28

Team Information
Role	        Name	                  Responsibilities
Test Manager	Mercy Melody Chemutai	  Planning, scheduling, coordination, metric tracking
Risk Analyst	Lorraine Bwayo         	Risk identification, prioritization, test design linkage
Test Executor	Susan Mwangi	          Execution, evidence capture, defect logging

Group Rules
Each student must belong to only one group.
Duplicate membership or multiple submissions will result in invalidation.
Every group member must contribute towards this project.

Project Overview

System Under Test: Word Puzzle Game Plus
Technology Stack: HTML, CSS, JavaScript
Environment: Chrome Browser (Desktop)

Features Under Test
Feature	Description	Risk Category
Reset Game	Clears score and progress instantly	State Management / Functional
Leaderboard	Stores top 3 scores in localStorage	Data Persistence / Functional
Bonus Round	Every 3 puzzles → doubles score	Business Logic / Functional

Test Plan
Objectives
Verify correct calculation and triggering of the Bonus Round feature.
Validate Leaderboard data persistence and sorting logic.
Confirm Reset Game clears only session data (not leaderboard).
Ensure no regressions in core game logic (hint usage, scoring).

Scope

In Scope:
Functional and logical testing of the 3 new features.
Data integrity testing of localStorage.
Negative testing (invalid or empty inputs).
Basic usability and UI feedback checks.
Regression testing of hint and score logic.

Out of Scope:
Cross-browser testing (limited to Chrome).
Performance or load testing.
Security or accessibility testing.
Tools & Resources
GitHub – Version control, issue tracking, and Kanban board.
Google Chrome – Primary test environment.
Chrome DevTools – For console logs and localStorage inspection.

Schedule
Phase	Planned Duration	Actual Duration	Status
P1: Planning & Setup	1 Day	1 Day	✅ Completed
P2: Risk Analysis & Test Design	2 Days	2 Days	✅ Completed
P3: Test Execution & Defect Logging	2 Days	2 Days	✅ Completed
P4: Reporting & Closure	1 Day	1 Day	✅ Completed
Risk Analysis
Risks
ID	Feature	Risk Description	Likelihood	Impact	Priority	Mitigation Strategy
R-01	Bonus Round	Calculation may trigger incorrectly or double wrong score	3	5	15 (High)	Create test cases for puzzles 2–6 to confirm timing
R-02	Leaderboard	Data fails to save, sorts incorrectly, or loses persistence	4	5	20 (Critical)	Test multiple score inputs and refreshes
R-03	Reset Game	Reset may clear leaderboard instead of session data	2	4	8 (Medium)	Verify localStorage contents remain after reset
R-04	Hint Logic	Hint flag or deduction not reset properly	3	3	9 (Medium)	Regression test after each new puzzle
R-05	Usability	Player confusion about bonus round or hint cost	3	2	6 (Low)	Test clarity of on-screen instructions
R-06	Leaderboard	Game crash when localStorage disabled	2	4	8 (Medium)	Test with storage disabled manually

Risk Coverage
Tested Risks Percent: 100%
Untested Risks Percent: 0%

Test Cases
ID	Feature	Objective	Expected Result	Actual Result	Status	Risk Link
TC-01	Leaderboard	Verify top-3 sorting and persistence	Board shows scores [12, 8, 5] after refresh	Works correctly	✅ PASS	R-02
TC-02	Bonus Round	Verify bonus triggers on 3rd puzzle	Score doubles and “Bonus Round!” appears	Works correctly	✅ PASS	R-01
TC-04	Reset Game	Verify reset clears progress but not leaderboard	Score reset; leaderboard unchanged	Puzzle area turns blank after reset	❌ FAIL	R-03
TC-05	Hint Logic	Verify hint reset between puzzles	Hint resets and applies cost properly	Works correctly	✅ PASS	R-04
TC-06	Guess Input	Verify empty input	Message “Please enter a guess!” appears	Works correctly	✅ PASS	-
TC-07	Usability	Verify bonus message clarity	Message visible long enough to read	Disappears too quickly (~1.2s)	❌ FAIL	R-05
TC-08	Leaderboard	Verify disabled localStorage behavior	Game runs; leaderboard doesn’t update	Works correctly, no crash	✅ PASS	R-06
TC-09	Scoring	Verify score integrity on rapid-submit	Score should increment once	Score increments 3 times	❌ FAIL	-

Defects
ID	Issue Title	Severity	Risk ID	Status	GitHub Link
BUG-001	Reset button fails to load new puzzle, leaving blank screen	Medium	R-03 https://github.com/melodytangus/PLP-Database-TestCaseTrio-wk-5/issues/1
BUG-002	Clicking submit after reset shows “please enter a guess” error	Medium	R-03 https://github.com/melodytangus/PLP-Database-TestCaseTrio-wk-5/issues/2
BUG-003	Game is an endless loop with no clear start or finish button	Low	R-05 https://github.com/melodytangus/PLP-Database-TestCaseTrio-wk-5/issues/3

Metrics
Test Case Pass Percent: 6/8 = 75%
Defect Density: 3 Defects / 8 TCs = 0.375
Risk Coverage: 100% (6/6 Risks Tested)
Regression Success Rate: 100% (1/1 Regression TC Passed)

Defect Summary
Total Defects Logged: 3
Critical/High: 0
Medium: 2
Low: 1

Fix Rate: 0% (All defects currently open)

Test Control & Project Management
Phases
Phase	Deliverable	Actual Output	Variance	Owner
Test Execution	All test cases executed; defects logged	8/8 executed, 3 failed	3 failed TCs (TC-04, TC-07, TC-09)	Susan Mwangi
Test Closure	Final report and metrics	Completed	Build not ready for release	Mercy Melody Chemutai

Progress Tracking Method:
Used a GitHub Project (Kanban board) with To Do, In Progress, and Done columns. Daily 15-minute stand-ups were held for updates.

Change Control Notes:
No changes to project scope or resources during the cycle.

Lessons Learned
Most Defect-Prone Feature: Reset and game state management.
Risk Analysis Impact: Accurate — led to early detection of logic defects.
Team Communication: Excellent; GitHub Issues centralized all defects.

Improvements for Next Cycle:
Fix BUG-001 and BUG-002 to ensure the game never enters a blank state.
Add a “Game Over” or “Main Menu” screen to fix BUG-003.
Introduce peer reviews for test cases before execution.

Attachments
Evidence for BUG-001/002: Screenshot showing blank state after reset.
Evidence for TC-06: Screenshot of “Please enter a guess!” message (Passing Test).

Sign Off

Name	                    Role	    Initials	Date
Mercy Melody Chemutai	Test Manager	M.M.C.	2025-10-

Lorraine Bwayo	      Risk Analyst  L.B.	2025-10-28

Susan Mwangi	        Test Executor	S.M.	2025-10-28

Overall Summary
Statement:
The test cycle is complete, but the build is not approved for release. Execution revealed 3 defects — two medium-severity issues (BUG-001, BUG-002) that disrupt the game loop. All defects remain open and require regression testing after fixes.
Test Status: ✅ Completed
