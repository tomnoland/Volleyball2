# Volleyball2

cd /Volumes/Data/Projects

cd ~

---

REPO_NAME=Volleyball2

hub delete -y tomnoland/$REPO_NAME

git clone https://github.com/tomnoland/$REPO_NAME

cd $REPO_NAME

---

git add README.md

git commit -m "Changed README.md file"

git push origin master

---

git pull origin master

---

/usr/bin/open -a /System/Library/CoreServices/Finder.app .

"/Applications/NetBeans/Apache NetBeans 11.1.app/Contents/Resources/NetBeans/bin/netbeans" README.md

