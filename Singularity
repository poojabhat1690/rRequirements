BootStrap: docker
From:ubuntu:16.04


%post

        apt-get -y update
        apt-get install -y tzdata && \
        apt-get install -y software-properties-common && \
        add-apt-repository -y -u ppa:certbot/certbot && \
        apt-get install -y libopenblas-dev  libcurl4-openssl-dev libopenmpi-dev openmpi-bin openmpi-common openmpi-doc openssh-client openssh-server libssh-dev wget vim git nano git cmake  gfortran g++ curl wget python autoconf bzip2 libtool libtool-bin r-base-core libxml2-dev



R --slave -e 'source("https://bioconductor.org/biocLite.R")'
R --slave -e 'BiocInstaller::biocLite(c("GenomicRanges"))'
R --slave -e 'BiocInstaller::biocLite(c("biomaRt"))'
R --slave -e 'BiocInstaller::biocLite(c("Biostrings"))'
R --slave -e 'install.packages(c("checkmate", "ggplot2","reshape","dplyr","plyr","tibble"), repos="https://cloud.r-project.org/")'


%environment
export LC_ALL=C
export PATH=$PATH





















