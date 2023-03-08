# just-some-material




Chapter 2

ROBOTIC VEHICLES

2.1.	Introduction
2.1.1.	What are robotic vehicles?

The ﬁeld of robotics encompasses a broad spectrum of technologies in which computational intelligence is embedded in physical machines, creating systems with capabilities far exceeding the core components alone. Such robotic systems are then able to carry out tasks that are unachievable   by conventional machines, or even by humans working with conventional tools. The ability of a machine to move by  itself, i.e.,  “autonomously,” is one such capability that opens up an enormous range of applications that are uniquely suited to robotic systems. This chapter describes such unmanned and autonomous vehicles and summarizes their development and application within the international perspective of this study.
Robotic  vehicles  are  machines  that  move  “autonomously” on the
ground, in the air, undersea, or in space. Such vehicles are “unmanned,” in the sense that no humans are on board. In general, these vehicles move by themselves, under their own power, with sensors and computational resources onboard to guide their motion. However, such “unmanned” robotic vehicles usually integrate some form of human oversight or supervision of the motion and task execution. Such oversight may take diﬀerent forms, depending on the environment and application. It is common to utilize so-called “supervisory control” for high-level observation and monitoring of vehicle motion. In other instances, an interface is provided for more continuous human input constituting a “remotely operated vehicle” (ROV). In this case, the ROV is  often  linked  by  cable or wireless communications in order to provide higher bandwidth communications of operator input. In the evolution of robotic vehicle technology that has been observed in this study, it is clear that a higher
 
12	Robotics: State of the Art and Future Challenges


level of autonomy is an important trend of emerging technologies, and the ROV mode of operation is gradually being replaced by supervisory control of autonomous operations.
2.1.2.	Why are robotic vehicles important?

First, robotic vehicles are capable of traveling where people cannot go,  or where the hazards of human presence are great. To reach the surface  of Mars, a spacecraft must travel more than 1 year, and on arrival the surface has no air, water, or resources to support human life. While human exploration of Mars may someday be possible, it is clear that robotic exploration is a fundamental step that provides enormous scientiﬁc and technological rewards enhancing our knowledge of other planets. The National Aeronautics and Space Administration (NASA) Mars rover shown in Fig. 2.1 is a robotic vehicle that has successfully achieved these goals, becoming a remote scientiﬁc laboratory for exploration of the Martian surface. The Mars rover is an example of a robotic vehicle under supervisory control from the earth, and capable of local autonomous operation for segments of motion and deﬁned scientiﬁc tasks.
Another example of a hostile and hazardous environment where robotic
vehicles are essential tools of work and exploration is the undersea world. Human divers may dive to a depth of 100 m or more, but pressure, light,

Fig. 2.1. NASA Mars rover (NASA Jet Propulsion Laboratory (JPL)).
 
Robotic Vehicles	13

Fig. 2.2. IFREMER ASTER autonomous underwater vehicle.



currents, and other factors limit such human exploration of the vast volume of the earth’s oceans. Oceanographers have developed a wide variety of sophisticated technologies for sensing, mapping, and monitoring the oceans at many scales, from small biological organisms to major ocean circulation currents. Robotic vehicles, both autonomous and ROV types, are an increasingly important part of this repertoire, and provide information that is unavailable in other ways. Figure 2.2 shows an autonomous underwater vehicle (AUV) called ASTER under development at Institut Franc¸ais de Recherche pour l’Exploitation de la Mer (IFREMER), the French National Institute for Marine Science and Technology. ASTER will be used for coastal surveys up to 3000 m in depth and is capable of carrying a wide variety of instrumentation for physical, chemical, and biological sensing and monitoring. In research in the US, the evolution of remotely operated vehicles for deep ocean exploration enabled the discovery of the sunken Titanic and the ability to explore that notable shipwreck.
In addition to space and oceans, there are many applications where
human presence is hazardous. Nuclear and biological contamination sites must often be explored and mapped to determine the types and extent of contamination, and provide the basis for remediation. Military operations incorporate many diﬀerent autonomous and remotely operated technologies for air, sea, and ground vehicles. Increasingly, security and defense systems may use networks of advanced mobile sensors that observe and detect potential events that may pose threats to populations.
 
