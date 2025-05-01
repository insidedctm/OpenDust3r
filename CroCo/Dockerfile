FROM nvcr.io/nvidia/pytorch:21.02-py3

# Avoid interactive prompts
ENV DEBIAN_FRONTEND=noninteractive

# Update and install essential utilities (optional, but often helpful)
RUN apt-get update && apt-get install -y \
    git \
    wget \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Upgrade the conda install
conda install -n base -c defaults python=3.11 conda=25.3.1

# Activate conda and install habitat-sim with the specified options
#RUN conda install -y -c conda-forge -c aihabitat habitat-sim=*=*bullet*headless*

# Optional: verify installation
#RUN python -c "import habitat_sim; print('Habitat-Sim installed:', habitat_sim.__version__)"

# Default command (optional)
CMD ["/bin/bash"]

