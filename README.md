 Reason why I rebuild the Linux Environment and install all packets is that:
 
 1: In Linux command line, can not import torch module (torch is installed in fact)
 
 2: In Spyder IDE, can not run Mininet module as "Error: Mininet Must Run as Root"

SND-Env-Deployment-in-Ubuntu-MacOS, Linux OS, Mininet Setup, and ML Env Deployment

# Step 1: Install Linux

For Windows: https://www.youtube.com/watch?v=yNmv7GiHIKE

For MacOS: Create Linux OS in UTM (MacM1 OS Software)

######### Method 1

(1) Download 64-bit ARM64 Desktop Image: https://ubuntu.com/download/server/arm  (ubuntu-22.04.1-live-server-arm64.iso)

(2) Error showing: Install Ubuntu desktop in Shell command line, not working for a couple of hours, then I tried another VM software (VirtualBox, also not working after a few trails) 

Then, I come back to UTM and tried it successfully. Follow this vedio: https://www.youtube.com/watch?v=MVLbb1aMk24&t=92s

<img width="921" alt="Screenshot 2022-11-29 at 16 12 13" src="https://user-images.githubusercontent.com/95262224/204582526-c0796f91-dbee-4054-90e8-96c26a37ea39.png">

This installation costs a few minites.

Finished and click button "Reboot Now"

<img width="494" alt="Screenshot 2022-11-29 at 16 14 51" src="https://user-images.githubusercontent.com/95262224/204583117-bc0dae3f-a899-4c31-a967-e4aeb9fb13ed.png">

Then, install Ubuntu desktop using command:

sudo apt upgrade

sudo apt install tasksel

sudo tasksel install ubuntu-desktop

Note: if you are stuck at the step of "sudo tasksel install ubuntu-desktop", please use "sudo tasksel install ubuntu desktop", installation costs a few mins.

########## Method 2 (Recommand use Ubuntu 20.02 Version): 

https://cdimage.ubuntu.com/focal/daily-live/current/  (Use focal-desktop-arm64.iso)


# Step 2: Install Mininet and Ryu controller

Installations:

sudo apt install git

git clone https://github.com/mininet/mininet

mininet/util/install.sh -a

![Screenshot 2022-11-29 at 18 23 06](https://user-images.githubusercontent.com/95262224/204614350-a62a4978-62c5-4c45-9998-bde86617f986.png)

pip install numpy

git clone http://github.com/faucetsdn/ryu.git

cd ryu

sudo pip install -r tools/pip-requires

sudo python3 setup.py install

![Screenshot 2022-11-29 at 18 54 11](https://user-images.githubusercontent.com/95262224/204620474-ffcc2c09-1bc8-440f-9c4e-8d55d8881c51.png)

Then, you need to install: pip install eventlet=0.30.2

![Screenshot 2022-11-29 at 18 56 13](https://user-images.githubusercontent.com/95262224/204620923-e506db8d-9791-4bb3-83f6-ed29d97fcf1e.png)


![Screenshot 2022-11-29 at 19 00 36](https://user-images.githubusercontent.com/95262224/204621768-5c14a7fb-2100-4d61-83c0-0fa56d1ad61f.png)

![Screenshot 2022-11-29 at 19 00 03](https://user-images.githubusercontent.com/95262224/204621655-64677df1-e24e-4e08-9026-ed781bbd8f77.png)

Ryu and Mininet Installed Successfully here!


****** Run: sudo python3 xxx.py, if error showing: "ModuleNotFoundError: Can not import module named torch", (1) first check "pip list" that the missing module is installed; (2) Normally this error is caused that the defaulted path searching by python is different from the sudo path.

Solution: https://blog.csdn.net/weixin_39591031/article/details/122389413

# Step 3: Save and load the A-TCNN model 



# Step 4: Ryu Controller Coding













