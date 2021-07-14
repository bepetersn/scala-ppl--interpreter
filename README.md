# scala-ppl

Spin up a Scala environment in a Jupyter Notebook (this one being setup for my Principles of Programming Languages class).

If this is useful to you, you should know that the best way I have yet found to work with this is
to run `jupyter notebook` yourself and pass the `--NotebookApp.allow_origin=https://example.com` option, but with the URL equal to where GitPod sets up the Jupyter Notebook server URL to be. Seems like that's generally your GitPod workspace url, prefixed by the Jupyer Server's port number as part of the url, altogether, typically the following command:

    jupyter notebook --NotebookApp.allow_origin=https://8888-$(echo $GITPOD_WORKSPACE_URL | cut -d '/' -f 3)

I've also sometimes needed to pass the `--ip=0.0.0.0` option to get the server visible, or so I thought. 
