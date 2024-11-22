# Exploring Specialized Congestion Algorithms for Low Earth Orbit Satellite Networks

### Aims
Our growing demand for fast internet has extended its reach beyond the Earth, pushing development into space where data is transmitted via satellites in low Earth orbit. With billions of dollars in funding, satellite internet has been in the works for years, and companies like Starlink (currently the most competitive in the market) have already launched thousands of active satellites. It won’t be long before this service becomes commercially available. These technologies aim to provide high-speed internet even in the most remote areas, places where traditional ISPs find it unprofitable to expand.

However, these advancements come with added complexity. Satellite networks are inherently dynamic due to the rapid movement of satellites in orbit. As a result, the routes that packets take change frequently, leading to fluctuating round-trip times (RTTs). Traditional congestion control algorithms like Cubic are not designed to handle routers in motion, interpreting these fluctuations as signs of network congestion and adjusting the transmission window inefficiently.

This project seeks to explore the performance characteristics of emerging algorithms like HPCC, OrbTCP, and other techniques being developed for satellite networks and data centers. By emulating their performance in satellite environments, we aim to evaluate their effectiveness in handling the unique challenges of these networks.

## Objectives 
1. Research and understand how HPCC operates by reviewing published studies.
2. Research and understand the workings of INT through an analysis of published studies.
3. Research and understand how UDT functions by studying relevant academic publications.
4. Investigate whether MiniNet can emulate HPCC and OrbTCP by examining its GitHub repository.
5. If MiniNet proves unsuitable, identify alternative emulation platforms.
6. Analyze the performance characteristics of the algorithms by running simulations or emulations.
# Relevance
One of the key aspects of this project is the research involved. Given that the topic is relatively new and not yet fully implemented, much of the available information will come from academic literature, which is often written for readers with substantial expertise in the field. Gaining experience in extracting valuable insights from these sources will be highly beneficial for my career, especially when exploring new topics and developing innovative solutions.

Another important aspect is the use of existing tools and libraries for emulation. These tools are often niche and may lack comprehensive documentation, which means I may need to rely on reading and understanding the code directly. Developing this ability is crucial for success as a programmer, as we often spend more time reading code than writing it.

If the implementation is successful, I will have the opportunity to analyze the performance of the algorithms, sharpening my critical thinking skills to interpret the observed patterns. This experience could be highly relevant if I decide to pursue research in any field later on.

# Resource Required
This project might require more powerful servers to run the emulation if it requires intensive computing.

# Weekly Timetable
|     | Monday  | Tuesday | Wednesday | Thursday | Friday  | Saturday | Sunday |
| --- | ------- | ------- | --------- | -------- | ------- | -------- | ------ |
| 9   |         |         |           |          |         |          |        |
| 10  | Lecture |         | Lecture   |          |         | Project  |        |
| 11  |         |         |           |          |         | Project  |        |
| 12  |         | Lecture |           | Seminar  |         | Project  |        |
| 13  | Lab     | Lecture | Lecture   |          | Lab     | Project  |        |
| 14  |         |         |           |          | Lab     |          |        |
| 15  | Lecture | Project | Project   | Project  | Lecture |          |        |
| 16  | Lecture | Project | Project   | Project  | Lecture |          |        |
| 17  |         | Project | Project   | Project  |         |          |        |
| 18  |         | Project | Project   | Project  |         |          |        |
# Project Timeline
###### Autumn Semester
Week 6: Read academic literatures on HPCC, and UDT. Start writing the interim report.
Week 7: Research MiniNet and UDT User space as well as finish writing the interim report.
Week 8: Research how to implement HPCC in MiniNet framework
Week 9: Start the implementation of HPCC with MiniNet and UDT userspace.
Week 10: Continue the implementation of HPCC with MiniNet and UDT userspace.
Week 11: Continue the implementation of HPCC with MiniNet and UDT userspace.
###### Spring Semester
Week 1: Analyse the performance results of HPCC and evaluate the correctness of the emulation.
Week 2: Improve on the implementation.
Week 3: Analyse the performance results of HPCC and evaluate the correctness of the emulation.
Week 4: Research OrbTCP and other related algorithms
Week 5: Research how to implement the OrbTCP and satellite constellations with MiniNet
Week 6: Research how to implement the OrbTCP and satellite constellations with MiniNet
Week 7: Implement of the OrbTCP and satellite constellations with MiniNet
Week 8: Implement of the OrbTCP and satellite constellations with MiniNet
Week 9: Analyse the performance results of emulation and its correctness
Week 10: Discuss and reason about the results and work towards finishing the report
Week 11: Polish the report


