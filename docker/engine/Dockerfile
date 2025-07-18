FROM scoringengine/base

COPY bin/engine /app/bin/engine

COPY docker/worker/resolv.conf /etc/resolv.conf

COPY scoring_engine /app/scoring_engine
RUN pip install -e .

CMD ["./wait-for-container.sh", "bootstrap", "/app/bin/engine"]
