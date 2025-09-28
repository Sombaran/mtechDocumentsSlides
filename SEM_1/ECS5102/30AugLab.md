# 30 August 2025

> [Click here for recording](https://cciitpatna-my.sharepoint.com/:v:/r/personal/ecs5102_iitp_ac_in/Documents/Recordings/ECS%205102%20-%20Lecture%20Room-20250830_193226-Meeting%20Recording.mp4?csf=1&web=1&e=fWPNK3&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

## Recap

> [16AugustLab.md](https://github.com/Sombaran/mtechDocumentsSlides/blob/main/SEM_1/ECS5102/16AugLab.md)

## Virtualization 5 key components

- Server virtualization
- Desktop virtualization
  - Coporates use this type of virtualization
  - Can be accessed to anywhere
  - Connect to coporate VPN
- Application virtualization (containerization)
- Storage virtualization
- Network virtualization

## Benifits

- No need to buy hardware
- Cost effective
- Resource optization
- High fault tolerance
- Data replication
- High availibilty

## Limitation

- Performance overhead
- Resource contention

## Cloud and virtualization

- Website should not go down during peak hours
- Solution is self service
  - Creates IAAS
- On demand computing
- Distributed computing
- Cloud is application level
- Every virtualization needs hardware
- Virtualization evolved to containerization
- Run more application rather than more VM
- Cloud adapted virtualization
- Containerization run hardware(OS)

## Cloud services model

- On premises
  - Application
  - Data
  - Runtime
  - Middleware
  - OS
  - Virtualization
  - Server
  - Storage
  - Network
- IaaS
  - Application
  - Data
  - Runtime
  - Middleware
  - OS
- PaaS
  - Application
  - Data
  - For eg email service
- SaaS
  - What software you want

## Cloud deployment model

- By default is public
- Private
- Hybrid (Combination of public and private)
- Community
- Multi

## Virtual machine

- Computer system(guest) created using software (hypervisor) on one physial computer (host) to emulate the functionality of another seperate physical computer

## Demo AWS

- Created AWS free tier account
  - ID __365535501733__
- Created Static website
  - [Click here for static website](https://myfirstawswebsiteriaan.s3.ap-southeast-2.amazonaws.com/index.html)
- Steps to create static website
  - Open S3 bucket service
  - Click _create bucket_
  - Add _name_ for your bucket
  - Click on _create bucket_
  - Once website is created, we need to upload _index.html_ file or _folder with pictures_
  - Click on _index.html_
  - Copy content from _copy URL_
  - Open on browser
    - Error: _Access denied_
  - Go back to page where you clicked _index.html_
  - Navigate to _Properties_  and _enable_ static website option
  - Click on save changes, refresh browser
    - Error: _Access denied_
  - Go back to page where you clicked _index.html_
  - Navigate to _Permission_ and uncheck _block public access_
  - Click on save changes, refresh browser
    - Error: _Access denied_
  - Go back to page where you clicked _index.html_
  - Navigate to _Permission_ and _object ownership_, enable _ACL's enabled_
  - Go back to page where you clicked _index.html_ and select _index.html_
  - Click on _Actions_ and click _Make public using ACL_
  - Click on save changes, refresh browser
