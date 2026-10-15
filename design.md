# Exercise 3 - Self-Driving Trailer Agent 

## 1. PEAS Framework
The PEAS framework describes the Performance measure, Environment, Actuators and Sensors of the self-driving trailer travelling from Nairobi to Kisumu.

* **Performance Measure:** Find the shortest route from Nairobi to Kisumu, successfully pass the goal test upon arrival, reach the destination safely, follow traffic rules, save fuel and deliver the cargo on time without damage.
* **Environment:** Kenyan highways, towns such as Nairobi, Nakuru, Kericho and Kisumu, other vehicles, pedestrians, traffic, potholes, roadblocks and weather conditions. 
* **Actuators:** Steering wheel for changing direction (including making left or right turns at town junctions), accelerator for increasing speed, brakes for slowing down or stopping, and indicators, lights and the horn. 
* **Sensors:** GPS and maps for identifying the trailer's current state or location, running goal tests and finding routes; cameras, radar and LiDAR for detecting obstacles; and a speedometer and odometer for tracking speed and distance. 

## 2. Five Definitions of the Agent's Environment

1. **Fully Observable vs. Partially Observable**
   * **On the actual road:** The environment is partially observable because the trailer's sensors cannot see everything around it and some information (like blind spots, heavy fog or what is happening around a corner) is hidden or noisy.
   * **On the map:** The environment is fully observable because the agent has complete access to the map information, including all towns and distances, before choosing a route.

2. **Deterministic vs. Stochastic**
   * **On the actual road:** The environment is stochastic because there are unpredictable elements outside the agent's control, such as sudden traffic jams, reckless driving by others, rain or tyre problems.
   * **On the map:** The environment is deterministic because the next state depends entirely on the current state and the agent's chosen action (for example, moving from Nairobi to Nakuru reliably results in arriving at Nakuru with a fixed distance).

3. **Episodic vs. Sequential**
   * **Sequential:** The environment is sequential because current actions heavily depend on previous ones. Each choice of action affects all future states; for example, choosing to travel through Nyeri instead of Nakuru changes the entire subsequent path and total distance to Kisumu.

4. **Static vs. Dynamic**
   * **On the actual road:** The environment is dynamic because it continues changing while the agent deliberates and decides what to do (other vehicles move, traffic lights change and pedestrians cross).
   * **On the map:** The environment is static because the map remains completely still while the agent calculates the shortest route.

5. **Single-Agent vs. Multi-Agent**
   * **On the actual road:** The environment is multi-agent because the trailer operates alongside other drivers, matatus and pedestrians in the same environment.
   * **On the map:** The environment is single-agent because the trailer operates completely alone when solving the route-planning search problem.
