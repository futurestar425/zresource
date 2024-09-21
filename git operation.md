```
$git clone --mirror old-repo-url new-repo
$cd new-repo
$git remote remove origin
$git remote add origin new-repo-url
```
Command To Change User.
```
$git filter-branch -f --env-filter '
NEW_NAME="senior devloper"
NEW_EMAIL="futurestar425000@gmail.com"

if [ "$GIT_COMMITTER_EMAIL" != "$NEW_EMAIL" ]
then
    export GIT_COMMITTER_NAME="$NEW_NAME"
    export GIT_COMMITTER_EMAIL="$NEW_EMAIL"
fi
if [ "$GIT_AUTHOR_EMAIL" != "$NEW_EMAIL" ]
then
    export GIT_AUTHOR_NAME="$NEW_NAME"
    export GIT_AUTHOR_EMAIL="$NEW_EMAIL"
fi
' --tag-name-filter cat -- --branches --tags

$git push --all
$git push --tags
```


git remote set-url origin https:// token @github.com/futurestar425/blum-mining-telegram-bot.git

git remote set-url origin https://token@github.com/GitHubUser/AwesomeRepo
https://github.com/futurestar425/blum-mining-telegram-bot.git


git remote set-url origin https://token@github.com/forward012/excel-extension.git