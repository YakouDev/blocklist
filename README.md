# Kominfo Blocklist
Uncensored Kominfo blocklist taken directly from their site
## Steps to Update this
1. Get repo perms
2. Use Linux
3. Make a .sh file and paste this in
```
#!/bin/bash
# 4. git clone https://YOUR_USERNAME:YOUR_TOKEN@github.com/lepasid/blocklist.git in your Documents folder
# (If you just git clone normally, do git remote set-url origin https://YOUR_USERNAME:YOUR_TOKEN@github.com/lepasid/blocklist.git in the $TARGET_DIR folder)

TARGET_DIR=~/Documents/blocklist
FILE_NAME="$(date +"%Y-%m-%d")"
SOURCE_URL=KOMINFO'S SITE, IF YOU WANT TO KNOW WHAT IT IS JOIN OUR DISCORD
GIT_USERNAME=YOUR_USERNAME
GIT_EMAIL=YOUR_EMAIL

curl --insecure -o "$TARGET_DIR/$FILE_NAME" "$SOURCE_URL"
cd "$TARGET_DIR"

git add "$FILE_NAME"
git commit -m "Add $FILE_NAME"
git config user.name "$GIT_USERNAME"
git config user.email "$GIT_EMAIL"
git push -u origin main

cd ../
echo "Script completed successfully."
```
5. chmod +x YOUR_FILE.sh
7. ./YOUR_FILE.sh
7. Enjoy