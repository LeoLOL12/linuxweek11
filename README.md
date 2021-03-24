# linuxweek11
Linux Week11 lab

# Script 
- Filename: weather_chk
- Usage: Check weather of the current location (based on IP address) by using wttr.in

1. Make a new directory /home/vagrant/week11
`mkdir /home/vagrant/week11`
2. Copy the script to /home/vagrant/week11
`cp weather_chk /home/vagrant/week11`


# Service
- Filename: wthr.service
- Usage: A service to execute script weather_chk

1. Copy the wthr.service to /etc/systemd/system
`sudo cp wthr.service /etc/systemd/system`


# Timer
- Filename: wthr.timer
- Usage: A timer to run wthr.service hourly

1. Copy the wthr.timer to /etc/systemd/system
`sudo cp wthr.timer /etc/systemd/system`
2. Start the timer
`sudo systemctl start wthr.timer`
3. (Optional) Enable the timer service (run at boot)
`sudo systemctl enable wthr.timer`


# Result
- A file with weather informatoin will be created /home/vagrant/week11/weather.txt
- The file will be updated hourly




# Check the timer
Run this to check the status of the timer `systemctl status wthr.timer`
- Make sure it is in active status

# List the timer
Run this to list the timer details `systemctl list-timers wthr.timer`

