# iCopy Version 0.2.x

[<img src="https://f002.backblazeb2.com/file/jsuforum-upload/optimized/1X/cff2835c1652bb57a18aac42a3eee34b51cd9b89_2_1380x386.gif" width="50%" alt="iCopy">](https://bbs.jsu.net/c/official-project/icopy/6)  

[![iCopy Telegram-Bot](https://img.shields.io/badge/iCopy-Telegram%20BOT-red?style=flat-square&logo=appveyor)](https://bbs.jsu.net/c/official-project/icopy/6)
[![Programming Language](https://img.shields.io/badge/LANGUAGE-Python%203.6%2B-success?style=flat-square&logo=appveyor)](https://bbs.jsu.net/c/official-project/icopy/6)
[![Version](https://img.shields.io/badge/Version-0.2.0--beta.6.4-ff69b4?style=flat-square&logo=appveyor)](https://bbs.jsu.net/c/official-project/icopy/6)
[![License](https://img.shields.io/github/license/fxxkrlab/iCopy?style=flat-square&logo=appveyor)](https://bbs.jsu.net/c/official-project/icopy/6)
[![DATABASE](https://img.shields.io/badge/DATABASE-MongoDB-brightgreen?style=flat-square&logo=appveyor)](https://github.com/mongodb/mongo)
[![Stars](https://img.shields.io/github/stars/Nenokkadine/iCopy-Heroku?style=flat-square&logo=appveyor)](https://github.com/Nenokkadine/iCopy-Heroku)  


## Install  

1.Python 3.6+ is Required  
2.Mongodb is Required  
3.Pre-install and Configured [fclone](https://github.com/mawaya/rclone/releases/tag/fclone-v0.3.1) is Reqired  
&nbsp;&nbsp;&nbsp;&nbsp;For Linux directly use this command  
&nbsp;&nbsp;&nbsp;`bash <(wget -qO- https://git.io/JJYE0)`  
4.`git clone https://github.com/fxxkrlab/iCopy.git && cd iCopy`  
5.`chmod +x iCopy.py`  
6.`pip3 install -r requirements.txt`  
7.&nbsp;Edit config/conf.toml

## Requirements for Heroku Deployment
1. Heroku CLI
2. Latest `git` Installed on ur PC.

## Deployment to Heroku
1. First U should have a Heroku Account
2. Go to heroku and Create a New app
3. And then add a Config Var `RCLONE_CONFIG`  as `/app/rclone.conf` 
4. Go to the build packs section in settings and click add buildpack and enter "https://github.com/Nenokkadine/heroku-buildpack-Fclone-mod.git" as buildpack url then click save changes.
5. Add Another Build Pack "Python" Which will be Available there.
4. Now `git clone https://github.com/Nenokkadine/ICopy-Heroku.git && cd ICopy-Heroku`
5. Copy Your Service Accounts to accounts folder
6. Edit `config/conf.toml`  With MongoDB URL and Bot Token etc.
7. Copy a Remote u Created Using FClone/GClone to ` rclone.conf`  and Dont forget to Give the same name of the Remote `config/conf.toml`
8. Open rclone config and edit `service_account_file_path = /app/accounts/` as the json paths
9. Now Open Terminal/CMD in the same location
10. Now Type the following Commands

   |              Commands                |
   | :----------------------------------: |
   | `git init`                           |
   | `heroku login`                       |
   | `git add .`                          |
   | `heroku git:remote -a YOURAPPNAME`   |
   | `git push heroku master`             |

10. Now go to resourses section and Turn the Worker ON


