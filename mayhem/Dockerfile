FROM python:3.11-slim

RUN apt-get update && \
    apt-get install -y --no-install-recommends clang && \
    rm -rf /var/lib/apt/lists/*

RUN CLANG_BIN=$(which clang) pip3 install atheris

COPY . /unidecode
WORKDIR /unidecode
RUN python3 -m pip install . && chmod +x fuzz/unidecode_fuzz.py

ENTRYPOINT [ ]
CMD ["/unidecode/fuzz/unidecode_fuzz.py"]
