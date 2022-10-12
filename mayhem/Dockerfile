FROM python:3.8-bullseye
RUN pip3 install atheris

COPY . /unidecode
WORKDIR /unidecode
RUN python3 -m pip install -r requirements.txt && python3 -m pip install . && chmod +x fuzz/unidecode_fuzz.py

ENTRYPOINT [ ]
CMD ["/unidecode/fuzz/unidecode_fuzz.py"]