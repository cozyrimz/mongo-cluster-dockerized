# create a file named file.key to store a randomly genrated key

'openssl rand -base64 700 > file.key'
This will make a file.key key in the root folder

# set file permissions

'chmod 400 file.key'
Change file.key permission to be 4-0-0
4 meaning Users can read it
0 meaning groups have no permission
0 meaning others have no permission

# create a docker compose file for replica instantiation

MRS-compose.yml -> Mongo Replica Set yaml file

# specify all 3 hosts

# persists volume

# set authentiation with file.key

# CMD - run docker compose

docker-compose -f MRS-compose.yml up -d

# CMD - tear down commands

docker-compose -f MRS-compose.yml down

# CMD - prune, save space

docker volume prune

# References

https://blog.skbali.com/2019/05/mongodb-replica-set-using-docker-compose/
