***CSI Data Retrieval, Visualization, and Storage Program***

   This application is designed to efficiently retrieve Channel State Information (CSI) data from a router, specifically from the recvCSI program running on the      router. The primary functions of this program include real-time visualization of the CSI data and the option to store the collected information in the labtop.

***Sample Setup for Visualizing CSI***

   The experimental setup involves three devices: two wireless routers and one labtop.

1. Access Point (AP) Configuration:
   
   The first wireless router, designated as A, operates as an Access Point (AP).

   The second wireless router, labeled B, and the labtop establish connections with this AP.

3. Initialization of recv_csi Tool on A:
   
   A initiates the recv_csi tool, accessible here (Routers/recvCSI), with the IP address of the labtop and port 1234.

   The command would resemble: ./recv_csi2 <labtop_IP> 1234.

5. Visualization Setup:
   
   The labtop launches the run_visualization.py script from the provided folder.

   This script is instrumental in visualizing the real-time CSI data.

   The command would resemble: ./sendDatacontp wlan <i> <Mac_Address> <time_interval > <num_packets>. 

   For example: ./sendDatacontp wlan0 64:70:02:CB:FC:27 50000 100

   **It will send 100 packets time interval between them 0.05 second

7. Data Transmission from B:
   
   B launches the send_data tool, available here (Routers/sendData).

   Packages sent by B should now be received and processed by the labtop.

***Troubleshooting:***

   If the labtop fails to receive packages, firewall issues should be investigated.

   Confirm the correct UDP port configuration in the recvCSI program arguments.

   Ensure the presence of the 'pyqt' library, a prerequisite for the visualization script.