14	Robotics: State of the Art and Future Challenges

(a)	(b)
Fig. 2.3. (a) Agricultural robotic vehicle (International Harvester, the United States).
(b)	Mining haul truck (ACFR, Australia).



In a second class of applications, robotic vehicles are used in routine tasks that occur over spaces and environments where machine mobility can eﬀectively replace direct human presence. For example, large-scale agriculture requires machines to cultivate, seed, irrigate, and harvest very large areas of terrain. The ability to track an autonomous vehicle using global positioning systems (GPS), sensing the soil and plant conditions in the ﬁeld, encourages the implementation of robotic vehicles for agricultural or “ﬁeld” applications. Figure 2.3a shows an example of an agricultural robotic vehicle under development in the United States. Figure 2.3b shows a large autonomous mining haul truck developed in Australia.
Similar challenges occur in areas of environmental monitoring, where
mobile vehicles may move through air, water, or ground to observe the presence of contaminants and track the patterns and sources of such pollutants. In large manufacturing facilities, mobility is essential to tran- sport components and subassemblies during the manufacturing process and a variety of robotic guided vehicles are utilized in these domains.
A third class of applications of robotic vehicles occurs in the support
of personal assistance, rehabilitation, and entertainment for humans. A robotic wheelchair may provide mobility for a human who would otherwise not be able to move about. The integration of sensors, computational intelligence, and improved power systems have made such personal robotic aids increasingly capable and practical for everyday use. An example of  a wheelchair that utilizes emerging robotic technologies for guidance and balance is shown in Fig. 2.4. More details on medical robotics and robotic aids to the handicapped will be described in Chap. 6.
 
Robotic Vehicles	15

Fig. 2.4. IBOT advanced wheel chair (DEKA, the United States).


Other examples of such personal aids include vehicles that support elderly care through feeding, household tasks, and emergency notiﬁcation. Many daily household tasks may beneﬁt from enhanced mobile robotics, and there are rapid commercial developments of vacuum cleaners and lawn mowers that utilize advanced sensor and navigation systems. Also, advanced entertainment systems will incorporate robotic vehicles including locomotion of humanoids and biomimetic pets that entertain and provide interactive companions. The Japanese development of humanoids and robotic pets with sophisticated locomotion systems, as shown in Fig. 2.5, is a major topic of this international comparative study. While Sony no longer manufactures robots like the QRIO shown in Fig. 2.5(a), it is included here since it was one of the most advanced humanoid entertainment robots at the time of this study. More detailed examples of personal and entertainment robotic vehicles will be described in Chap. 5, and of humanoid robots in Chap. 4.

2.1.3.	How do robotic vehicles work? What are the key technologies for mobility?
Robotic vehicles move on the ground, through the air, and on and under the water. To achieve these various modes of propulsion, a large number of diﬀerent technological solutions have been proposed and investigated.
 
16	Robotics: State of the Art and Future Challenges

Fig. 2.5. Humanoid robots with locomotion (left: Sony, right: Honda).


As illustrated in Table 2.1, there are two major approaches to the evolution of these technologies in the robotics research ﬁeld.
(a)	“Wheels and props” strategy.
Engineering solutions are borrowed from the evolution of technologies that have been developed over many centuries for transportation. Robotic ground vehicles are developed with wheels and treads, much like automobiles. Robotic air vehicles are developed with propellers, or jet engines, and stationary wings (or rotating wings, such as helicopters). Robotic undersea vehicles utilize propellers and control surfaces.
(b)	“Running and ﬂapping” strategy.
In the evolution of robotics, there is a long tradition of utilizing biological systems as inspiration and models for new technological solutions. The Japanese research laboratories have been particularly interested and eﬀective in these eﬀorts toward “biomimetics.” There has been a community of international researchers that has worked on the development of legged locomotion systems, including bipedal locomotion that resembles human walking and running. Similarly, there have been robotic snakes that slither, birds and insects that ﬂap their wings, and ﬁsh and eels that swim using undulating motions. There has even been recent work on hybrid systems, such as “Whegs,” combining attributes of wheels and legs.
 
