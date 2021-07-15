Bootstrap: docker

From: continuumio/miniconda3

%files
    environment.yml
    eukdetect
    rules
    tests
    setup.py

%post
    /opt/conda/bin/conda init bash
    /opt/conda/bin/conda env update --name eukdetect -f environment.yml
    /opt/conda/bin/conda run -n eukdetect /bin/bash -c python setup.py install

%runscript
    /opt/conda/bin/conda run -n eukdetect /bin/bash -c eukdetect "$@"
