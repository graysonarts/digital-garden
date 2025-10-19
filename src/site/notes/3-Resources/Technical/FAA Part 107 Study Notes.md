---
{"dg-publish":true,"permalink":"/3-resources/technical/faa-part-107-study-notes/","tags":["🌱_Processing"],"updated":"2025-10-18T23:14:20.686-07:00"}
---

# Important References
- FAA-H-8083-25B - Pilot Handbook
- FAA-G-8082-22 - Remote Pilot - sUAS Study Guide
- FAA-S-ACS-10 - Remote Pilot - sUAS Airman Certification Standard

# Loading and Performance

- 3 axes of rotation
	- Roll is tilting left and right
		- Aeleron. On a quad, right stick left and right
	- Pitch is tilting up and down
		- Elevator. On a quad, right stick up and down
	- Yaw is panning left and right
		- Rudder. On a quad, left stick left and right
	Power on a quad is left stick up and down, and that controls elevation
		For fixed wing, power is forward thrust
* Flight Forces
	* Summary of Forces
		* Fixed Wing
			* Lift is force applying "up" on the aircraft
			* Weight is the force applying "down". gravity
			* Thrust is force created by the primary engine. Prop or Jet
			* Drag is wind resistance opposite thrust
		* Quad (rotorcraft)
			* Lift is created by the motors
			* Weight is gravity
			* Thrust is when we tilt the quad in a direction, thrust is created in that direction
			* Drag is wind resistance opposite thrust
## Forces

### Lift
* Quad - Produced by the motors
* Fixed - created by the wing (airfoil)
* Applied as the Center of Pressure/Lift (CP/CL)
* Counteracts the Weight
* _Relative Wind_ is parallel to the flight path in the opposite direction
	* Pretend that the aircraft is fixed in position
* _Leading Edge_ (airfoil) where the wind hits the airfoil and splits the air above and below the surfaces
* _Trailing Edge_ (airfoil) where the wind remerges at the back of the airfoil
* _Chord Line_ (airfoil) the line drawn between the leading and trailing edge
* _Angle of attack_ (airfoil) the angle between the chord line and the relative wind
* Lift is always perpendicular to the relative wind.
* Proportional to speed of aircraft and angle of attack
	* Faster speed or increase angle of attack = more lift
* Lift is governed by [[3-Resources/Atomic Notes/Newton's 3rd Law\|Newton's 3rd Law]] and [[3-Resources/Atomic Notes/Bernoulli's Principle\|Bernoulli's Principle]]
### Drag
* Always perpendicular to the lift (basically, the relative wind)
* _Resultant Force_ (airfoil) the total lift. From vector math, subtract the drag from the true lift, I think
* 2 types of drag
	* _Parasite Drag_ by product of flying through the air
		* As speed increases, parasite drag increase.
		* Three types of Parasite drag
			* _Form Drag_ the shape of an object (e.g. Truck vs sports car)
			* _Interference Drag_ increased drag created by the junction between different objects
			* _Skin Friction_ any imperfections on the surface of the lift generating object (propeller, wing, etc)
	* _Lift Induced Drag_ 
		* As soon as lift is created for fixed wing
		* As soon as we have lateral movement for quads
		* LID becomes less as speed increases
			*  proportional to angle of attack
* Drag can cause _stall_ based on Angle of Attack usually at low speed
	* only a fixed-wing can stall
	* only way to recover is to lower the nose of the aircraft
	* Can occur when the critical angle of attack is reached regardless of airspeed
### Weight
* Result of gravity
* Applied as center of gravity. This is different than the center of pressure/lift.
* Always points to center of earth
* Every aircraft has a maximum allowable weight to be able to leave the ground.
	* If exceeded, no flight
### Thrust
* Created by the propeller
* A Propeller is just an airfoil and creates lift using the same principles as a wing.
* In a quad, thrust is only created when the quad is banked, otherwise, it's creating only lift
* Trust > Drag = Accelerating
* Drag > Thrust = Decelerating 
* Drag == Thrust = Consistent speed
* If Thrust == 0 then Drag == 0, meaning you aren't moving

## Load Factor (G-Force)
* It's the acceleration of gravity.
* Increases with the bank/roll angle of the aircraft
* Sometimes called the Resultant Force
* Load is equal to the lift
* Typical values of load factor at angles, not it's exponential
	* 0° = 1
	* 10° = 1.015
	* 30° = 1.154
	* 45° = 1.414
	* 60° = 2
	* 85° = 11.473
* Also effects stall speed
	* Load factor increases with bank angle
	* stall speed increases with load factor
	* fly at slow airspeed when doing abrupt maneuvers to avoid stalling

## Stability
* Ability to return to the original flight path after being disturbed
* Static Stability - Initial ability to return to equilibrium.
	* Positive static stability is returning back to equilibrium
	* Neutral static stability is not returning but not getting worse
	* Negative static stability is getting worse after disturbance
* Dynamic Stability - Aircrafts response over time when disturbed
	* Positive-Static-Positive-Dynamic - returns back to stability
	* Positive-Static-Neutral-Dynamic - oscillates "forever"
	* Positive-Static-Negative-Dynamic - oscillates with increasing amplitude "forever"

## Performance Factors
### Center of Gravity Location
* _CG_ = The point at which WEIGHT is applied
* _CP_ = The point at which LIFT is applied
* _Arm_ = Distance between the CG and where a force is applied
* _Moment_ = Efficiency of the force = Arm × Force
* There are limits to where the CG can go based on aircraft design. When mounting things to sUMAs you must take into account resulting CG
* Make sure the loaded equipment does not negative impact the CG. Too forward or aft can cause crashes
* A large arm between CG and CP will cause a large moment. The elevator help compensate for that. Taildown force is the force created by the elevator.
* With an AFT CG - fixed wing
	* Higher cruising speeds
	* Increase Range
	* Faster take offs
	* Decreased Stability
	* Maybe uncontrollable
	* Over rotation on take offs and flaring on landing
	* lower stall speed
* With a forward CG - fixed wing
	* mostly the opposite of everything above
	* easier stall recovery
* Exceeding CG Limits (envelope of the aircraft)
	* Uncontrollable
	* Too far forward, can't get off the ground - fixed wing
	* Too far aft, stall immediately - fixed wing
	* For quad - motors have to work harder in an imbalance
	* Make sure weight is also within limits

### Altitude
* As altitude increase, air pressure decreases
* Performance will decrease because it's moving less air
### Temperature
* increased temperature means decreased performance
* though battery efficiency decreases at low temperatures too, which will decrease performance
### Humidity
* increased humidity means decreased performance too.
* humid air has more density, meaning more drag
### Weight
- Heavier weight requires more lift which usually requires faster speeds

### Other factors to consider
- Launch area
- Surface
- Surface Wind
- Obstacles