Robotic Vehicles	17




 
18	Robotics: State of the Art and Future Challenges


Biomimetics research has two important broad goals. First, these eﬀorts to replicate the motion of biological organisms will teach us about the natural world. Therefore, the engineering of an artiﬁcial swimming ﬁsh will help us to understand the physical process, the energetics, and the control systems used by these creatures. Second, these studies provide insight into practical systems that may have advantages over the engineering solutions mentioned earlier. For  example, one may argue that legged locomotion  is much better suited to  rough terrain where foot placement may be  used more eﬃciently than wheels. Similarly, there is evidence that the energy eﬃciency of some biological organisms including ﬂying insects and ﬁsh exceeds that of engineering systems, and therefore important new developments could emerge. These goals may also intersect in applications such as personal robotics where robotic pets or entertainment devices may resemble biological creatures in both physical and behavioral manner.
2.2.	Research Challenges

Historically, there have been examples of technologies that could be controlled through remote mechanical linkages (e.g., mechanically coupled manipulators for handling dangerous chemicals), and other technologies that provided preprogrammed motions (e.g., missiles and torpedoes). However, only with the development of microelectronics and embedded computation it has been possible to design systems that combine both mobility and autonomy. Four major research challenges have dominated these developments, and they continue to represent the key themes observed in this international study.

2.2.1.	Mechanisms and mobility

As described above, both engineering and biomimetic approaches have been taken to design mobile robotic vehicles, and current research eﬀorts continue to follow both of these strategies. Key research themes include the following: Principles of motion. Basic studies of kinematics and dynamics  of motion in all domains (ground, air, and water) continue to examine fundamental issues of devices that contact  and  interact  with  the  forces around them. A primary example of this work is the study of bipedal locomotion and the distinction between “quasistatic” walking and “dynamic” walking. Algorithms used in recent full-humanoid prototypes exhibit very sophisticated motion and balance, but still do not achieve
 
Robotic Vehicles	19


all of the characteristics of human dynamic balance. New theories and experiments continue to impact this research. Similarly, such studies have a direct eﬀect on diﬀerent walking patterns, such as trotting and running gaits, and how these may be executed on two-legged and multi-legged robotic vehicles.
Materials properties and design. Materials considerations are also of primary interest for new mechanisms, and uses of light and strong materials, with controllable compliance, are the current research topics.

2.2.2.	Power and propulsion

The long-term autonomy of vehicles is directly impacted by the available power and the energy eﬃciency of motion. These considerations are of additional importance in remote domains, such as planetary and undersea deployments, where recovery or refueling is impractical. While battery technologies are of primary interest for all such vehicles, from vacuum cleaners to spacecraft, there are premiums obtained by eﬃcient motion and even sharing of tasks among multiple vehicles. In addition,  there  are several strategies for energy storage (e.g., fuel cells, and microfuel cells), as well as strategies for energy harvesting in many forms (e.g., solar cells, ocean temperature gradients and currents, wind, and biological batteries), and energy management using sophisticated control techniques to improve energy budgets. Figure 2.6 shows a solar-powered autonomous underwater vehicle capable of recharging on the surface and diving for 6–8 h of continuous underwater operation.
Biomimetic approaches to create artiﬁcial muscles using specialized
materials and methods of micro and nanofabrication are also a topic of current research.

2.2.3.	Computation and control

The introduction of microcomputation has enabled the use of embedded computer systems that are small, light, and energy eﬃcient. Such embedded computational systems have been instrumental in the development of robotic vehicles with sophisticated computer architectures that organize sensor-based feedback and control actions onboard. Much of the current research internationally is focused on advanced computer architectures and implementations that coordinate these tasks. There are two fundamental
 
20	Robotics: State of the Art and Future Challenges

Fig. 2.6. Solar-powered AUV (Autonomous Undersea Systems Institute (AUSI), FSL, Rensselaer Polytechnic Institute (RPI), the United States).

