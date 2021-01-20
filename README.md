# Natsume-Docker-builder :

## Natsume Presentation  :
__Natsume__ is a Cloud build based for docker generation from several environment : `conda` , `anaconda` and `pip` based :
![Docker Chart](media/Natsume_chart.png)
<br/>
<br/>
<br/>
![Docker builder from json and yml environment file ](media/environmentyml.gif)
<br/>
<br/>
<br/>
The `Json file` holds The docker definition and pre and post docker image build.
<br/>
<br/>
<br/>
![Json environment file](media/json.gif)
<br/>
<br/>
<br/>
__Natusme__ binary checks the Json file definition on the remote server.
The `Dockerfile.json` is downloaded and parsed. `yml` definition environement file is checked and adds the python packages to the `Dockerfile`.
The image is built and added to the local repository and then executed automatically.
<br/>
<br/>
<br/>
![Docker builder from json and yml environment file ](media/out.gif)

## Natsume delivery :
__Natsume__ uses secured TLS connection with the server to retrieve the json file and learn about the building process.
<br/>
The secured server chain is hold in app/server-nginx-configuration/client-conf/ :
<br/>
1) Trusted certificate in case of self signed certificate : `nginx-selfsigned.crt`
2) Client certificate : `client.crt`
3) Client private key : `client.key`
