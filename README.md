# Wheelchair-Assistance
This is a device that would ultimately be added to an electric wheelchair with actuators to rise and lower the chair to 
assist the user in using the restroom. 

This is a system some classmates and I developed to assist a handicapped person using the restroom. It would ultimately 
be mounted onto an electric wheelchair that would have actuators to lift or lower the chair.

The system is designed to allow the user to accurately approach a toilet of various heights in the reverse direction, 
indicate to the user when they are in the correct final position in regard to the position of the toilet, and allow for 
easy hands-free clean up when finished. The system is composed of two subsystems mounted directly onto the chair and 
controlled by an Arduino Mega. The toilet detector system measures the distance from the chair to the toilet and alerts 
the user when they are within close proximity. The bidet system contains a hose, hydro pump, and fan.

For the reverse positioning system, two distances are needed, the distance from the back of the wheelchair to the front 
of the toilet, and the distance from the lip of the toilet rim to the ground, which are gathered from two independent 
ultrasonic distance sensors and relayed to the Arduino then displayed on an LCD screen. To begin, the user must press a 
button that is mounted on the side of the wheelchair which then turns on both distance sensors, a blue blinking light 
mounted next to the button, and two buzzers that are integrated into the distance sensing software. When the horizontal 
distance is less than 80 inches from the front of the toilet the LCD will begin to display the horizontal distance and 
one buzzer will begin to emit sound. As the user approaches the toilet in the reverse direction the duration of the buzzer 
chirp will increase, going from no sound at 80 inches to a constant buzz at 0 inches, giving the user an audible 
approximation of the distance from the front of the toilet while displaying the exact distance on the LCD screen. As 
the horizontal distance from the front of the toilet approaches 0, the vertical sensor will then pick up the lip of the 
toilet which then begins to display the vertical distance from the ground to the lip of the toilet on the LCD screen as 
well. When the vertical sensor reads the lip of the toilet this will also turn the blue blinking light that is mounted on 
the side of the wheelchair to solid red and sound a second buzzer that will play a constant tone at a different frequency 
than the buzzer used for the horizontal distance, indicating to the user that they are in the final correct position.

When the user is ready, they can activate the bidet system by pressing the button that is mounted on the side of the 
wheelchair a second time. When the button is pressed, it will send a signal to switch a relay that is powered by a 9 
volt battery, that in turn will power a submersible pump that is mounted below the wheelchair in a bottle of water that 
will shoot a stream of water of a duration of 5 seconds and then turn off. After 5 seconds is up, another signal will 
be sent to a second relay powered by the same 9-volt battery that will then power a brushed DC fan for a duration of 5 
seconds to dry the user. After the fan turns off the solid red light that is mounted on the side of the wheelchair will 
then turn green notifying the user that the entire process is complete, and they may now pull away from the toilet.
