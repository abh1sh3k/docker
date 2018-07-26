FROM r-base:latest

RUN apt-get update && apt-get install -y \
    sudo \
    gdebi-core \
    pandoc \
    pandoc-citeproc \
    libcurl4-gnutls-dev \
    libcairo2-dev/unstable \
    libxt-dev \
    libssl-dev \
    default-libmysqlclient-dev \
    libxml2-dev \
    openjdk-8-jre-headless

RUN R -e "install.packages(c('RMySQL','jsonlite','forecast','httr'), repos='http://cran.rstudio.com/')"

CMD ["Rscript","run.R"]
