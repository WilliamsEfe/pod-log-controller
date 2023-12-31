﻿
#  POD CONTROLLER

The pod controller is a kubernetes controller that performs custom actions to a kubernetes application which include:

  

```

1. Listening to kubernetes for new pods

2. Annotating these pods with a timestamp

3. Logging the pods and timestamps to stdout

4. Making deploys to a helm chart (podlog)

5. Only responding to pods with a particular annotation

6. Only responding to pods in namespaces with a particular annotation

7. Implementing leader election

```

  
  

## Getting Started

  

1. Follow the guidelines here to install kubernetes on your machine:

  

https://kubernetes.io/docs/tasks/tools/

  

2. Get a cluster and set it as your current configuration

https://kubernetes.io/docs/tasks/access-application-cluster/configure-access-multiple-clusters/

  
  

## Installation

  


  

 - To push a modified image to docker hub


	```docker build -t <username>/<repository-name>:<tag> .```

  

	```docker push <username>/<repository-name>:<tag>```

  -  To remove and upgrade the chart from helm, run

  

		``` helm uninstall podlog ```

  

		``` helm upgrade --install podlog podlog ```

  
  

## Usage

  

 - In order to specify the namespaces to watch:

	Edit line 12 on ```podlog/values.yaml```

  

- In order to specify the annotation to watch:

	Edit line 13 on ```podlog/values.yaml```

- Run run a custom manifest file containing pods:

	Run ```kubectl <path-to-test-pod.yaml>```

## Screenshots

  

imageedit_2_9013813631.gif![imageedit_2_9013813631](https://user-images.githubusercontent.com/37749047/121085142-69b17400-c7d9-11eb-81b2-4e95e8a830a9.gif)

  

## Contributing

  

Please read [CONTRIBUTING.md](https://www.dataschool.io/how-to-contribute-on-github/) for details on contributions and the process of submitting pull requests.

  

## Support & Contact

  

<div>

<a  href="https://twitter.com/williamsmishael"  ><img  src="https://img.shields.io/twitter/url/http/shields.io.svg?style=social"></a>
  
  

## Contributors ✨

  

Thanks to me ([emoji key](https://allcontributors.org/docs/en/)):

  
  
  

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
