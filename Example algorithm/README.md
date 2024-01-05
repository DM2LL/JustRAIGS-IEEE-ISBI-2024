# JustRAIGS Example Algorithm

This is an example repository for making an algorithm submission for the [JustRAIGS challenge](https://justraigs.grand-challenge.org/). This algorithm is just for inference of your model.

### Task 1: Referral performance
The algorithm will input the images and will output the binary labels (0 or 1) along with the likelihood.

No referable glaucoma: 0, Referable glaucoma:1

![image](https://github.com/yeganehmadadi/JustRAIGS_Challenge_Multi-Label-Classification/assets/44732616/18250910-a78d-40f1-acdc-70d1547a4dca)

### Task 2: Justification performance
The algorithm will output binary labels (0,1) for each ten additional features for only referable glaucoma. For example, if image is classified as referral glaucoma in task 1 then classification of ten additional features is required.

Feature is absent: 0, Feature is present: 1

![image](https://github.com/yeganehmadadi/JustRAIGS_Challenge_Multi-Label-Classification/assets/44732616/8b608cf7-47ce-4c91-943c-566f8a2725dd)

------------------------------------------------------

You can upload your algorithms [here](https://justraigs.grand-challenge.org/). If you have a verified account on Grand Challenge and are accepted as a participant in the JustRAIGS challenge, you should be able to submit your Docker container. If something does not work for you, please do not hesitate to [contact us](mailto:yeganeh.madadi@gmail.com) or add a post to the [forum](https://justraigs.grand-challenge.org).

Here are some links that may also be useful:

* [Tutorial on how to make an algorithm container on Grand Challenge](https://grand-challenge.org/documentation/create-your-own-algorithm/)

* [Docker documentation](https://docs.docker.com/)

* [Evalutils documentation](https://evalutils.readthedocs.io/en/latest/)

* [Grand Challenge documentation](https://comic.github.io/grand-challenge.org/algorithms.html)


### Prerequisites

You will need to have [Docker](https://docs.docker.com/) installed on your system. We recommend using [WSL 2.0](https://learn.microsoft.com/en-us/windows/wsl/install) if you are on Windows to install Linux on Windows with WSL and install Docker there.


### Adapt the container to your algorithm

This codebase uses a not-so-smart algorithm that you may want to adapt to a smarter one that was training using the training data provided on the challenge web page. This section explains how to do that.

#### 1. Change the Dockerfile.

  * You may want to change *FROM pytorch/pytorch* to another base image that already has some machine learning packages installed.
  * Install the required packages.
  * Copy additional files, such as model weights.

#### 2. After developing your algorithm, generate a docker container image.

#### 3. On the page of your new algorithm, go to Containers in the menu on the left and click Upload a Container. Now you can upload your .tar.gz file of the Docker container image. You could also not build the container, but use a GitHub repo. Then you should click Link GitHub Repo instead. It will take some time before your Docker container is Ready. Do not proceed with the following steps, once this is the case.

#### 4. You can try out your algorithm when clicking Try-out Algorithm on the page of your algorithm, again in the left menu.

#### 5. Now, you will make a submission to one of the development or test phases. Go to the [JustRAIGS Challenge page](https://justraigs.grand-challenge.org/) and click Submit. Choose which phase you want to submit to. You choose the algorithm that you just created. Then hit Save. After the processing in the backend is done, your submission should pop up on the leaderboard.
