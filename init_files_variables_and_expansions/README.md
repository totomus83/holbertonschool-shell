command to display a variable = echo " "
variable name containing the previous working directory = OLDPWD
command to display the exit code of the previous command = echo $?
command to define a new command = alias ... = "..."

exercice 3 :

Create a script that counts the number of directories in the PATH.
echo $PATH | tr -s ':' '\n' | wc -l

exercice 4 :

Create a script that lists environment variables.
= printenv

exercice 5 :

lists all local variables and environment variables, and functions
= set
