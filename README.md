# limonada
LIpid Membranes Open Network And DAtabase


__Installation__

1. git clone https://github.com/LimonadaMD/LimonadaMD.git
2. pip install requirements/dev.txt
3. apt-get install sqlite3 openbabel
4. sqlite3 db.sqlite3 < db.sqlite3.txt
5. python manage.py migrate
6. python manage.py runserver

__Configuration__

When a topology is added to the database, a verification is made with gromacs or charmm to check its validity.
Add gromacs and charmm bin path at the end of limonada/settings/base.py

Add a cron task to remove temporary files created in the media/tmp directory
  Change the media path in limonada.cron
  copy limonada.cron to /usr/bin/
  execute "crontab -e" and add "0 * * * * /usr/bin/limonada.cron" at the end of the file


