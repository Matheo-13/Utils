# Commands terminal Ubuntu
## For shortening and un-shortening the path in terminal :

Add to .bashrc :
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

## For sourcing a specific ROS version :
Add to .bashrc :

```
if [ -f ~/.bash_aliases ]; then
    . ~/.bash_aliases
fi
```

Add to .bash_aliases : 
```
alias RosJazzy='source /opt/ros/jazzy/setup.bash && pyenv shell system'
```

### Commands : 
`shortpath` to shorten the path \
`longpath` to make it long again \
`Ros$Version$` to source the setup.bash for this version and use system python
