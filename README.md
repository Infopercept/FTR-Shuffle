# Invinsense packaging 
Scripts and info for configuring a dynamic Shuffle instance in the Invinsense environment

# Invinsense Shuffle installation
1. Git clone the folder
2. Configure access for Opensearch according to the [install guide](https://github.com/frikky/Shuffle/blob/master/.github/install-guide.md)
3. Set up Shuffle on the server (with docker-compose) WITHOUT creating a user
4. Open configure.py and add API-keys and URLs for all other sources 
5. Install required python packages (requirements.txt) 
6. Run configure.py!


## Base installation guide
- https://github.com/frikky/Shuffle/blob/master/.github/install-guide.md

## Installing Docker on the server
- https://gist.github.com/npearce/6f3c7826c7499587f00957fee62f8ee9
- https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html

## Installed packages
- docker
- docker-compose
- git

## Installing Shuffle
```
cd /home/ec2-user/shuffle
docker-compose up -d
```

# Post install
PS: If you use the docker-compose from this repository, please keep in mind UID should 1010:1010 and NOT 1000:1000 for the CHOWN command. 

## Installation location(s)
- /home/ec2-user/shuffle

## Configuring Shuffle
To configure Shuffle, the only required part is to run the configure.py script

```
pip3 -r install /home/ec2-user/shuffle/requirements.txt
python3 /home/ec2-user/shuffle/configure.py
```

## Contact
- frikky@shuffler.io
