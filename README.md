# JTS3BOT-autostart-script
JTS3ServerMod - TS3 Server Bot init.d script to automatic start JTS3BOT on boot as diferent user.


<img src="https://img.shields.io/badge/Build%20Status-passed-green.svg" alt="status-passed"> <img src="https://img.shields.io/badge/tested%20version%20JTS3BOT%20-6.5.3-red.svg" alt="JTS3SERVERMOD - TS3 SERVER BOT"> <img src="https://img.shields.io/badge/java-jdk1.8.0__181-orange.svg" alt="OpenJDK Runtime Environment"> <img src="https://img.shields.io/badge/tested%20OS-Debian%20server%209.6%20x64-blue.svg" alt="debianos">

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

If you change /etc/init.d/ts3bot file --->  ```  sudo update-rc.d ts3bot defaults ```    &   ```    systemctl daemon-reload     ```  
If not work starting try to stop ```     service ts3bot stop    ``` 


If not work starting try to stop ```     service ts3bot stop    ```  and start again  ```     service ts3bot start    ```  !!!
