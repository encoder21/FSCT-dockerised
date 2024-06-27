
FROM python:3.9
RUN git clone https://github.com/encoder21/FSCT.git /app/FSCT
WORKDIR /app/FSCT
RUN pip install -r requirements.txt
CMD python scripts/train.py
# CMD tail -f /dev/null
