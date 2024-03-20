
# Bernstein

The goal of the project is to deploy 2 websites, with a Kubernetes infrastructure to handle the trafic.


## Deployment

In postgres.secret.yaml, replace:

```plaintext
POSTGRES_PASSWORD: "{{TODO: YOUR PASSWORD HERE (BASE64 ENCODED)}}"
POSTGRES_USER: "{{TODO: YOUR USER HERE (BASE64 ENCODED)}}"
```

Replace everything between quotes with a password and a user encoded in **BASE64**.
You can use any tool that can encode the data you want.
*i.e.* https://www.base64encode.org/


Make sure **kubectl** tool is configured and connected to your Kubernetes cluster.  
Then apply the configuration to the cluster.

```bash
./apply.sh {POSTGRES_USER} {POSTGRES_DB}
```
## Result

You should be able to access the poll and result web applications with:

Poll Application -> http://poll.dop.io:30021/  
Result Application -> http://result.dop.io:30021/  
Traefik dashboard ->  http://localhost:30042
## Authors 
[![Github Noa](https://img.shields.io/badge/Noa%20Trachez-gray?&logo=github)](https://github.com/Noa-Trachez)  
[![Github Benjamin](https://img.shields.io/badge/Benjamin%20Goussard-grey?logo=github)](https://github.com/BenjaminGoussard)  
[![Github Clément](https://img.shields.io/badge/Clément%20Vandeville-grey?logo=github)](https://github.com/ClementVandvl)  