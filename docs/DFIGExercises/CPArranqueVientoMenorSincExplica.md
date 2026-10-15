# Explanation of the signal evolution

!!! tip "🎯 Explanation of the signal evolution during cutin"
    ***Objective:*** Understand the Controller logic during start-up: how the Pitch acts to accelerate the Power Train up to the target RPMs and how the power stabilizes.
    ***What to observe:*** The Pitch evolution, the Power Train acceleration, the start of the electrical power and the subsequent deceleration until the stable point.
    💡 Why does the electrical power cause a Power Train deceleration just after the B2B connects to the grid?

!!! warning "❓ Guiding questions"
    1. Why does the Controller force the Pitch to practically 0º when the target RPMs are reached?
    2. What happens to the Power Train acceleration when electrical power begins to flow to the grid? Why?
    3. What is the Pitch role during start-up to control the acceleration speed?

| ![](<lib/DFIG Caso conexion a 7 - 3 Detail.jpg>) | The figure on the left shows the time interval from when the hydraulic brake is released until the Electrical Power delivered to the grid reaches its target. It can be seen that the Controller keeps modifying the blade Pitch value so that the Power Train reaches its rpms target (for the existing wind), in the fastest way. Shortly after the B2B controller closes the Generator stator connection with the grid, a net flow of Electrical Power to the grid begins, which causes the Power Train to decelerate. Finally that acceleration is 0 when the target rpms for the existing wind are reached. At that moment the Controller forces the Pitch to practically 0º, which is the one that allows extracting the maximum power from the existing wind. |
|---|---|

*The key concepts for the Grid Connection or Start-up or Cutin operation are the following:*  
*1) Control the Pitch so that the Power Train reaches its rpms target in the shortest possible time.*  
*2) Use the Back-to-Back converters capacity to control the power delivered to the grid helping the control described in point 1, from 0 to the target value corresponding to the existing wind smoothly, without creating large grid disturbances.*  
*3) After the target rpms have been reached, control the Pitch in a coordinated way with the B2B control so that the greatest possible power is extracted from the wind.*
