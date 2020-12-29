# For git-filter-repo test

## How to change password
The example story "-f" is specified.
Not specified → Change to "***REMOVED ***"  

Change from "my_password" to "XXXXXXX"
```
git filter-repo -f --replace-text  <(echo “my_password==>XXXXXXX”)
```


Change with regular expression.
```
### single
git filter-repo --replace-text <(echo 'regex:(password:).*==>\1******') 
### dobule
git filter-repo --replace-text <(echo -e "regex:(password:).*==>\1******") 
```

## Check the log

```
git log -p --ignore-space-change 
```

