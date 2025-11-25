# Project Presentation Guide

Use this guide to run your demonstration smoothly in front of your teacher.

## 1. Preparation (Before the teacher arrives)
*   **Open your IDE** (VS Code) to the project folder.
*   **Open the Terminal** at the bottom.
*   **Clean up**: Delete old `.png` files so new ones are generated fresh during the demo.
    ```bash
    del *.png
    ```
*   **Open these files** in tabs so you can quickly show code if asked:
    *   `noc_simulator.py` (The core logic)
    *   `fttm_mapper.py` (The smart algorithm)
    *   `Semester_Project_Report.md` (Your report)

## 2. The Pitch (1 Minute)
*"Sir/Ma'am, for my semester project, I implemented a **Fault-Tolerant Network-on-Chip (NoC)** system based on a research paper. As chips get smaller, cores fail more often. My system detects these faults and automatically moves tasks to the best available spare core to keep the processor running while saving energy."*

## 3. The Live Demo (Step-by-Step)

### Step 1: Show Basic Fault Recovery
**Command**:
```bash
python main.py
```
**What to say**:
*"First, I'll show a basic scenario on a 4x4 grid. Here, the system maps 12 tasks. Then, I inject a permanent fault."*
**Show**: Open the generated images `Initial_Mapping_...png` and `Post-Fault_Mapping_...png`.
*"As you can see, the task on the red faulty core was automatically moved to a green spare core."*

### Step 2: Show Robustness (Stress Test)
**Command**:
```bash
python stress_test.py
```
**What to say**:
*"Now, let's stress the system. I will inject multiple faults one after another to see if the system breaks."*
**Show**: The terminal output showing "Injecting Fault #1... #2... #3".
*"The system successfully recovers from every fault, remapping tasks dynamically."*

### Step 3: Show Efficiency (The "A" Grade Feature)
**Command**:
```bash
python comparison.py
```
**What to say**:
*"The most important part of the research paper is energy efficiency. I wrote a script to compare my algorithm against a standard random mapping."*
**Show**: The `Comparison_FTTM_vs_Random.png` bar chart.
*"My algorithm achieves about **15-20% energy savings** because it intelligently picks spare cores that are close to the task's communication partners."*

### Step 4: Verification (Optional/Bonus)
**Command**:
```bash
python test_suite.py
```
**What to say**:
*"To ensure code quality, I also wrote a unit test suite that validates the entire logic."*

## 4. Potential Q&A

**Q: How do you calculate energy?**
**A**: *"I use the standard model from the paper: Communication Volume multiplied by Manhattan Distance (number of hops)."*

**Q: What happens if there are no spare cores left?**
**A**: *"Currently, the system logs a critical error. In a real OS, this would trigger a process kill or a system-level alert."*

**Q: Why did you choose Python?**
**A**: *"Python allows for rapid prototyping of the high-level mapping algorithms, which was the focus of this research project."*
