
# Assumptions in this composition:

This composition was designed to connect to a mysql server running on the node (and not containarized).
`.my.cnf` file should be edited to suit your needs ...

# Extending it:
You could change the `socket=/tmp/mysql.sock` with `port=3306` and add `host=<your_ip>` just make sure your user and password is allowed to connect from that host.

# Contributions
Add a pull-request with your desired state and we will merge it.
