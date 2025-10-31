**SYSTEM:**  Surgical Robot System   
**Description:** this document describes the main actors and use cases needed for Surge's robot system   
**ACTORS:** Primary Surgeon, Assistant Surgeon, Tool Shifting System, Visual System, Control System, Security System   
**USE-CASES:**    

 1. ***UC1:*** Arm movements   
	 ***Actors:*** Primary Surgeon, Vision System   
	 ***Description:*** The robotic arms simulate the surgeons movements   
	 **Start:** Robot is turned on and on surgery mode   
	 ***Normal Flow:***   
			 1. Surgeon places fingers in controller   
			 2. Surgeon moves controller   
			 3. Controller sends data in the form of signals to control system   
			 4. Control system receives data   
			 5. The system processes and translates data into commands for the arm   
			 6. The arm mirrors the surgeons movements   
			 7. Sensors on the arm measure position, speed, angle, and electromagentism   
			 8. Arm sends feedback to control system   
			 9. Controller continuosly sends data   
			 10. Control system dynamically adjusts commands accordingly to maintain stability   
	***End:*** Robot continuosly moves to the desired position   
	***Alternatives:***    
		3. controller fails to send data, error message is displayed   
		4. control system fails to receive data, error message is displayed   
	   
 2. ***UC2:*** Changing camera angle   
 ***Actors:*** Assistant Surgeon, Camera System   
 ***Description:*** Changing the camera angle while operating surgery to view the necessary place without obstructions     
 ***Start:*** Surgery is underway, Robot is on, cameras are on, and Primary surgeon asks to change angle      
 ***Normal Flow:***     
		1. Assistant Surgeon is asked to change the camera angle     
		2. Assistant Surgeon moves the joystick on camera-angle controller     
		3. The joystick senses movement and sends data to the vision system      
		4. The vision system receives the data     
		5. The vision system directs the camera to move in accordance to data sent by the joystick     
		6. Camera changes angles smoothly     
		7. Assistant surgeon releases joystick     
		8. Camera angle stops changing      
***End:*** The camera is fixed at new angle and the updated location is logged to vision system        
    
3. ***UC3:*** Viewing the operation     
	***Actors:*** Primary Surgeon, Vision System     
	***Description:*** Using First-Person-View goggles to provide the surgeon with real-time visuals of the surgery through the robot camera     
	***Start:*** Goggles are connected to the camera, robot system is turned on, and primary surgeon is wearing FPV goggles     
	***Normal Flow:***      
			1. The camera on the robot system captures live video feed      
			2. The video is sent to the visual system in real-time and continuously     
			3. the vision system processes the data      
			4. the vision system sends data through a wire to the FPV goggles      
			5. The primary surgeon can view the image in real-time       
			6. The vision System continuously updates the feed        
	***End:*** The surgeon receives constantly updated visuals through the FPV      
          
4. ***UC4:*** Emergency button    
	***Actors:*** Assistant Surgeon, Security system    
	***Description:*** in case of emergencies, the assistant surgeon may manually press a button to halt the operation     
	***Start:*** Robot system is turned on and security system is connected     
	***Normal Flow:***     
			1. An error occurs during surgery       
			2. Assistant surgeon presses emergency button on the robot      
			3. Button senses push and sends signal to security system     
			4. Security system receives signal       
			5. Security system sends signal to robot system to halt all operations and movements      
			6. The system displays message that says emergency stop has been activated     
			7. the system remains in fixed state until either the option 'system reset' or 'continue operation' is chosen from the robot system's GUI     
	***End:*** all movement is disabled and the security system logs event        
	***Alternative:***    
			3. button fails to send signal, security system triggers hard shutdown       
			4. if button is pressed accidentally and 'continue operation' is chosen, the robot system asks for confirmation then reactivates and continues operation       
