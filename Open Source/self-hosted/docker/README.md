- Prerequisites
  - [Docker Engine v20.10+](https://docs.docker.com/engine/release-notes/20.10/)
- 
     ```
        docker run -d 
         -p 8080:8080 -p 9000:9000
         -v $HOME/flipt:/var/opt/flipt 
         docker.flipt.io/flipt/flipt:latest
     ```
    - `-p 8080:8080`
      - for the UI
      - Open in your desired browser 'localhost:8080'
    - `-p 9000:9000` 
      - for the BE
    - `-v $HOME/flipt:/var/opt/flipt`
      - host-mounted volume (host '$HOME/flipt' -- container '/var/opt/flipt') / stores persistent Flipt data
        - == persist data between container restarts
    - `-v $HOME/flipt/config.yaml:/etc/flipt/config.yaml`
      - optional
      - supply custom configuration