strategies that are often integrated into these systems — hierarchical and behavioral control structures.
Hierarchical (or deliberative) control structures. In a complex system, engineers are often led to deﬁne hierarchies representing diﬀerent levels of functions of the system. From the engineering perspective, they hope to simplify design principles and criteria in a manner that will permit more consistent and veriﬁable designs. Such an engineering approach often supports systematic techniques for error detection, service, and support as well as formal approaches to analysis and optimization of the system. As suggested in Fig. 2.7, one such hierarchy might represent a strategic plan (e.g., “go to the stone”) deﬁning a high-level task. The strategic plan might then generate a navigation plan (e.g., “ﬁrst, go to the corner, then turn left”), followed by a supervisory control (e.g., “pick a point 10 m away with no likely collisions”), and a ﬁrst simple motion control (e.g., “move the wheel motors at one revolution per minute”).
Behavioral control structures. The behavioral control architecture may be thought of as a biomimetic analog to the nervous system of animals. Biological creatures seem to incorporate many sensor-based feedback systems that evolve in a behavioral context. These systems seem to provide a stable and context-sensitive response to complex situations, without constructing an explicit and detailed internal representation of
 
Robotic Vehicles	21

Fig. 2.7. Integration of hierarchical and behavior control architectures in a search-and- rescue domain (Center for Robot-Assisted Search and Rescue (CRASAR), University of South Florida (USF), the United States).


the environment at all levels. Such behavioral feedback loops may also integrate learning procedures and mechanisms that permit the system to adapt to changing conditions and to preferentially react to environmental conditions that are signiﬁcant  to  the  task  or  behavior  at  hand.  For example, a robotic vehicle might approach a door using an algorithm to maximize the observed opening area. This algorithm moves the robot closer to the door, as well as perpendicular to the door opening. The vehicle could move through the door using this implicit sensory feedback without computing an explicit representation of geometries and distances.
Both hierarchical and behavioral architectures are active areas of research and many practical vehicles integrate some features of both approaches. Trade-oﬀs occur where hierarchical architectures may be more provably robust since formal analytical methods may be applied, while behavioral systems may be more eﬃcient to implement and computationally faster, and may support adaptive methods more naturally. On the implementation side, all computational and control architectures for sophisticated vehicles require careful and disciplined software engineering to implement and maintain. Integration of such embedded software systems is a major key to the success and longevity of vehicle prototypes and products. In addition, advances in communication technologies provide information links for command and control and have a strong role in multivehicle and distributed architectures.
 
22	Robotics: State of the Art and Future Challenges

2.2.4.	Sensors and navigation

Recent advances in successful robotic vehicle technologies for ground, air, and water have been tied to the development of improved sensors and sensor networks. Such sensors serve two major purposes on robotic vehicles:
(a)	Sensors are used to monitor the environment and to control interactive tasks. For example, an underwater vehicle might detect the presence of biological contaminants in the water, map the distribution, and support analyses that would identify the source. One area of technology advancement is the development of microelectronics and micro- electromechanical systems technologies for speciﬁc sensors in air and water. For example, detection of nitrogen compounds in air, and detection of dissolved oxygen in water, support valuable environmental applications.
(b)	Sensors are essential for the navigation of a robotic vehicle. Each vehicle
must sense its surroundings and utilize the relative locations of events and landmarks in order to answer questions: Where am I? Do I have a map of this area? How do I move in order to accomplish my task? New sensor technologies include laser-based techniques, such as Light Detection and Ranging (LIDAR), which generate depth maps of solid objects, permitting the robot to detect both obstacles and landmarks and integrate them into their navigation strategies.
Navigation and localization have been very important topics in the research community over the past 10 years. The problem of simultaneous localization and mapping (SLAM), also called cooperative mapping and localization (CML), is a research ﬁeld with signiﬁcant outcomes that have directly inﬂuenced the reliability and practicality of robotic vehicle deployments in real applications. Important results, particularly in the United States, Europe, and Australia, have derived algorithms that enable a vehicle to eﬃciently learn a “map” of its environment, then utilize that map as the basis for planning navigation leading to the accomplishment of goals. Such algorithms are now commonly implemented in some form on most prototype and production vehicles, ranging from vacuum cleaners, to underwater vehicles, to planetary explorers and agricultural devices.
The principle of the SLAM algorithms is a sophisticated and  elegant
mathematical formulation that represents the detected features of the environment by probability distributions. By moving a vehicle, or using several vehicles, to observe the same features, the consistency of these probability distributions is resolved into a small number of feasible maps
 
