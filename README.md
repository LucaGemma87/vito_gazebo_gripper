# vito_gazebo_gripper

This is a simple gazebo plugin able to attach and detach an object grasped by the Pisa IIT Soft Hand

Example of usage of the plugin.

In the gazebo description file of the hand (soft_hand.gazebo.xacro)

you need only to add:


		<gazebo>
      <plugin name="${name}_gazebo_gripper" filename="libvito_gazebo_gripper.so">
		    <updateRate>1000.0</updateRate>
		    <gripperAttachLink>${name}_thumb_knuckle_link</gripperAttachLink>
                       
 		    <gripperLink>${name}_thumb_distal_link</gripperLink>  
		    <gripperLink>${name}_thumb_proximal_link</gripperLink>
		    <gripperLink>${name}_index_knuckle_link</gripperLink>
			  <gripperLink>${name}_index_proximal_link</gripperLink>
			  <gripperLink>${name}_index_middle_link</gripperLink>
 			  <gripperLink>${name}_index_distal_link</gripperLink> 
			
			  <gripperLink>${name}_middle_knuckle_link</gripperLink>
			  <gripperLink>${name}_middle_proximal_link</gripperLink>
        <gripperLink>${name}_middle_middle_link</gripperLink>
 			  <gripperLink>${name}_middle_distal_link</gripperLink>				
			
			  <gripperLink>${name}_ring_knuckle_link</gripperLink>
			  <gripperLink>${name}_ring_proximal_link</gripperLink>
			  <gripperLink>${name}_ring_middle_link</gripperLink>
        <gripperLink>${name}_ring_distal_link</gripperLink> 
		       
			  <gripperLink>${name}_little_knuckle_link</gripperLink>
			  <gripperLink>${name}_little_proximal_link</gripperLink>
        <gripperLink>${name}_little_middle_link</gripperLink>
 			  <gripperLink>${name}_little_distal_link</gripperLink>
		
        <maxRelativeMotionRate>0.005</maxRelativeMotionRate>
        <attachWait>0.1</attachWait> 
        <detachWait>0.0</detachWait> 
     </plugin>
	</gazebo> 
	
	Then start evaluating end refine maxRelativeMotionRate and attachWait and detachWait parameters. 
