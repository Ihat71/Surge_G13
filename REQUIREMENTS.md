# REQUIREMENTS.md

## Table of Contents
- [Requirement Elicitation](#requirement_elicitation)
- [Requirement Classification](#requirement_classification)
- [Structured Specification](#structured_specification)
- [Requirements Prioritization](#project_requirements_prioritization)

# Requirement Elicitation
**Chosen elicitation techniques:** Brainstorming and Interviewing
## Elicitation Documentation
### Brainstorming Session 

### Interviews With Surgeons 

## Raw Requirements List
**Services:**
- The robotic arms must have the capability of being precise to less than 0.5mm
- The area of surgery must be displayed in the operating room
- There must be a safe emergency stop system that is instant
- Surge must have 3 arms, a base, a computer, a controller, displays and a co-pilot seat
- The camera must have x-y-z movement and can be fastened in position
- The joints of Surge must have gold standard brushless stepper motors
- Surge must have all the tools required for surgery
- Surge must be able to cycle between the different tools
- The controller of the arms should be in a way similar to the structure of the arm, with pinchers at the top that would permit the arm to do its action
- The controller must have gold standard encoders
- Surge should be fastened to a rail system that allows it to move around the surgery bed
- The surgeon must have a display in which he can see through the lens of the camera
- The surgeon must have a pedal system that he can zoom in and out of the camera
- The surgeon must have a scroll wheel to control the rail
- Both the surgeon and assistant surgeon need an emergency stop button
- The assistant surgeon must have a controller to set up the position of the camera
- The software must provide useful analytics of estimated blood loss, estimated size of the region of surgery and etc
- The software must have intuitive GUI that allows the user to do the primary tasks within 3-4 clicks or less
- The delay of the system must not go beyond 500ms and should be below 250ms optimally
- The system should deploy control systems that can self correct Surge
- The system should support remote trouble shooting
- The system should support remote surgeries
- Surge should be lightweight
- The cabling/networking of the system should be controlled
- Surge must be shock resistant
- Surge must be able to handle being regularly sanitized
- The system must be cost efficient and each Surge unit should not exceed 500k in costs
- Surge must be relatively mobile and small sized
  
**Constraints:**
- Must be secure
- Must have privacy: footage of the surgery must never be released or used without consent or necessity
- The system must conform to the medical standards around the world

# Requirements Classification
## User Requirements
## System Requirements
### Functional Requirements
### Non-Functional Requirements


# Structured Specification
## Functional Requirement 1: Precise Control of Robotic Arms
**Requirement ID:** FR-01

**Description:**
The robot must move its arms very accurately and respond quickly to the surgeon’s controls.

**Rationale:**
Precise movement is important so that the robot does not harm the patient and follows the surgeon’s exact actions.
- Commands from the surgeon’s controller.
- Data from sensors that track how the arms move.
- Smooth and accurate arm movement in real time.
- The robot must be fully checked and calibrated before the surgery.
- The arms should be in their correct starting position.
- There are no delays or sudden movements.
  
**Criticality:**
High mistakes in arm movement could be dangerous for the patient.

## Functional Requirement 2: Real Time Visual Display
**Requirement ID:** FR-02

**Description:**
The robot must show a live video of the surgery area so the surgeon can clearly see what is happening.

**Rationale:**
Good video helps the surgeon make better decisions and avoid errors during surgery.
- Video from the cameras on the robot.
- Lighting and zoom settings chosen by the surgeon.
- A clear and steady video feed on the surgeon’s screen.
- The ability to zoom in, rotate, or change the camera view easily.
- Cameras and lights must be working correctly before the surgery.
- The video has little to no delay
- The picture stays clear and smooth the whole time.
 
**Criticality:**
High poor video could make the operation unsafe.

## Functional Requirement 3: Emergency Stop System
**Requirement ID:** FR-03

**Description:**
The robot must have a safety system that can stop all movement right away if something goes wrong or if the surgeon presses the emergency stop.

**Rationale:**
This prevents accidents and keeps the patient and surgeon safe.
- A signal from the emergency stop button or voice command.
- Data from sensors that detect any problems, like too much force.
- An alarm sounds and flashes to warn the team.
- The robot is running and ready for surgery.
- Emergency systems must be checked and working.
- The robot stops safely and cuts power to its motors.
- It can only restart after the issue is fixed.
  
**Criticality:**
Very High this is the most important feature for safety.

# Project Requirements Prioritization
**Task:** prioritize all project requirements into 3 categories with reasoning:
- **Mandatory (M)** - Must be included for the project to function properly.
- **Nice To Have (N)** - Adds value, and desirable but not essential.
- **Superfluous (S)** - Extra and unnecessary for the project goal and feasibility.

## 1. Mandatory (M)

-The Robot must include an additional control for the camera to enable zoom in/out functionality.
*Reason:* to allow the Doctor to have full control over the camera.

-The camera should have a built-in light source.
*Reason:* To provide clear visibility of the area being operated on.

-The robot must include an emergency stop system.
*Reason:*in case something fails to work the robot will shutdown immediately.


## 2. Nice To Have (N)

-The robot shall provide an integrated Intraoperative Ultrasound that gives real-time information needed.
*Reason:* dangerous tumors can be hidden but with IOUS it can easily be visualized and identified.

-The robot shall support telecommunication features that enable remote telesurgery.
*Reason:* This allows top surgeons perform surgical operations from different locations with real-time control, as if physically present in the room.

-The control interface should be made with Anti-vibration materials to ensure maximum stability and precision.
*Reason:* This feature minimizes unwanted motion, making the robot as steady and accurate as possible, mainly useful for older surgeons with less steady hand control.


## 3.Superfluous (S)

-the robot shall analyze patient’s blood to determine safe / correct amount of anesthesia dosage.
*Reason:* Unnecessary, usually done by the anesthesiologists.

-the robot shall be able to store data for each patient who undergoes surgery.
*Reason:* increases complexity and requires an additional storage hardware and data management.

-The robot shall have a friendly, smiley appearance to make it look less scary for the patients.
*Reason:* completely extra, and its only for aesthetic.
