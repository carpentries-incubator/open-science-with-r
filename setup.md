---
title: Setup
---

## Option 1: using a Docker image

The preferred option to install all softwares and packages is to use a tailor-made Docker image. See [this nice introduction to Docker here](https://aws.amazon.com/docker/).   

This image is based on the [rocker verse Docker image](https://hub.docker.com/r/rocker/verse) image with three extra R libraries (`skimr`, `plotly` and `nycflights13`). The latest image can be [found at the Science Park Study Group DockerHub](https://hub.docker.com/repository/docker/scienceparkstudygroup/master-gls).


> ## Before you start
>
> Before the training, please make sure you have done the following: 
>
> 1. First, install [Docker desktop](https://www.docker.com/products/docker-desktop) for your operating system.  
> 2. If needed, install Shell Bash: [follow these instructions](http://swcarpentry.github.io/shell-novice/setup.html).
> 3. Open a new Shell Bash window and navigate to a folder that will be your workspace. For instance, you could create a folder named `r-tutorial/` on your Desktop and move inside with the Shell using `cd ~/Desktop/r-tutorial/`. 
> 4. In a Shell Bash window, type the following command: `docker run --rm --name rstudio_instance -v $PWD:/home/rstudio/ -e PASSWORD=mypwd -p 8787:8787 scienceparkstudygroup/master-gls:openr-latest`. This will download a Docker image for the course, create and run a container where RStudio will be running.   
> 4. Navigate to [http://localhost:8787](http://localhost:8787) in your web browser. You should have an RStudio session running. Type `rstudio` as the user name and `mypwd` as your password. 
> 5. To quit, close the web browser window where RStudio is running and exit the Shell too. 
{: .prereq}



> ## Important note
>
> You can save files to your disk when working inside the Docker-powered R session. You need to save them as you would normally. The files (e.g. `my_plot.png`) will be where you were working (the directory from which you launched the Docker container). If you were 
>
{: .callout}


__Docker command-line explanations:__  
- The `--rm` removes the container when it has been run. No need to store it into your computer after use.      
- The `--name` gives a name to the running container for easy retrieval.  
- The `-p 8787:8787` follow the format `-p host_port:container_port`. Therefore the port 8787 inside the container will be exposed to the outside port on the host machine. That way, the running instance of RStudio can be access through the <IP address>:port format.

## Option 2: manual installation
This is the second way to install softwares and packages. It _should_ work but there is no guarantee that it _will_ work since R and packages versions on your machine might be different from the software and package versions used in this lesson. Thus, the preferred way is still to use the Docker image (option 1).  

> ## Before you start
>
> Before the training, please make sure you have done the following: 
>
> 1. Download and install **up-to-date versions** of:
>    - R: [https://cloud.r-project.org](https://cloud.r-project.org)
>    - RStudio: [http://www.rstudio.com/download](http://www.rstudio.com/download) 
>    - Git: [https://git-scm.com/downloads](https://git-scm.com/downloads) 
>
> 2. Within R/RStudio, install these packages:
>    - `tidyverse`
>    - `skimr`
>    - `plotly`
>    - `nycflights13`
>
> To do so, open R and use the `install.packages()` function. 
>
> ~~~
> install.packages("tidyverse")
> install.packages("skimr")
> install.packages("plotly")
> install.packages("nycflights13")
> ~~~
> {: .language-r}
{: .prereq}


{% include links.md %}
