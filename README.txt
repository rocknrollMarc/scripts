A project with some handy scripts that can be used from a bash command line.
Each script should be added to the path by moving it into one of the active bin folders.
An example of such a folder would be /usr/local/bin on most unix system.

Do this as follows on Linux as super user:
# cp scripts/myscript /usr/local/bin
where myscript is the script that you're copying.

Then give executable priviledges:
# chmod +x /usr/local/bin/myscript

You should now be able to execute this in any terminal that you open.

I have a created a folder for each script, or set of scripts.

Have fun!!!

Here are specific instructions for the individual scripts / sets of scripts:

####################################################################################
1. gred

Used for invoking a text editor of choice on a Grails project from the command line.

Ensure that you have the following line in your .bashrc file:
export EDITOR="/path/to/editor"

Now change to the directory of your project:
cd myproject

By simply entering the command, you will receive the following help:

Usage: gred <domain class> [options]
 options:
     -tests       :  open all unit and itegration tests.
     -unit        :  open unit tests
     -integration :  open integration tests
     -int         :  open integration tests
     -builder     :  open test object builders
     -controller  :  open controller
     -service     :  open all services
     -views       :  open all .gsp files for domain class
     -reports     :  open all test reports


An example of using the script:
Having a User domain class with unit and integration tests in your Grails project,
you can open gedit on all the related artifacts by simply typing:
> gred user -all

If you only wanted to see the integration test, you could type:
> gred user -integration
or simply
> gred user -int

It is also noteworthy that the name of the domain class can be written in a case-insensitive 
way for convenience.

2. griffed

Used for invoking a text editor of choice on a Griffon project from the command line.

Ensure that you have the following line in your .bashrc file:
export EDITOR="/path/to/editor"

Now change to the directory of your project:
cd myproject

By simply entering the command, you will receive the following help:

Usage: griffed <group> [options]
 options:
     -controller  :  open controller
     -view        :  open view
     -model       :  open model
     -service     :  open service
     -tests       :  open all unit and itegration tests.
     -unit        :  open unit tests
     -integration :  open integration tests
     -int         :  open integration tests
     -builder     :  open test object builders
     -reports     :  open all test reports
     -all         :  open all artifacts for the group


An example of using the script:
Having a MyGroup with unit and integration tests in your Griffon project,
you can open gedit on all the related artifacts by simply typing:
> griffed mygroup -all

If you only wanted to see the integration test, you could type:
> griffed mygroup -integration
or simply
> griffed mygroup -int

It is also noteworthy that the name of the group can be written in a case-insensitive 
way for convenience.

