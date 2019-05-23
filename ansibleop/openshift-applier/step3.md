There are parameters that match up with each Template to then create a list of OpenShift objects

Our `ruby-example-template` only has one parameter: `BUILD_NAMESPACE`. 

Let's create a parameter file to set this value:

```
echo 'BUILD_NAMESPACE=ruby-example' > params/ruby/build
```{{execute}}


Now we'll create the parameters for the Project template:

```
cat <<EOM >params/projectrequests/project
NAMESPACE=ruby-example
NAMESPACE_DISPLAY_NAME="Ruby Example"
EOM
```{{execute}}
