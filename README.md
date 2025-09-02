# Commands terminal Ubuntu
## For shortening and un-shortening the path in terminal :

```
# START of custom commands

# Save current prompt and shorten it
shortpath() {
    export ORIGINAL_PS1="$PS1"   # store current prompt
    export PS1="\W \$ "          # shorten to current directory only
}

# Restore the original prompt
longpath() {
    export PS1="$ORIGINAL_PS1"   # restore prompt
}

# END of custom commands
```


added to the end of .bashrc

### Commands : 
`shortpath` to shorten the path \
`longpath` to make it long again
