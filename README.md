```py
  _    _                 _       ____        _    
 | |  | |               | |     |  _ \      | |   
 | |  | |_ ____   _____ | |_ ___| |_) | ___ | |_  
 | |  | | '_ \ \ / / _ \| __/ _ \  _ < / _ \| __| 
 | |__| | |_) \ V / (_) | ||  __/ |_) | (_) | |_  
  \____/| .__/ \_/ \___/ \__\___|____/ \___/ \__| 
        | |  Reddit Karma bot by Nyx 
        |_|   
```
##  Reddit Upvote Bot
This script uses lists of account logins to upvote specified posts.

## Instalation
To install a stable version of the code navigate to the [Releases](https://github.com/Nyxqxx/UpvoteBot/releases) tab of this repository and download the latest release.
If no releases are available download the latest up to date code from [the github repository](https://github.com/Nyxqxx/UpvoteBot/archive/refs/heads/main.zip)

## Running the program
#### Open a terminal window in the root of the project
#### Run the below command to install the dependencies of the project
```
pip install -r requirements.txt
```
#### Run the below command to run the program
```
python src/main.py
```

## Running the program using docker
#### Open a terminal window at the root of the project
#### Run the below command to build the docker image
```
docker build --rm -t UpvoteBot .
```
#### Run the below command to run the image in interactive mode
```
docker run --rm -i reddit
```

## Converting user:password lists
The program requires lists in the below format to allow for access to the reddit api.
```
user1:password1:appid1:appsecret1
user2:password2:appid2:appsecret2
```
A convert function is present in the program that converts lists shown in the text block below
```
user1:password1 --> user1:password1:appid1:appsecret1
user2:password2 --> user2:password2:appid2:appsecret2
```

## User requirements

So I need a reddit api upvote bot, since web bots are slow and shit. I think the previous dev reversed reddit apk.

The features need to be:
- Upvote & downvote posts and comments
- Use 1 or more proxies (support for a single rotating proxy)
- Check if the accounts have been suspended before upvoting
- Requests must not be linked in any way (headers)
- Options for delays between upvotes.
- Ability to upvote multiple posts at the same time.
- Option to provide account information in a txt file
