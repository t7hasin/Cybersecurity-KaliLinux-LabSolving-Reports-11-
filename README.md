# Kali Linux Foundation Building 
# Problem 1 - Lock python version to prevent updates during full system upgrades
Step by step commands that are used - 
1. python3 --version
2. sudo apt-mark hold python3
3. apt-mark showhold
4. sudo apt-mark unhold python3 [Later use]
# Problem 2 - Download htop source, compile via 'make', and execute the binary
1. sudo apt install -y build-essential git
2. git clone [latest source code - take from browser]
3. cd htop
4. ./autogen.sh
5. ./configure
6. make
7. ./htop
# Problem 3 - Identify Kernel version and list all currently loaded memory modules
1. uname -r
2. lsmod | less
# Problem 4 - Enable SSH and restrict login access to a specific username only
1. sudo apt install openssh-server
2. sudo systemctl enable --now ssh
3. sudo nano /etc/ssh/ssh_config
4. AllowUsers [your_name] 
Then press ctrl + O,enter and ctrl + x
5. sudo systemctl restart ssh
6. sudo systemctl status ssh
# Problem 5 - Identify top CPU process, pause for 60 seconds and then resume
1. mousepad &
2. pidof mousepad
3. kill -STOP [PID number]
4. sleep 60
5. kill -CONT[PID number]

