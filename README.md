Whats docker-collections ?
==========================

Well there are quite a few out there (or so I assume), and what we have here is
probably a lot of things we scattered around the www ...

How this could be used ?
========================

* The short answer -> Ansible
* The loner answer -> [ansible-role-docker-compose-executor](https://github.com/shelleg/ansible-role-docker-compose-executor)

It's a simple mesh-up of tasks which simply either copies compositions from a source folder via ansible copy module or checks out from git (in development atm) the "catch" is git repo must be public (ATM) ...

What brought this to life ?
===========================

Considering the need of some configuration manager / deployment tools to "know"
or infrastructure at some level the idea was that each container / micro-service at some level of the deployment looks like

    jenkins:
      env_file: .env
      image: jenkins:latest
      ports:
        - '8080:8080'
      volumes:
        - ${jenkins_homedir}/:/var/jenkins_home
      restart: always

Which makes a lot of sense over running:

    docker run -d --env_file=.env -v - ${jenkins_homedir}/:/var/jenkins_home jenkins:latest

The next thing you know it your "SWARMING" ... so an exmaple like the one under `docker-compose/discovery/consul-registrator` or `monitoring/prometheus/prometheus-server` is where you can see that in action ...
