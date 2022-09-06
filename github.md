### create a new repository on the command line
```
echo "# <new-repo>" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/arashnm80/<new-repo>.git
git push -u origin main
```
