# SND-Env-Deployment-in-Ubuntu-MacOS
Linux OS, Mininet Setup, and ML Env Deployment

Step 1: Install Linux

For Windows: https://www.youtube.com/watch?v=yNmv7GiHIKE

For MacOS: Create Linux OS in UTM (MacM1 OS Software)

(1) Download 64-bit ARM64 Desktop Image: https://ubuntu.com/download/server/arm  (ubuntu-22.04.1-live-server-arm64.iso)

(2) Error showing: Install Ubuntu desktop in Shell command line, not working for a couple hours, then I tried another VM software (VirtualBox, also not working after a few trails) 

Then, I come back to UTM and tried it successfully. Follow this vedio: https://www.youtube.com/watch?v=1WWj6qoWhJw
https://www.youtube.com/watch?v=MVLbb1aMk24&t=92s

<img width="921" alt="Screenshot 2022-11-29 at 16 12 13" src="https://user-images.githubusercontent.com/95262224/204582526-c0796f91-dbee-4054-90e8-96c26a37ea39.png">

This installation costs a few minites.

Finished and click button "Reboot Now"

<img width="494" alt="Screenshot 2022-11-29 at 16 14 51" src="https://user-images.githubusercontent.com/95262224/204583117-bc0dae3f-a899-4c31-a967-e4aeb9fb13ed.png">

Then, install Ubuntu desktop using command:

sudo apt upgrade

sudo apt install tasksel

sudo tasksel install ubuntu-desktop

Note: if you are stuck at the step of "sudo tasksel install ubuntu-desktop", please use "sudo tasksel install ubuntu desktop", installation costs a few mins.

Step 2: Install Mininet

Step 3:

Step 4:
