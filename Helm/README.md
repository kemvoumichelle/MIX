### Helm Documentation Links

* [Helm release](https://github.com/helm/helm/releases)
* [Helm Website](https://helm.sh/)
* [Quickstart Guide](https://helm.sh/docs/intro/quickstart/)

* [phcollignon/helm3](https://github.com/phcollignon/helm3)

* [Find, install and publishKubernetes packages](https://artifacthub.io/)


* NOTES.txt: It contents what is going to display on the terminal when someone download and install your chart
* Template: It contents kubernetes objects like deployment, serverce, configmap etc.
* chart.yml: contents the information about the chart
* varlues.yaml: it has all the default configuration values for the chart
* -helpers contents functions. If we have a code that repeat itself many time in the code, we can create functions in -helpers and call those function in the code. This will reduced duplicated lines og code in you manifest files
* tests: The content og this runs first before the actual deployement can happens. If the code in the test folder fails to run, you application will not be deploy in kubernetes. It is usefull if you want to test something before deploying your application
* .helmignore: This is the same like dockerignore, gitignore etc or files that we don't want consider for Helm command