Robotic Vehicles	23


that describe the world being explored. Currently these methods are used to eﬃciently and reliably resolve two-dimensional domains of modest size, such as a building layout or a local outdoor setting. Research is still being pursued to enlarge the size of these domains, improve the consistency required to resolve rarer events that occur at large scales, and extension of the basic approach to enable computational eﬃciency of these methods in three dimensions.
SLAM algorithms provide an example of the importance of basic
analytical research that stimulates advances in practical applications. As an example, in military applications the integration of ground, air, and water sensors and vehicles is essential to fully interpret the activities     in a theater of operations. As suggested in Fig. 2.8, the complexity of dynamic coordination of large-scale operations using sensor feedback and real-time assessment is extremely complex. Algorithms such as SLAM

Fig. 2.8. Integration of sensor and navigation in a military application (U. Penn, the United States).
 
24	Robotics: State of the Art and Future Challenges


deﬁne fundamental principles that underlie the consistent interpretation of such complex activities, and support the development of reliable implementations.

2.3.	International Survey

Robotic vehicles have been a principal theme of robotics research in many of the laboratories that were visited in this international survey. In many cases, the emphasis on the types of vehicles, the approaches to design, and the applications of interest have varied among these diﬀerent international communities. This section summarizes these observations.

2.3.1.	Research on robotic vehicles — the United States

In the United States, research on robotic vehicles has emphasized work in the following ﬁve areas.
2.3.1.1.	Military and defense systems
The US federal government investment in robotic vehicle research has strongly emphasized the development of ground, air, and underwater vehicles with military applications. As shown in Fig. 2.9, there have been signiﬁcant accomplishments in these areas in which large development programs have resulted in capable and reliable vehicle systems. Many of these systems are deployed in a “remotely operated” mode, i.e., a human controller works interactively to move the vehicle and position it, based on visual feedback from video or other types of sensors. In addition, there is a strong emphasis on integration of autonomous probes and observers with other parts of the military tactical system. The integration of sophisticated computer and communications architectures is an essential feature of these systems, and the use of algorithms such as SLAM to interpret complex scenes is an important contribution to these systems. The United States is generally acknowledged as the world leader in military applications of robotic vehicle technologies. As indicated in Chap. 1, in 2004 and 2005 the US Department of Defense conducted competitive Grand Challenge events in which autonomous robotic vehicles navigated and drove over 200 km in oﬀ-road desert conditions; in 2007 they navigated in an urban area.
2.3.1.2.	Space robotic vehicles
The ﬁeld of space robotics was identiﬁed as a topic for separate focus in this study and the major results of that eﬀort will be presented in Chap. 3.
 
Robotic Vehicles	25
 
26	Robotics: State of the Art and Future Challenges


In the context of vehicle technologies, the recent Mars rover programs have uniquely demonstrated perhaps the most successful deployment of robotics vehicle technologies to date in any domain of applications. The rovers have landed and explored the surface of Mars and have carried out important scientiﬁc experiments and observations that have dramatically enhanced human understanding of that planet and its natural history. This US NASA eﬀort has been the only successful demonstration of interplanetary vehicle space technology and is clearly recognized as the world leader in this domain.
2.3.1.3.	Field robotics
Robotic vehicles developed for both military and space applications are intended for use in rough terrain, i.e., without roads or cleared areas. In this context, the experience of oﬀ-road robotic vehicles in the United States has also provided a basis for research in ﬁeld robotics, the application of robotic vehicles to other unstructured domains, such as agriculture, mining, construction, and hazardous environments. In addition, the US industrial companies active in these areas have invested in prototype developments for these applications. Figure 2.3(a) is an example of such a prototype vehicle.
2.3.1.4.	Undersea robotics
The United States has supported research in several diﬀerent types of applications of underwater vehicles. These include:

