FROM scoringengine/base

COPY bin/setup /app/bin/setup
COPY bin/competition.yaml /app/bin/competition.yaml

COPY docker/worker/resolv.conf /etc/resolv.conf

COPY scoring_engine /app/scoring_engine
RUN pip install -e .

CMD ["./wait-for-port.sh", "mysql:3306", "python", "/app/bin/setup"]
