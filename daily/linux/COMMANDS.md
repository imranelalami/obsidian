# git

  my tokn : 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

  Set Up Git:
   git config --global user.name "Your Name"
   git config --global user.email "youremail@domain.com"

git rm -r --cached . = remove all the added to staged faze 
git add -A = add all folders back and forth 
git log = to see all ur saves
git show <"commit hash"> = show u the content of a specific commit 
git diff = show u what u modified
git restore = restore a deleted file
git commit -m "something" --amend = correct commit message 
git reset hi.py = take hi.py out of staging area
git log --oneline = show u id of past commits
git reset a99e157 --hard = go back to a commit as it was
git checkout 21fcf57f8da287597f653a6ad8a2526cae85b04e hi.py = get hi.py to the version it was on that commit
git log --all --graph = show all logs in graph view
git config --global alias.s "status" = make status = s
git remote add = add remote  repo
git remote = show remote repos
git remote remove = delete remote repos
git push  origin main --set-upstream = set up a shortcut for u to write only git push
git push -f = force pushing if u wanna oberwite a commit
git pull = pull all the changes in the remote repo to the local one
![[Screenshot from 2024-01-11 20-48-42.png]]

![[Screenshot from 2024-01-12 20-38-22.png]]

  FIX: "Support for password authentication was removed. Please use a personal access token instead :
   git remote set-url origin https://tokenhere@github.com/user_name/repo_name.git :
      git remote set-url origin https://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@github.com/imranelalami/myjourney.git

![[git-github-reference.pdf]]




# vim
dd = delete whole line
l = move right
h = move left
k = move up
j = move down
w = move by word
b = move by word
29k = move 29 line up
16j = move 16 line down
u = redo 
cntr + r = redo redo 
d3l = remove 3 letters
d3j remove 3 lines
d2w = delete 2 words 
d5w = delete 5 words
v = go in visual mode 
y = copy 
p = past 
f( = jump to ( character 
dfr = delete anthing to the r
o = make a new line an+ go insert 
O = make a new line up an+ o insert


# bash
echo "hello imran" | tr m n = replace all m letters with n letters
echo "hello imran" | sed 's/ /n/g' = replace all the space with n 