(a)	Military and defense applications As described in ‘Military and Defense Systems,’ the US defense technologies have included many fundamental prototypes and products that provide both ROV and AUV technology for the military. Figure 2.9 shows several of these vehicles.
(b)	Coastal   security   and   environmental monitoring  systems.	AUV
systems may be used as surveillance and observance of the systems with both defense and environmental implications. Figure 2.10 shows an overview of the autonomous oceanographic sensor network (AOSN) systems, deployed as an experiment at the Monterey Bay Aquarium Research Institute (MBARI) in California, which integrate many diﬀerent robotic and sensor resources.
(c)	Scientific	mission	and	deep	ocean	science.	AUV	and	ROV
technologies are the only means to actively explore large portions of the ocean volume. The study of ocean currents, ocean volcanoes, tsunami detection, deep-sea biological phenomena, and migration and changes
 
Robotic Vehicles	27

Fig. 2.10. Advanced oceanographic sensor network (MBARI, the United States).


in major ecosystems are all examples of topics that are studied with these systems. Several of the major scientiﬁc laboratories in the world are located in the United States and are leaders in these ﬁelds. A new project, HROV, is funded by the National Science Foundation (NSF) to develop a new hybrid remotely operated vehicle for underwater exploration in extreme environments, capable of operation at 11,000-m depth as shown in Fig. 2.11.
2.3.1.5.	Search-and-rescue robotics
In recent years, there has been an increased emphasis on eﬀective response to natural disasters, from earthquakes to hurricanes, in addition to other events, including terrorist activity. Robotic  vehicles  provide  a  means to explore such hazardous sites at times of extreme danger, providing information to support other responses and guiding search-and-rescue activity at the site. Rapid and reliable response and eﬀective links to human interaction are essential features of these systems. An example of a search- and-rescue robotic vehicle system is shown in Fig. 2.12.
2.3.2.	Research on robotic vehicles — Japan and South Korea

In Japan and South Korea, there is a long history of research on robotic vehicles with an emphasis on biomimetic systems and their applications to
 
28	Robotics: State of the Art and Future Challenges

Fig. 2.11. HROV (Hybrid ROV) project (Johns Hopkins University (JHU) and Woods Hole (WHOI), the United States).

Fig. 2.12. Search-and-rescue robotics (CRASAR, USF, the United States).
 
Robotic Vehicles	29


personal and service systems. In addition, there is signiﬁcant research in underwater vehicles.
2.3.2.1.	Personal and service robotic vehicles
In Japan and South Korea there have been broad national initiatives  that have shaped the course of research activities. Projections of the economic value of robotics technology have suggested that personal and service applications, including entertainment,  are  major opportunities for Japanese industry to build international markets. In this context, Japanese researchers have identiﬁed applications areas in household, eldercare, security and surveillance, and entertainment robotics as the areas of opportunity. Examples of household robotic vehicles include vacuum cleaners, as shown in Fig. 2.13, with projections of signiﬁcant economic markets developing in the next ten years. Eldercare robotics is viewed as a high priority in both Japan and South Korea where aging populations suggest a need for service and support technologies. These technologies and markets will be discussed further in Chap. 5, but mobility is a primary requirement for many of these markets and both wheeled and legged ground vehicles are important constituents of the development eﬀorts. Japan is viewed as a world leader in developing personal, service, and entertainment robots with potential international markets.
2.3.2.2.	Biomimetic mobility
In both Japan and South Korea, there has been signiﬁcant research eﬀort in the development of mechanisms and systems that mimic biological mobility

Fig. 2.13. Personal and service robots (Hanool, South Korea).
 
30	Robotics: State of the Art and Future Challenges


systems. These projects range from ﬂying insects to snakes and swimming ﬁsh, and include both two-legged and multi-legged locomotion. Studies from a ﬂying insect project in Japan are shown in Fig. 2.14a. A robotic swimming ﬁsh from South Korea is shown in Fig. 2.14b, while a brachiation robot (swinging between tree limbs) is shown in Fig. 2.14c.
Humanoid walking and bipedal locomotion have been a major focus of
development in conjunction with recent humanoid projects in Japan and South Korea (see Chap. 4). As shown in Fig.2.5, these humanoid robots are sophisticated and have achieved signiﬁcant results in bipedal locomotion, including stair climbing.
2.3.2.3.	Undersea robotics
In both Japan and South Korea there are signiﬁcant research eﬀorts in underwater robotics. Sites of particular interest include:
The Japan Agency for Marine-Earth Science and Technology (JAMSTEC) has developed very sophisticated deep-sea vehicles for ocean science and exploration of ocean resources. Figure 2.15 shows the URASHIMA vehicle, which is 10 m long and will be powered by fuel cell technology.
The Ura Laboratory, University of Tokyo, has developed a series of underwater vehicles that are used in ocean research, and have  also been used in environmental monitoring experiments in fresh water environments (Lake Biwa Research Institute). Figure 2.16 shows the photo of a vehicle from the University of Tokyo laboratory.
The national laboratory Korean Ocean Research and Development Institute (KORDI) has developed undersea vehicle technology that is used in ocean science and monitoring ocean resources.

