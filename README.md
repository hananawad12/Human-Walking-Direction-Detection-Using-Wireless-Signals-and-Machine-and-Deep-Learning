# Human-Walking-Direction-Detection-Using-Wireless-Signals-and-Machine-and-Deep-Learning
we introduced a device-free method that can precisely identify the direction of human walk using CSI of Wi-Fi signals, machine, and deep learning algorithms. Raw CSI signals are first calibrated and effectively denoised using Hampel filter and DWT algorithms.
We conducted extensive experiments in two indoor environments. Our system, using SVM and CSI amplitudes, achieved recognition accuracy of 92.9\%, 95.1\%, and 89\% in the classroom, meeting room, and both rooms, respectively. Additionally, our system, employing 1D-CNN and CSI amplitudes, demonstrated recognition accuracy rates of 88.1\%, 100\%, and 84.2\% in the classroom, meeting room, and both rooms, respectively.  

Our experiments consistently proved the robustness of our system in various scenarios. The accuracy remained stable even with an increasing number of volunteers and different training sizes, different individuals, environments, group sizes, and training data variations. Our approach demonstrates versatility in its applicability across various scenarios. It can be effectively employed to track the walking direction of customers in retail stores. Furthermore, in security systems, it proves valuable for monitoring human walking directions and detecting unauthorized access in restricted areas.

----------------------------------------------------------
# Repository Structure:

The repository is structured into five key directories, each serving a distinct purpose:

***Routers:***

This directory encompasses the source code for two essential programs: sendData and recvCSI.
sendData is responsible for transmitting data packets from one router, while recvCSI calculates the Channel State Information (CSI) data on another router.
The calculated CSI data is subsequently sent to a user's computer via a UDP connection for further processing.

***Experiment:***

This directory houses a program named run_visualization.py.
This program functions as a listener for the recvCSI program, facilitating the real-time visualization of incoming data and storing it in a file for subsequent analysis.
Additionally, the directory includes a script named run_test_client.py designed for a dummy server, emulating incoming data from the router to aid in testing scenarios.
A sample CSI data file, stored in binary format as it emanates from the router, is also provided under the path data/sample_csi_packet_big_endian.dat.

***Preprocessing and Training:***

Within the model directory, all the code pertaining to the Proprocessing and training of the Data.

***- Propressing:***

*Amplitudes are affected by various types of outlier and noise, from limited bandwidth to transition rate and power adaptations, as well as thermal noise. Consequently, signal outliers arise that are not attributable to human actions. To address this problem, the Hampel filter algorithm is applied.

*To extract the useful features of CSI amplitudes, we used DWT. The DWT algorithm can be used to decompose the CSI into multiple levels of wavelet coefficients, each representing different frequency bands in the signal. The high-frequency wavelet coefficients represent the noise and other high-frequency components of the signal, while the low-frequency coefficients represent the smoother components of the signal. By filtering out the high-frequency coefficients representing noise and high impulses and retaining the low-frequency coefficients, the denoised signal is obtained.  

*Finally, reconstructing the data.

***- training:***

* Various notebooks used to train the data, we evaluate the performance of our approach using a variety of machine and deep learning classifiers, including RF, KNN, SVM, and 1D-CNN.

***Dataset:***

The dataset is structured with a hierarchical organization, encompassing nine folders, each corresponding to a distinct user. Within each user folder, there exist two subfolders, namely "classroom" and "meeting room," signifying the source of the data collected from two distinct rooms.

--------------------------------------------------------------------------------------
# Dataset:

The dataset can be downloaded by the following [Link](https://doi.org/10.6084/m9.figshare.24718371.v1)
.


