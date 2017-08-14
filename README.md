# LHCb Presentation template

This template provides a beamer style file, a beamer module, and a pandoc template to use for making beautiful presentations simply. It is customized slighly for UC, but that is easy to replace with different branding.

## Quick setup

Get going fast with the script available at [this link](https://gitlab.cern.ch/hschrein/lhcb_presentation/raw/master/default/setup_pres.sh). This script should be sourced in the directory you want to setup a new presentation in, and the one argument required is the name of the presentation you want to make. It will make a new git repository, and check this repository out as a submodule. The basics will be prepared for you.

A fast method is to run the following in your terminal, replacing `my_presentation_name` with your presentation name:

```bash
curl -s https://gitlab.cern.ch/hschrein/lhcb_presentation/raw/master/default/setup_pres.sh | bash /dev/stdin my_presentation_name
```


## Gitlab builds

If you use GitLab, you can use the CI system to build your pdfs for you. An example file for builds is included when you make a new presentation, and the output is avaible at `https://gitlab.cern.ch/<user>/<reponame>/builds/artifacts/master/file/<presentation_name>.pdf?job=compile_pdf`.

You might need a relative path or HTTPS path in `.gitmodules` to build (see [this page](https://docs.gitlab.com/ce/ci/git_submodules.html)). This is because GitLab CI uses HTTP(S) for all cloning.
