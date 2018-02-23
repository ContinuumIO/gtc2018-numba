# Build with:
#     docker build -t numba_gtc2018:latest .
# Run with:
#     nvidia-docker run -p 8888:8888 -it numba_gtc2018:latest
FROM conda_cuda_base:latest

RUN conda install -y scipy matplotlib

RUN git clone https://github.com/ContinuumIO/gtc2018-numba

WORKDIR ./gtc2018-numba

ARG BRANCH="master"
RUN git fetch && git checkout $BRANCH

CMD jupyter notebook --ip=*
