Bootstrap:docker  
From:ubuntu:18.04

%post
    # Installing ubuntu dependencies
    apt-get update
    apt-get install -y libcurl4-gnutls-dev libxml2-dev libssl-dev libmariadb-client-lgpl-dev ibglib2.0-dev libcairo2-dev \
    ghostscript libxt-dev r-base
    apt-get clean
    rm -rf /var/lib/apt/lists/*
    # Installing all R packages
    Rscript -e 'r = getOption("repos"); r["CRAN"] = "https://cran.rstudio.com/"; options(repos = r); install.packages(c("graphics","ggplot2","mvtnorm","cluster","grDevices","png","jpeg","RColorBrewer","Matrix","nnet","methods","splines","stats","utils","lattice","Formula","latticeExtra","ggpubr","survminer","survival","rpart","car","rstatix","survAUC","nricens","Hmisc"))' 
%test
    R --version
