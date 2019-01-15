### 1915 - Virtual-Reality-Based-Preoperative-Surgery-Planning-System ###

# Introduction  

Precision OS is a company that develops a realistic Virtual Reality surgery environment. Drawing upon the talents of game designers and the expertise of orthopedic surgeons, they can simulate real operating procedures with a high degree of accuracy. One use case for Precision OS’s virtual surgery environment is to allow surgeons to practice new procedures and develop skills in a simulated setting. Another use case is to assist in pre-operative planning for specific surgeries, using real data from patients modeled in 3D. For this second use case Precision OS can take CT (Computerized Tomography) scans of broken bones belonging to real patients and generate 3D models from this data. Precision OS would like a feature where the user, a surgeon, could drag the 3D model of the patient's fractured bone to an approximate position on the reference model and have a program automatically identify what bone it is, rotate the bone to the correction orientation and connect the bone to the proper position on the reference model. This feature would help to optimize a surgeon’s workflow and decrease surgery planning time. Substantial research exists for the matching and registration of 3D models in general. Tools such as ITK exist that have built in functionality for rotating and transforming an object so that it best matches the orientation of another object and providing metrics for the goodness of fit. Precision OS has done some research already using this tool which we hope to build upon. Other research has found methods for distinguishing between different 3D objects based on random point distributions, though not specifically between different bones. 

# Problem Statement  

For our capstone project we have been tasked by Precision OS to develop a custom identification and interfacing software solution that will be used by Orthopedic surgeons to plan out procedures on real-life patients. Using our solution, a surgeon should be able to drag an 3D model bone from a menu onto a reference model skeleton in the VR environment and have the bone automatically move into place. The piece of software must therefore be able to perform the following tasks: 

1. Analyze a 3D bone (.obj and or .fbx format) using various algorithms and then classify the type of bone (i.e. femur, tibia, skull); this process will be referred to as identification 

2. Using the above information, correctly orientate and place the bone into a VR environment using a fully automated method and or a combination of user inputs. This will be referred to as transformation.

For the purposes of this project our core objective will be to identify and properly orient three different 3D models of fractured bones using algorithms that we develop. These algorithms will then be implemented in C++ with a user interface and visualization in the Unreal Engine.