2.3.3.	Research on robotic vehicles — Europe

European research laboratories have emphasized the development of fundamental capabilities of robotic vehicles, including navigation systems and architectures, as well as applications in areas such as transportation systems, personal and service robotics, and undersea vehicles.
 
Copyright © 2008. Imperial College Press. All rights reserved.












(a)	(b)






 

Univ Tokyo, Japan
 
(c)
 

 
Univ Nagoya, Japan
Fig. 2.14. Projects in biomimetic robot design. (a) Insect flight studies (Uno, U. Tokyo, Japan). (b) Robotic fish (Pohang Univ. of  Science & Technology (POSTECH), South Korea). (c) Brachiation robot (U. Nagoya, Japan).
 
32	Robotics: State of the Art and Future Challenges

Fig. 2.15.  URASHIMA AUV (JAMSTEC, Japan).



Fig. 2.16. Tri-Dog AUV with sensor guidance (U. Tokyo, Japan).
2.3.3.1.	Navigation and architectures
Signiﬁcant fundamental research has been carried out at several laboratories, including the Laboratoire d’Analyse et d’Architecture des Syst`emes (LAAS) laboratory in Toulouse, France, the Robotics Laboratory at the University of Oxford, the United Kingdom, and the University of Karlsruhe, Germany, on computational architectures and communications in support of algorithms for navigation and mapping. These programs have
 
Robotic Vehicles	33

Fig. 2.17. Sensor-based mapping and localization using SLAM algorithms (U. Oxford, the United Kingdom).


contributed signiﬁcantly to the international community in sensor-based navigation and vehicle control systems. An example of sensor-based map building from the University of Oxford is shown in Fig. 2.17. European laboratories have been among the leaders in international research in these fundamental areas.
2.3.3.2.	Transportation systems
In European community programs, there has been investment in the development of robotic vehicles that could contribute to transportation systems and be used in urban environments. Figure 2.18 shows an example of the CYBERCar at l’Institut National de Recherche en Informatique et en Automatique (INRIA) Sophia-Antipolis, France, demonstrating vision- based following control. Figure 2.19 shows the implementation of vehicle- based vision systems for vehicle following and road following at high speed at the University of Braunschweig, Germany. European programs have demonstrated unique capabilities in these urban applications of robotic vehicle technologies.
2.3.3.3.	Personal and service robotics
A number of European programs have also addressed the issues of personal and service robotics, including household robots, rehabilitation and eldercare robotics, and search-and-rescue robotics. Figure 2.20 shows
 
34	Robotics: State of the Art and Future Challenges

Fig. 2.18.  CYBERCar prototype (INRIA, France).

Fig. 2.19.  Autonomous   road  following  and  vehicle  following  at  high  speed   (U. Braunschweig, Germany).


Fig. 2.20. Prototype vehicles used in urban and indoor settings.
 
Robotic Vehicles	35


mobile robots that have been developed for urban and indoor settings. Related medical and rehabilitation applications will be described in more detail in Chap. 6.
2.3.3.4.	Undersea robotics
European programs have been very active in undersea robotics research. Programs at the Heriot-Watt University in Edinburgh, the United Kingdom, Southampton University in the United Kingdom, IFREMER in  Toulon,  France,  Cybern´etix  in  Marseille, France,  and  the  University of Girona, Spain, all have signiﬁcant research programs with prototype vehicles and systems that contribute to international collaborative projects. Figure 2.21 shows several prototypes and products including the ALIVE AUV developed by Cybern´etix in conjunction with IFREMER and Heriot-Watt University. Figure 2.20 also shows the Garb´ı AUV used in experiments at the University of Girona. Research at Heriot-Watt University brings a strong systems capability (supporting software systems) that contributes to eﬀective navigation and task control of AUVs.

2.4.	Comparative Review of Programs

Based on the visits described in this book and the review of national programs in this international community in the area of robotic vehicles, a number of research priority areas have become clear. These research priorities are summarized in Table 2.2.

Table 2.2. International research priorities in robotic vehicles.
Region	Research priorities
 
The United States	Outdoor vehicular mobility: ground, air, undersea
Navigation and mapping in complex outdoor environments
Japan and South Korea	Indoor mobility using humanoid locomotion
Novel mechanisms of locomotion
Key applications: service, entertainment, commercial
Europe	Mobility in urban and built environments Sensor-based navigation with maps
Key applications: Infrastructure support and transportation
 
36	Robotics: State of the Art and Future Challenges
 
Robotic Vehicles	37


In summary, in the area of research in robotic vehicles, this study concludes:
The US leadership in robotic vehicles has been strongly dependent on federal mission-oriented programs (DOD, NASA, and other agencies), and continuity of investment in basic research will be critical.
The United States lags in the identiﬁcation of strategic priorities
that could translate vehicle capabilities to innovation and commercial, industrial, and civil infrastructure applications.
Japan and Korea have aggressive national plans and investment to develop mobile robots supporting personal and service applications, including healthcare and eldercare.
The European Community has developed strategic plans that coordinate vehicle programs and emphasize civilian and urban infrastructure, as well as some space applications.
Other countries, particularly Australia, have made signiﬁcant contri- butions to both theory and implementation of these technologies. International capabilities will continue to grow and more countries will demonstrate capability to build both prototype and commercial systems meeting applications needs.
Key future challenges in robotic vehicle research will include:
•	Multivehicle systems.
—	Distributed sensor networks and observatories.
•	Long-term reliable deployment.
•	Micro and nanoscale mobility.
•	Eﬃcient and independent power.
•	Human–robot vehicles.
•	Interactions.
—	Service and entertainment.
2.5.	Further Readings

The following recent books provide an overview of research progress in the ﬁeld of robotic vehicles, and related topics in computational architectures, navigation, and mapping algorithms.
 
38	Robotics: State of the Art and Future Challenges

1.	R. C. Arkin, Behavior-Based Robotics (MIT Press, Cambridge, MA, 1998).
2.	G. A. Bekey, Autonomous Robots: From Biological Inspiration  to Implementation and Control (MIT Press, Cambridge, MA, 2005).
3.	T. Braunl, Embedded Robotics: Mobile Robot Design and Applications with Embedded Systems (Springer-Verlag, New York, 2001).
4.	H. Choset, K. Lynch, S. Hutchinson, G. Kantor, W. Burgard, L. Kavraki   and S. Thrun. Principles of Robot Motion: Theory, Algorithms, and Implementations (MIT Press, Cambridge, MA, 2005).
5.	G. Dudek and M. Jenkin, Computational Principles of Mobile Robotics.
(Cambridge University Press, Cambridge, MA, 2000).
6.	D. Kortenkamp, R. P. Bonasso and R. Murphy, Artificial Intelligence and Mobile Robotics: Case Studies of Successful Robot Systems (AAAI, New York, 1998).
7.	R. Madhavan, E. R. Messina and J. S. Albus, Intelligent Vehicle Systems
(Nova Science Publishers, Hauppauge, NY, 2007).
8.	R. Murphy, An Introduction to AI Robotics (MIT Press, Cambridge, MA, 2000).
9.	U. Nehmzow, Scientific Methods in Mobile Robotics: Quantitative Analysis of Agent Behavior (Springer, New York, 2006).
10.	R. Siegwart and I. R. Nourbakhsh, Introduction to Autonomous Mobile Robots
(MIT Press, Cambridge, MA, 2004).
11.	S. Thrun, W. Burgard and D. Fox, Probabilistic Robotics (MIT Press, Cambridge, MA, 2005).
