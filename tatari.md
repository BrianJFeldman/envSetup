###Tatari Specific

- add tatari folder to desktop (`cd && cd Desktop && mkdir tatari && cd tatari`)
- Clone BE repo (`git clone git@github.com:tatari-tv/philo.git`)
- Clone FE repo (`git clone git@github.com:tatari-tv/philo-fe.git`)
- Create a python virtualenv
  - create it (`pyenv .venv`)
  - use it (`source .venv/bin/activate`)
  - make the shell not weird (`deactivate`)
- install postgresql(`brew cask install postgres && dockutil --add /Applications/Postgres.app`)
  - Open postgres (`open -a Postgres.app`)
    - Add a new env ("+" on the bottom left)
    - select 9.6 and initialize
- follow docs to get BE running
  - pg_restore from a dump into a database, often called tatariprodsnap
  - navigate to localhost:8081/admin
    - add yourself as a user, make yourself and admin, add clients
  - foolow docs to get FE running
    - turn off the mockAPI setting
