## Unix-Linux-Shell-Variables

A variable is nothing more than a pointer to the actual data. The shell enables you to create, assign, and delete variables.

### Defining Variables

Variables are defined as follows −

``` variable_name=variable_value ```

For example −

``` NAME="Ameen Alam" ```


### Accessing Values

To access the value stored in a variable, prefix its name with the dollar sign ($) −

For example, the following script will access the value of defined variable NAME and print it on STDOUT −

<p style="background: #ccc" >
 Live Demo 
 #!/bin/sh 
 NAME="Zara Ali" 
 echo $NAME 
</p>

### Read-only Variables

Shell provides a way to mark variables as read-only by using the read-only command. After a variable is marked read-only, its value cannot be changed.

For example, the following script generates an error while trying to change the value of NAME −


<p style="background: #ccc" >
#!/bin/sh <br />
NAME="Zara Ali" <br />
readonly NAME<br />
NAME="Qadiri"<br />
</p>


### Unsetting Variables


Unsetting or deleting a variable directs the shell to remove the variable from the list of variables that it tracks. Once you unset a variable, you cannot access the stored value in the variable.

Following is the syntax to unset a defined variable using the unset command −

<p style="background: #ccc" >
unset variable_name
</p>

The above command unsets the value of a defined variable. Here is a simple example that demonstrates how the command works −


<p style="background: #ccc" >
#!/bin/sh <br />
NAME="Zara Ali" <br />
unset NAME <br />
echo $NAME <br />
</p>


