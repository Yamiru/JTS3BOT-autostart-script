# JTS3BOT-autostart-script
JTS3ServerMod - TS3 Server Bot init.d script to automatic start JTS3BOT on boot as diferent user.


![Build Status](https://img.shields.io/badge/Build Status-passed-green.svg)
![JTS3BOT](https://img.shields.io/badge/tested%20version%20JTS3BOT-6.0.7-red.svg)
![java](https://img.shields.io/badge/java-version%201.8.0__66-orange.svg)
![os](https://img.shields.io/badge/tested OS-Ubuntu server 15.10 x64-blue.svg)
##Requirements
- debian based OS
- sudoers   (```aptitude install sudo```)
- nano editor (```sudo apt-get install nano```)
- screen (```sudo apt-get install screen```)
- downloaded JTS3ServerMod - TS3 Server Bot init.d https://www.stefan1200.de/forum/index.php?topic=2.0
- dir location of mc /opt/ts3bot/
- installed latest java (```sudo apt-get install default-jre```)
- user teamspeak3bot  (```sudo adduser --disabled-login teamspeak3bot```) 
- permission for teamspeak3bot user (```sudo chown teamspeak3bot:teamspeak3bot -R /opt/ts3bot```)


##How to build
1. Terminal/Console:

    ``` sh
     cd /etc/init.d
    ```
    ``` sh
     nano ts3bot
    ```

2. paste/rewrite code from ts3bot file [ts3bot](https://github.com/Yamiru/JTS3BOT-autostart-script/blob/master/ts3bot) 
3. CTRL+X
4. Y
(name:ts3bot)
5. ENTER 
6. Terminal/Console:


    ```
     sudo chmod 755 /etc/init.d/ts3bot
    ```
7. Terminal/Console:

    ```
     sudo update-rc.d ts3bot defaults
    ```


8. Terminal/Console:

``` reboot ```


 
##Commands

stop  ts3bot :  ```     service ts3bot stop    ```
    
start ts3bot  :  ```     service ts3bot start    ```



Chceck java version ```     java -version    ```
If you change /etc/init.d/ts3bot file --->  ```  sudo ts3bot ts3bot defaults ```    &   ```     systemctl daemon-reload    ```  
If not work starting try to stop ```     service ts3bot stop    ``` 


If not work starting try to stop ```     service ts3bot stop    ```  and start again  ```     service ts3bot start    ```  !!!
