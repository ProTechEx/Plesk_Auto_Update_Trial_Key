[![Build Status](https://travis-ci.com/megoRU/Plesk_Auto_Update_Trial_Key.svg?branch=master)](https://travis-ci.com/megoRU/Plesk_Auto_Update_Trial_Key) 
![GitHub All Releases](https://img.shields.io/github/downloads/megoRU/Plesk_Auto_Update_Trial_Key/total) 
[![GitHub stars](https://img.shields.io/github/stars/megoRU/Plesk_Auto_Update_Trial_Key)](https://github.com/megoRU/Plesk_Auto_Update_Trial_Key/stargazers)
[![GitHub license](https://img.shields.io/github/license/megoRU/Plesk_Auto_Update_Trial_Key)](https://github.com/megoRU/Plesk_Auto_Update_Trial_Key/blob/master/LICENSE)

# Plesk auto-update trial key
Plesk trial key auto-update

## Replace with your data:
private static final String CONN = "jdbc:mysql://IP:3306/ "database name without quotation marks" ?useSSL=false&serverTimezone=UTC&characterEncoding=utf8"; <br>
private static final String USER = ""; // LOGIN <br>
private static final String PASS = ""; // PASS  <br>

private static final String SSH_HOST = ""; // IP <br>
private static final String SSH_LOGIN = ""; // LOGIN <br>
private static final String SSH_PASSWORD = ""; // PASS <br>

## Create table in MySQL:

```
CREATE TABLE `Plesk` (
  `id` int(6) NOT NULL,
  `text` varchar(255) NOT NULL,
  PRIMARY KEY (`id`),
  UNIQUE KEY `text` (`text`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8;
```
```
INSERT INTO Plesk (id, text) values (0, "Your Key");
INSERT INTO Plesk (id, text) values (1, "Your Key2");
INSERT INTO Plesk (id, text) values (2, "Your Key3");
```

## Launch parameters:

java -jar Plesk_Auto_Update_Trial_Key.jar "ip address MySQL" "user MySQL" "pass MySQL" "ip address SSH" "login SSH" "pass SSH"

## Run on Linux (Debian/Ubuntu):
sudo apt-get install screen <br>

screen -dmS jar1 bash -c "java -jar Plesk_Auto_Update_Trial_Key.jar "ip address MySQL" "user MySQL" "pass MySQL" "ip address SSH" "login SSH" "pass SSH" "

## Get free key:
https://www.plesk.com/plesk-free-download/ <br>
https://temp-mail.org/ru/ <br>

## FAQ & Troubleshooting

• On Windows/MacOS, install Oracle Java from [here](https://www.oracle.com/java/technologies/javase-downloads.html) or OpenJDK from [here](https://adoptopenjdk.net/).
