
# Deploy Node Image in Azure




## Node Docker Image File

```bash

FROM node:20-alpine3.18

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . . 

EXPOSE 4000 

RUN npm run build

CMD npm run dev
##  Docker Image
```

Create Docker Image
```bash
  docker build -t user-name/image-name:latest .
```


Provide Tag
```bash
 docker tag image-id user-name/image-name:latest
```

 Push Image 
 ```bash
 docker push user-name/image-name:latest
```  
## Demo

1) Go to Azure Website

2) Click on Create a Resource 

3) Click on Web Application



a) Give Name to your Project and Creat resource group 

![App Screenshot](https://scontent.xx.fbcdn.net/v/t1.15752-9/438158247_826880252616841_5503869007353199626_n.png?stp=dst-png_p403x403&_nc_cat=101&ccb=1-7&_nc_sid=5f2048&_nc_ohc=xUNLJDbXMkQQ7kNvgF0mGnv&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_Q7cD1QF3nIBECFQnb3OpHJ58G0-fubRR5Jcu1b_TE1vWv5dyZg&oe=6666B26B)

b) Now Add the image that you have pushed to Docker Hub

![App Screenshot](https://scontent.xx.fbcdn.net/v/t1.15752-9/438154391_754329553352009_7332210224799454525_n.png?stp=dst-png_p403x403&_nc_cat=110&ccb=1-7&_nc_sid=5f2048&_nc_ohc=SHmbE7yvGyYQ7kNvgG3Jw14&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_Q7cD1QFkfjZEYcRg0EIx8fS7_W1Sz_13MyAc6YrTxpfhID6zJw&oe=66668854)

c) Press Reivew+create button an press  create button

d) After the project , go the default domain
![App Screenshot](https://scontent.xx.fbcdn.net/v/t1.15752-9/438158373_790918892998592_8180231081162545236_n.png?stp=dst-png_p403x403&_nc_cat=107&ccb=1-7&_nc_sid=5f2048&_nc_ohc=fgfROvCmRbwQ7kNvgHgUF8y&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.xx&oh=03_Q7cD1QEcuEdPmWL8jsR9argTucR75yPWsXPhoGYnyyBkPTmDzg&oe=66668844)




