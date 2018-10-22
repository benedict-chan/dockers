### A DockerFile for setting up Octopress 2 environment

This is not an optimized image. I just try to setup an environment to let me keep on using my old Octopress 2 blog.


#### To simply use it

The Docker image is hosted in Docker Hub: [https://hub.docker.com/r/benedictchan/octopress2/](https://hub.docker.com/r/benedictchan/octopress2/)


To simply use this Docker image, you can just mount your Octopress repository's source branch to the container's `app` folder:

`docker run -ti --rm -p 4000:4000 -v {source_path}:/app benedictchan/octopress2 `


#### How it works

The image is based on Ubuntu, after that it installs:

- Git
- Python
- Ruby

It then install basic Octopress requirments and Bundle Install my Octopress's version of `Gemfile` and `Gemfile.lock`.

So in case you have a different version of them, simple fork this and change to your Gemfile and build your own image.


