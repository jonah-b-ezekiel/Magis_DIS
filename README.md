Magis-100 DIS Github Repository

 - This repository was developed by Jonah Ezekiel (jezekiel@stanford.edu) on behalf of and with guidance from the SLAC Magis team to aid in the development and planning for the diagnostic imaging system for the Magis-100 experiment. This repository provides the functionality to trigger and modify internal variables of Flir Blackfly Model S cameras over software with the purpose of characterizing these cameras and developing and testing the system that will be used to interact with these cameras at the experiment. The planned layout is shown below:
 -
   Ethernet
      |
DC -- PI --(usb 3)--\         /--(usb 3)-- pi-controlled relay --(usb3)-- Cam 3 (Physics)
                      USB HUB --(usb 3)-- pi-controlled relay --(usb3)-- Cam 2
DC -----------------/         \--(usb 3)-- pi-controlled relay --(usb3)-- Cam 1

Directory

- jupyter_notebook: workbooks used for analasys of data taken using camCharacterization script and characterizing cameras (data stored in Slac SDF)
- plots: plots generated by jupyter_notebook file
- src: scripts for interacting with cameras, gpio, aquiring data, etc. See individual file comments for more information
- Makefiles: there are 3 makefiles, each with the ability to compile one of the scripts in src. The working method of compiling scripts has been to copy the correct makefile into the "Makefile" file. 


Spinnaker SDK API User Manual: http://softwareservices.flir.com/Spinnaker/latest/examples.html

Technical Reference for Camera: http://softwareservices.flir.com/BFS-U3-63S4/latest/Model/public/index.html?_ga=2.65493806.1496873635.1659466903-1933567677.1659466900&_gl=1*1rw8way*_ga*MTkzMzU2NzY3Ny4xNjU5NDY2OTAw*_ga_CYF2N4QDDM*MTY1OTQ2Njg5OC4xLjEuMTY1OTQ2Njk0NS4xOA..*_fplc*JTJGVCUyRiUyQlNrQ1BBVWhqOEttT0xSQnolMkJiaUpDM3gxdGNIQ2slMkJwQ3NHclkyUyUyQldrZGlQd0ZaWXJ3RXZjWTBEMUhYSXg5alFzN3EyZmdLWnJKWmZ4Z2xRMCUyQnpJUXZ0bWNlRlRvejVmckpDaHdISlprM2ZqQTFaZGYyWU1oa0RWOGclM0QlM0Q.
