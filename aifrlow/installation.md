# video script:

1. VirtualBox
1. Ubuntu - https://ubuntu.com/download/desktop (LTS version)
1. Setup new virtual env
    1. enable 64 bit (bios shenanigans)
    1. add video memory
    1. set clipboard to bidirectional (or whatever)
    1. set drag and drop (to whatever you want)
    1. enable EFI
    1. set ram to something larger than 1gb
    1. if possible turn on 3d acceleration
    1. create shared folder
1. insert ubuntu iso into drive
1. run your machine
1. install ubuntu
1. fix resolution
    1. insert guest tools 
    1. if nothing pops up run autorun.sh
    1. restart machine and set up resolution
1. udpate system
    1. sudo apt update
    1. sudo apt upgrade
    1. restart machine
1. install anaconda
    1. https://www.anaconda.com/products/distribution#linux - download correct installer
    1. bash Anaconda3-5.3.1-Linux-x86_64.sh
    1. dont install vscode
    1. restart terminal
1.  create new env
    1. conda create -n airflow_env python=3.10
    1. conda activate airflow_env
1. install and setup airflow
    1. https://www.youtube.com/watch?v=z7xyNOF8tak
1. create a directory for all your airflow projects
1. change airflow config
1. optionally turn off default dags