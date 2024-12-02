![Sin titulo](https://github.com/alvarobj/improve/blob/main/Images/improve_icon.png)
***
# About
We present IMPROVE [1], a multimodal database for assessing the impact of mobile phone usage on learners engaged in online education in a 30-minutes learning session. IMPROVE is a database which is initially introduced in arXiv technical report and currently under review in [Scientific Data](https://www.nature.com/sdata/) journal.

The IMPROVE database was developed to assess the impact of mobile phone usage on learners engaged in online education in a 30-minutes learning session. It evaluates not only academic performance and learner feedback but also captures biometric, behavioral, and physiological signals, enabling a thorough analysis of how mobile phone use affects learning. Data were collected from 120 learners, categorized into three groups based on their levels of mobile phone interaction. A variety of sensors were utilized to gather data, including electroencephalography (EEG) waves, RGB videos, eye tracking, and heart rate, all of which have been shown in cutting-edge research to be effective indicators of learner behavior and cognition. The database also features metadata derived from processed videos, such as face bounding boxes, facial landmarks, and Euler angles for head pose estimation. Additionally, it contains performance data and self-reported questionnaires from the learners. Phone usage events were labeled, encompassing both supervisor-triggered and uncontrolled instances.

# Motivation
The ever-increasing use of mobile phones has profoundly influenced various aspects of our lives, including education. While online education offers flexibility and accessibility, it also poses unique challenges such as lack of interaction between learners and intructors, feelings of isolation while learning and distractions. Despite extensive research in education and cognitive sciences, there remains a lack of comprehensive datasets that investigate the multimodal impact of mobile phone interaction on learners during online education. Most studies to date have focused on face-to-face learning environments and rely heavily on surveys and questionnaires, limiting the depth of insights into the online learning experience.

IMPROVE is designed to enable researchers and educators to assess the nuanced effects of mobile phone usage on learning outcomes during a 30-minute online learning session. Unlike traditional datasets that focus solely on academic performance or subjective feedback, IMPROVE offers a rich multimodal perspective. It integrates biometric, behavioral, and physiological data, making it a valuable resource for exploring questions at the intersection of education, psychology, and human-computer interaction.

The database stands out for its multidisciplinary approach, incorporating data from EEG signals, eye-tracking, heart rate monitoring, and high-resolution RGB videos. This multimodal design provides a holistic view of how mobile phone usage impacts attention, cognitive load, and emotional states. The inclusion of detailed metadata such as facial landmarks, head pose estimation, and phone usage events ensures that the dataset is both versatile and robust for a wide range of analyses.

By making this resource available to the scientific community, we aim to foster innovative research on digital distractions, learner engagement, and adaptive educational systems. The insights derived from IMPROVE have the potential to inform policies, design interventions, and develop tools that mitigate the negative impact of mobile phone distractions in online learning environments, ultimately enhancing the quality and effectiveness of online education.

# Sensors
The IMPROVE database use a wide range of sensors, as shown in the acquisition setup during the data capture:

![Sin titulo](https://github.com/alvarobj/improve/blob/main/Images/acquisition_setup.png)

- EEG: A NeuroSky EEG headset, which measures the power spectrum density across 5 electroencephalographic channels ($\alpha, \beta, \gamma, \delta, \theta$). Through the preprocessing of these EEG channels, estimates of attention and meditation levels, as well as the occurrence of eye blinks, are obtained. 
- Eye-tracker: A Tobii Pro Fusion\footnote{\url{https://go.tobii.com/tobii-pro-fusion-product-description}} equipped with two high-speed infrared cameras configured at 120 Hz for eye tracking. This device estimated the following data: gaze origin and point, pupil diameter, eye movement type (fixation, saccade, unclassified, eyes not found), event duration, data quality, eyeblink, and more; allowing us to measure visual attention.
- Smartwatches: 2 different smartwatches, the Huawei Watch 2 and the FitBit Sense, were used to monitor heart rate, stress level (EDA sensor) and inertial sensors (gyroscope and accelerometer).
- Cameras: 2 Logitech C170 cameras (side and overhead) operating at 20 Hz with a resolution of 640x480, and one front-facing RealSense camera were used. The RealSense camera contains one RGB camera and two NIR cameras, with dimensions of 90 mm length x 25 mm depth x 25 mm height. The NIR cameras are monochrome and sensitive in both the visible spectrum and NIR, following the sensitivity curve of the CMOS sensors. The three cameras were configured to operate at 30 Hz and 1280x720  resolution, and depth images are obtained by combining their three image channels.
- Keyboard and Mouse Activity: Keystrokes, mouse position, time between keystrokes, mouse wheel movements, etc., are monitored.
- Screen Capture: The monitor screen is captured at a frequency of 1 Hz.
- Logging data: Information about the activities learners engaged in and their phone usage timing was also captured.

# Experiment Groups
Three different groups were formed:
- Group 1: Mobile phone use and possession allowed. The device was placed on the learner's desk, visible to the learner, with sound and vibration activated.
- Group 2: Mobile phone possession was allowed, but their use was prohibited. The device was also placed on the learner's desk, but with the screen facing down, and with sound and vibration activated.
- Group 3: The mobile phone was confiscated during the whole learning session.
    
# Task
The learners were monitored while participating in a learning session about HTML in a MOOC. Before the session, they completed a pretest to assess their prior knowledge of HTML. During the session, learners watched instructional videos, read documents on language syntax and coding, completed assignments to evaluate their learning, and reviewed their mistakes.

# Code

# Download Data
Download license agreement, send by email one signed and scanned copy to atvs@uam.es according to the instructions given.


Send an email to atvs@uam.es, as follows:

Subject: [DATABASE: IMPROVE]


Body: Your name, e-mail, telephone number, organization, postal mail, purpose for which you will use the database, time and date at which you sent the email with the signed license agreement.


Once the email copy of the license agreement has been received at ATVS, you will receive a link to download the database.


For more information, please contact: atvs@uam.es

 [Download license agreement](https://github.com/alvarobj/improve/blob/main/License/IMPROVE_License_Agreement.pdf)

 # References
[1] IMPROVE

  # Related works
 - Becerra, A., Daza, R., Cobos, R., Morales, A., Cukurova, M., & Fierrez, J.  
  **M2LADS: A System for Generating Multimodal Learning Analytics Dashboards.**  
  *In Proc. IEEE 47th Annu. Comput., Softw., Appl. Conf. (COMPSAC)*, pp. 1564–1569, 2023.

- Daza, R., Morales, A., Fierrez, J., Tolosana, R., & Vera-Rodriguez, R.  
  **mEBAL2 Database and Benchmark: Multispectral Eyeblink Detection.**  
  *Pattern Recognition Letters*, **182**, pp. 83–89, 2024.

- Becerra, A., Irigoyen, J., Daza, R., Cobos, R., Morales, A., Fierrez, J., & Cukurova, M.  
  **Biometrics and Behavior Analysis for Detecting Distractions in E-Learning.**  
  *In Proceedings of the International Symposium on Computers in Education (SIIE)*, pp. 1–6, 2024.

- Daza, R., Gomez, L. F., Fierrez, J., Morales, A., Tolosana, R., & Ortega-Garcia, J.  
  **DeepFace-Attention: Multimodal Face Biometrics for Attention Estimation with Application to E-Learning.**  
  *IEEE Access*, **12**, pp. 111343–111359, 2024.

