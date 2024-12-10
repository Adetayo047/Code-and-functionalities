# Code-and-functionalities
ssh -i Test.pem [ubuntu@34.201.163.61](mailto:ubuntu@34.201.163.61) to access aws with the key

for my vpn :   ssh -p 9091 [philip@154.120.65.34](mailto:philip@154.120.65.34)

password : TKg1xB3##

ssh -p 9001 [unicconai@154.120.65.34](mailto:unicconai@154.120.65.34)

# To track the work of my team and know what people are doing

w

sudo aureport -u -i
sudo ausearch -ua j<username> -i

sudo ausearch -ua jude -i

# To deactivate an envirioment

- `source /home/philip/.vscode-server/extensions/ms-python.python-2024.8.1/python_files/deactivate/bash/deactivate`

# Using nohup to run a script

nohup python [downAudio.py](http://downaudio.py/) > output.log 2>&1 &

nohup docker-compose build --no-cache > output.log 2>&1 &

# Docker

sudo docker-compose up # to bring a set of docker container up

sudo docker-compose down # to bring a set of docker container down

sudo docker-compose down -d # to bring a set of docker container down in a discharge manner

docker load -i ai-apis_speech_synthesis.tar    # this is to extract a .tar zip into docker

# To build an image

- [ ]  docker build -t test:latest .

# To run the image

docker run -p 127.0.0.1:8000:8000 test:latest

docker run -d general_medical_chatbot:latest

docker build -t general_medical_chatbot:latest .

docker compose build --no-cache

nohup docker build -t pidgin_speech_synthesis:latest . > pidgin.log 2>&1 &

nohup docker build --no-cache translationv2:latest .>trans.log 2>&1 &

docker build --pull --no-cache --tag general_medicat_chatbot:latest .

docker-compose build --no-cache pidgin_speech_synthesis

# To filter none images

docker rmi -f $(docker images --filter "dangling=true" -q)

docker prune

docker image prune -f

docker container prune to remove all dangling containers

# To add to docker group

usermod -aG docker glory

id glory   # to check if the id exist in the docker group

docker run --gpus all   -it  \ 
--name speech_synthesis \
--network=host \
-p  10205:1405 # remove
-v /mnt/SDD1/ai-apis/digital_literacy/db:/digital_literacy/db \
-v /mnt/SDD1/ai-apis/api_utils:/digital_literacy/api_utils \
[nvcr.io/nvidia/pytorch:24.03-py3](http://nvcr.io/nvidia/pytorch:24.03-py3) 

docker run --gpus all -it \
--name speech_synthesis \
--network=host \
-v /mnt/SDD1/Speech_synthesis:/mnt/SDD1/Speech_synthesis \
[nvcr.io/nvidia/pytorch:24.08-py3](http://nvcr.io/nvidia/pytorch:24.08-py3)

docker run --gpus 0 -itd --name speech_synthesisV2 --network=host --restart unless-stopped -v /mnt/SDD1/Speech_synthesis:/mnt/SDD1/Speech_synthesis  [nvcr.io/nvidia/pytorch:24.08-py3](http://nvcr.io/nvidia/pytorch:24.08-py3)

docker run --gpus all -it \
--name translation\
--network=host \
-v /mnt/SDD1/Translation:/mnt/SDD1/Translation \
[nvcr.io/nvidia/pytorch:24.08-py3](http://nvcr.io/nvidia/pytorch:24.08-py3)

docker run --gpus all -itd --name translation --network=host --restart unless-stopped -v /mnt/SDD1/Translation:/mnt/SDD1/Translation [nvcr.io/nvidia/pytorch:24.08-py3](http://nvcr.io/nvidia/pytorch:24.08-py3)

docker run --gpus all -it \
--name speech_recognition\
--network=host \
-v /mnt/SDD1/Speech_Recognition:/mnt/SDD1/Speech_Recognition \
 [nvcr.io/nvidia/pytorch:24.07-py3](http://nvcr.io/nvidia/pytorch:24.07-py3)

docker run --gpus 0 -itd --name speech_recognition--network=host --restart unless-stopped -v /mnt/SDD1/Speech_Recognition:/mnt/SDD1/Speech_Recognition [nvcr.io/nvidia/pytorch:24.08-py3](http://nvcr.io/nvidia/pytorch:24.08-py3)

docker run --gpus all -it \
--name LLM \
--network=host \
-v /mnt/SDD1/LLM:/mnt/SDD1/LLM \
[nvcr.io/nvidia/pytorch:24.08-py3](http://nvcr.io/nvidia/pytorch:24.08-py3)

docker run --gpus 1 -itd --name LLM --network=host --restart unless-stopped -v /mnt/SDD1/LLM:/mnt/SDD1/LLM  [nvcr.io/nvidia/pytorch:24.08-py3](http://nvcr.io/nvidia/pytorch:24.08-py3)

# Github

### …or create a new repository on the command line

```
echo "# jomiloju_project" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/uniccongroup/Multi-language.git
git push -u origin main
```

ssh-keygen -t ed25519 -C "[your_email@example.com](mailto:your_email@example.com)" 

cat ~/.ssh/id_ed25519.pub

- Go to [GitHub SSH settings](https://github.com/settings/keys) in your web browser.
- Click **New SSH key**.
- In the "Title" field, add a name for your SSH key (e.g., "Personal Laptop").
- Paste the SSH key you copied into the "Key" field.
- Click **Add SSH key**.
- 

git clone [git@github.com](mailto:git@github.com):username/repository.git

hint:   git config pull.rebase false  # merge
hint:   git config pull.rebase true   # rebase
hint:   git config pull.ff only       # fast-forward only

- [ ]  ls -ld /mnt/SDD1/Llama3_RAG/  to check the kind of read access to the folder
- [ ]  sudo chmod -R 777 /mnt/SDD1/Llama3_RAG/   —-  this is to give permision to the folder
- [ ]  sudo lsof -i :8000 check the PID of the process using it
- [ ]  kill -9 PID
